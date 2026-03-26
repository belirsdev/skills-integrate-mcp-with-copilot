## Summary
This PR implements data persistence and improved error handling for the Mergington High School Activities API.

## Changes Made
- **Data Persistence**: Activities data is now stored in a JSON file (`activities.json`) instead of in-memory only. Data persists across server restarts.
- **Error Handling**: Added comprehensive validation for inputs, activity capacity checks, and proper HTTP error responses.
- **Validation**: Email domain validation, empty input checks, and duplicate signup prevention.

## Technical Details
- Added `load_activities()` and `save_activities()` functions for JSON file operations.
- Enhanced all API endpoints with try-except blocks and detailed error messages.
- Fallback to default activities if JSON file is missing or corrupted.

## Testing
- Verified data loads correctly on startup.
- Tested sign-up/unregister with validation.
- Confirmed data persists after server restart.

Closes #16