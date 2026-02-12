# QuizGame (Desktop Quiz Application)

A Windows desktop quiz game with a clean UI, optional images per question, and a built-in Question Management/Admin panel.  
The project is designed as a lightweight, gamified learning tool (e.g., Mathematics, History, and more).

## Download (Windows)

A ready-to-install Windows package is available here:

- **Windows installer/package**: http://dit.uoi.gr/files/QuizGame.zip

Unzip and run the included executable/installer (depending on the package contents).

## Screenshots

> The following images are stored in the repository under `docs/`.

| Start menu | Login | Register |
|---|---|---|
| <img src="docs/start_menu.png" width="260" /> | <img src="docs/login.png" width="260" /> | <img src="docs/register.png" width="260" /> |

**Gameplay (question screen)**  
![Gameplay](docs/game.png)

**Question Management / Admin panel**  
![Admin panel](docs/admin.png)

## Main Features

- **Gamified quiz flow**
  - Questions presented one-by-one with multiple-choice answers.
  - Player-friendly layout with visual elements (lives/score/progress).
  - Optional **illustration image** per question (image file path stored in the database).

- **Authentication**
  - Login and user registration screens.

- **Question Management (Admin)**
  - Add/modify/delete questions.
  - Attach an image to a question (stored as a filename/path in the database).
  - Difficulty level field for categorizing questions (e.g., Easy / Normal / Difficult).

- **Database-backed content**
  - Quiz sets stored in a local database (commonly SQLite in desktop setups).
  - Easy to expand with new subjects, quizzes, and question banks.

## Repository Structure (suggested)

- `docs/`  
  Screenshots used by this README.
- `assets/` or `images/`  
  Application images and per-question illustrations (if included in the repo).
- `db/` or `data/`  
  Database files / SQL initialization scripts (if included in the repo).
- `src/`  
  Application source code (if the repo contains the full project).

## Using Question Images (recommended)

- Keep question images in a dedicated folder (e.g., `images/`).
- Store only the **filename** (or a relative path like `images/my_image.png`) in the question record.
- Do **not** embed question text or answers in the image. The UI should render text; images should be purely illustrative.

## Build from Source (if the repository includes code)

If this repository includes the full source code (Qt/CMake typical workflow):

1. Install:
   - A C++ compiler (MSVC on Windows recommended)
   - **Qt 6.x**
   - **CMake** + **Ninja** (optional but recommended)

2. Configure & build (example):
   ```bash
   cmake -S . -B build -DCMAKE_BUILD_TYPE=Release
   cmake --build build --config Release
   ```

3. Deploy Qt runtime (Windows):
   - Use `windeployqt` on the built executable folder.

> Adjust the commands to match your local Qt path and generator.

## Contributing

Issues and pull requests are welcome:
- Bug reports: include steps to reproduce + screenshots if possible.
- Feature requests: describe the user story and expected behavior.

## License

Add a license file (`LICENSE`) to clarify reuse and distribution.
