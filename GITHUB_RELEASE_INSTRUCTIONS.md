# GitHub Release Instructions

Follow these steps to manually create a GitHub release with your pre-built binaries:

## 1. Create the Repository (if not already done)

1. Go to https://github.com/bytemindnz/Byte_Methodology
2. If it's an empty repository, you can upload files directly through the web interface

## 2. Upload Core Files (if repository is empty)

1. Click on the "Add file" dropdown and select "Upload files"
2. Upload the following key files:
   - `package.json`
   - `README.md`
   - `.github/workflows/release.yml`
   - Any other essential files for your repository
3. Commit these files directly to the main branch

## 3. Create a Release on GitHub

1. Go to your repository: https://github.com/bytemindnz/Byte_Methodology
2. Click on "Releases" in the right sidebar
3. Click "Create a new release" or "Draft a new release"
4. Enter "v1.0.0" as the tag (GitHub will create it for you)
5. Set "Version 1.0.0" as the release title
6. Add release notes describing the features and changes

## 4. Upload Release Files

Upload the following files from your `dist` directory:
- Methodology Section Generator-1.0.0-arm64.dmg
- Methodology Section Generator-1.0.0-arm64-mac.zip  
- Methodology Section Generator Setup 1.0.0.exe
- latest-mac.yml
- latest.yml

These files enable both the installer download and the auto-update functionality.

## 5. Publish the Release

Click "Publish release" to make it available to users.

## 6. Testing Auto-Update

To test the auto-update:
1. Install the current version (1.0.0) on a test machine
2. Create a new version (e.g., 1.0.1) by:
   - Updating the version in package.json
   - Building new installers
   - Creating a new GitHub release with tag "v1.0.1"
3. The installed app should detect and offer to install the update

## Notes

- The `latest-mac.yml` and `latest.yml` files are required for the auto-update system
- Always include these files in your releases
- Users will receive notification of updates based on their platform (macOS or Windows)
- If you need to authenticate with GitHub CLI later, use:
  ```
  gh auth login
  ``` 