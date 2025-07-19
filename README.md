# LAB_SQLAlchemy
 4.2  ศึกษา code จากโปรแกรม

# PSU Note Application

A simple web-based note-taking application built with Flask and SQLAlchemy. Create, edit, and organize your notes with tags for easy categorization and retrieval.

## Features

- ✅ Create notes with title, description, and tags
- ✅ Edit existing notes
- ✅ Delete notes
- ✅ Tag management (create, edit, delete)
- ✅ View notes by tags
- ✅ Responsive Bootstrap UI
- ✅ PostgreSQL database integration

## Prerequisites

- Python 3.8+
- PostgreSQL database
- pip (Python package installer)

## Database Setup

Before running the application, make sure you have PostgreSQL installed and create a database:

```sql
CREATE DATABASE coedb;
CREATE USER coe WITH PASSWORD 'CoEpasswd';
GRANT ALL PRIVILEGES ON DATABASE coedb TO coe;
```

## Installation and Setup

1. **Clone the project**
   ```bash
   git clone https://github.com/PeeranatPathomkul/LAB_SQLAlchemy.git
   ```

2. **Navigate to project directory**
   ```bash
   cd psu_note
   ```

3. **Install dependencies**
   ```bash
   python -m pip install -r requirements.txt
   ```

4. **Run the application**
   ```bash
   python psunote/noteapp.py
   ```

5. **Access the application**
   Open your web browser and go to: `http://localhost:5000`

## Usage

### Creating Notes
1. Click the "Create" button on the homepage
2. Fill in the title, description, and tags (comma-separated)
3. Click "Create" to save your note

### Managing Notes
- **View all notes**: Visit the homepage to see all notes ordered by title
- **Edit notes**: Click the "Edit" button on any note card
- **Delete notes**: Click the "Delete" button (with confirmation dialog)

### Managing Tags
- **View notes by tag**: Click on any tag name to see all notes with that tag
- **Edit tags**: Use the "Edit Tag" button on the tag view page
- **Delete tags**: Use the "Delete Tag" button (removes tag from all notes)

## Project Structure

```
psu_note/
├── psunote/
│   ├── noteapp.py          # Main Flask application
│   ├── models.py           # Database models
│   ├── forms.py            # WTForms definitions
│   └── templates/          # HTML templates
│       ├── base.html
│       ├── index.html
│       ├── notes-create.html
│       ├── notes-edit.html
│       ├── tags-view.html
│       └── tags-edit.html
├── requirements.txt        # Python dependencies
└── README.md              # This file
```

## Dependencies

- Flask - Web framework
- Flask-SQLAlchemy - Database ORM
- Flask-WTF - Form handling
- WTForms-SQLAlchemy - SQLAlchemy integration for forms
- psycopg2 - PostgreSQL adapter

## Configuration

The application uses the following default database configuration:
```python
SQLALCHEMY_DATABASE_URI = "postgresql://coe:CoEpasswd@localhost:5432/coedb"
```

To use a different database, modify the connection string in `noteapp.py`.

## Development

To run in development mode with debug enabled:
```bash
export FLASK_ENV=development  # Linux/Mac
set FLASK_ENV=development     # Windows
python psunote/noteapp.py
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is created for educational purposes.

---

**Happy note-taking! 📝**
