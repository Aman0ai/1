# Food Ordering Website - Django Version

This is a Django-powered version of your food ordering website. It includes all the functionality of your original HTML site plus backend features like user authentication, database storage, and dynamic content management.

## Features

- **User Authentication**: Login/logout functionality
- **Dynamic Food Management**: Add/edit foods through Django admin
- **Shopping Cart**: Session-based cart system
- **Order Management**: Complete order processing
- **Search Functionality**: Search foods by name
- **Responsive Design**: Maintains your original CSS styling
- **Admin Panel**: Easy management of foods, categories, and orders

## How to Run

### Prerequisites
- Python 3.8+ installed
- pip package manager

### Installation Steps

1. **Navigate to the project directory**
   ```bash
   cd "C:\Users\Asus\Desktop\Shivam Project\Earn Proj\Food_ordering_web-main\Food_ordering_web-main"
   ```

2. **Install required packages**
   ```bash
   py -m pip install django pillow
   ```

3. **Run database migrations**
   ```bash
   py manage.py makemigrations
   py manage.py migrate
   ```

4. **Create a superuser (admin account)**
   ```bash
   py manage.py createsuperuser
   ```
   - Username: admin
   - Email: admin@example.com
   - Password: (choose a secure password SamAi0723)

5. **Populate sample data (optional)**
   ```bash
   py manage.py populate_sample_data
   ```

6. **Run the development server**
   ```bash
   py manage.py runserver
   ```

7. **Open your browser and go to**
   ```
   http://127.0.0.1:8000/
   ```

### Admin Access
- **Admin Panel**: http://127.0.0.1:8000/admin/
- **Username**: admin
- **Password**: (the password you set during superuser creation)

## Project Structure

```
food_ordering_web-main/
├── manage.py                 # Django management script
├── food_ordering/           # Main project settings
├── foodstore/               # Main app
│   ├── models.py            # Database models
│   ├── views.py             # Business logic
│   ├── urls.py              # URL routing
│   └── admin.py             # Admin configuration
├── templates/               # Django templates
│   └── foodstore/          # App-specific templates
├── css/                     # Your original CSS files
├── js/                      # Your original JavaScript files
├── img/                     # Your original images
└── media/                   # User uploads (created automatically)
```

## Key Differences from Original

### Before (Static HTML)
- All food data was hardcoded in HTML
- Forms didn't actually work
- No user accounts or authentication
- No database storage
- Shopping cart was just visual

### After (Django)
- **Dynamic Content**: Food items loaded from database
- **Working Forms**: Add to cart, place orders, user login
- **User Authentication**: Real user accounts and sessions
- **Database**: SQLite database with admin management
- **Functional Cart**: Real shopping cart with session storage
- **Order Processing**: Complete order workflow

## Adding New Features

### Add New Food Items
1. Go to http://127.0.0.1:8000/admin/
2. Login with your admin credentials
3. Click on "Foods" under "Foodstore"
4. Click "Add Food" and fill in the details
5. Save and the food will appear on your website

### Add New Categories
1. In admin panel, go to "Categories"
2. Click "Add Category"
3. Fill in name and description
4. Save to see it on your website

### Customize Styling
- Edit `css/style.css` to modify the appearance
- All your original CSS classes are preserved
- Django templates use the same CSS classes

## Troubleshooting

### Common Issues

1. **"Module not found" errors**
   - Make sure you're in the correct directory
   - Run `py -m pip install django pillow`

2. **Database errors**
   - Run `py manage.py migrate` to apply migrations
   - Check if database file exists

3. **Static files not loading**
   - Run `py manage.py collectstatic` if needed
   - Check file paths in templates

4. **Port already in use**
   - Use different port: `py manage.py runserver 8001`
   - Or kill the process using the port

## Next Steps

- **Deploy to Production**: Use PostgreSQL, configure static files
- **Add Payment Gateway**: Integrate Stripe or PayPal
- **Email Notifications**: Send order confirmations
- **Mobile App**: Create API endpoints for mobile app
- **User Registration**: Add signup functionality
- **Reviews & Ratings**: Let users rate foods

## Support

If you encounter any issues:
1. Check the Django error logs in the terminal
2. Verify all files are in the correct locations
3. Make sure all migrations are applied
4. Check that the admin user was created successfully

Your original HTML files are preserved, so you can always go back to the static version if needed!
