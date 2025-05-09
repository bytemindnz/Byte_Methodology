# Research Methodology Section Generator

This app helps you generate a research methodology section by answering a few questions. It recommends the best template and fills in as much as possible for you.

## Getting Started

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Start the development server:**
   ```bash
   npm start
   ```

3. **Open your browser:**
   Visit [http://localhost:3000](http://localhost:3000)

4. **Build the macOS Electron app (.dmg):**
   ```bash
   npm run build:electron
   ```
   The installer will be created in the `dist/` directory. Open the `.dmg` file to install the app on your Mac (Apple Silicon supported).

## Project Structure
- `src/` - React app source code
- `public/` - Static HTML

## Features (in progress)
- Dynamic question form
- Live template matching
- Template preview and export
- Auto-updates from GitHub releases

## Releasing Updates

The application uses `electron-updater` to automatically check for and install updates from GitHub releases. Here's how to create a new release:

1. **Update the version number** in `package.json`

2. **Build the application for all platforms**:
   ```bash
   npm run electron:build:all
   ```

3. **Create a new GitHub release**:
   - Go to your [GitHub repository](https://github.com/bytemindnz/Byte_Methodology/releases)
   - Click "Draft a new release"
   - Set the tag version to match your package.json version (e.g., `v1.0.1`)
   - Set the release title (e.g., "Version 1.0.1")
   - Add release notes describing the changes
   - Upload the built files from the `dist/` directory
   - Publish the release

4. **Auto-updates will now work** for users with the previous version installed

## Version Scheme

Follow semantic versioning:
- `1.0.0` - Major version (breaking changes)
- `0.1.0` - Minor version (new features, non-breaking)
- `0.0.1` - Patch version (bug fixes)

## For template polishing and matching, use the prompt below:
```
I need you to refine the 'content' of @templates.json, ensuring the placeholders in the content elegantly match those in @placeholders.json.

If necessary, use your best judgment to make changes to 'content' for consistency with the placeholder JSON.

Also, please refine the display of 'content' to be clean, structured, and consistent. For tables, ensure they display properly.

Check through @templates.json and make your best effort to improve the content for me.

Just do Template 9, Template 11, and Template 12 in @templates.json