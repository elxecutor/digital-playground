# Digital Playground

Digital Playground is a web-based interactive board built with Django and Svelte, designed for creative collaboration and multimedia note-taking. Users can add photos, sticky notes, voice recordings, Spotify tracks, and doodles to a digital canvas, making it ideal for brainstorming, planning, and sharing ideas visually.

## Features

- **Interactive Canvas**: Drag, resize, rotate, and organize items on a flexible board.
- **Add Photos**: Upload or take photos directly and place them on the canvas.
- **Sticky Notes**: Create colorful notes for quick thoughts and reminders.
- **Voice Notes**: Record and add voice messages to the board.
- **Spotify Integration**: Embed tracks, albums, or playlists for collaborative listening.
- **Doodle Tool**: Draw freehand doodles and add them to your board.
- **Export/Import**: Save your board layout as JSON for later use (PNG/PDF export coming soon).
- **Undo/Redo**: Easily revert or repeat actions for flexible editing.
- **Responsive Design**: Works on desktop and mobile devices.

## Technology Stack

- **Backend**: Django (Python)
- **Frontend**: Svelte (JavaScript)
- **Database**: SQLite (default, configurable)
- **Static Assets**: Managed via Django static files

## Getting Started

### Prerequisites
- Python 3.8+
- pip (Python package manager)

### Installation

1. **Clone the repository**
	```bash
	git clone https://github.com/elxecutor/digital-playground.git
	cd digital-playground
	```

2. **Set up Python environment**
	```bash
	python -m venv venv
	source venv/bin/activate
	pip install -r requirements.txt
	```

3. **Apply Django migrations**
	```bash
	python manage.py migrate
	```

4. **Collect static files**
	```bash
	python manage.py collectstatic
	```

6. **Run the development server**
	```bash
	python manage.py runserver
	```

7. **Access the app**
	Open your browser and go to `http://127.0.0.1:8000/`

## Project Structure

```
digital-playground/
├── core/
│   ├── static/_app/immutable/   # Svelte build output
│   ├── models.py                # Django models
│   ├── views.py                 # Django views
│   ├── templates/               # HTML templates
│   └── ...
├── digitalplayground/
│   ├── settings.py              # Django settings
│   ├── urls.py                  # URL routing
│   └── ...
├── db.sqlite3                   # SQLite database
├── manage.py                    # Django management script
├── requirements.txt             # Python dependencies
├── .gitignore                   # Git ignore rules
└── README.md                    # Project documentation
```

## Configuration

- **Static files**: Ensure `STATIC_URL` and `STATIC_ROOT` are set in `settings.py`.
- **Database**: Default is SQLite; update `settings.py` for other databases.
- **Environment variables**: Use a `.env` file for secrets and config.

## Contributing


Please read our [Contributing Guidelines](CONTRIBUTING.md) before submitting issues or pull requests. By participating, you agree to abide by our [Code of Conduct](CODE_OF_CONDUCT.md).

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a pull request

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgements

- Svelte for the frontend framework
- Django for the backend
- Lucide for SVG icons
- Contributors and open-source libraries

