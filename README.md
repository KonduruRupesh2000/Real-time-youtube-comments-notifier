# Real-time YouTube Comments Notifier

## Project Overview

This project is designed to notify users of new comments on YouTube videos in real-time. If you own a YouTube video, you will receive notifications whenever someone comments on it. This can be particularly useful in scenarios like conferences (e.g., TEDx), where you might not own the video but still need to follow up on questions or comments in the video’s comment section.

## Key Features

- Real-time notifications for new comments on YouTube videos.
- Notifications are sent via a Telegram chatbot.
- Handles YouTube's pagination to retrieve all comments efficiently.

## Challenges Faced

### Pagination Issue

Google's YouTube API returns paginated results, with a default of 5 videos per page. This posed a challenge in retrieving and processing all videos efficiently.

#### Solutions Implemented

1. **Direct Method:**
   - Set the maximum results per page to 50, the highest allowed by the API. While this improves the situation, it is not the most efficient solution.

2. **Using Python Generator:**
   - Implemented a Python generator to handle pagination seamlessly. This allows for efficient retrieval of comments without being constrained by the pagination limit.

## Implementation Details

### YouTube API Integration

- **API Usage:** Utilizes Google’s YouTube Data API to fetch comments from a specific video.
- **Playlist ID:** Extracted from the YouTube URL to identify the video.

### Notification Deployment

- **Telegram Bot:** The script sends notifications about new comments to a designated Telegram chatbot, ensuring that the user is promptly informed of new interactions on their videos.

## Python Script

The Python script performs the following tasks:

1. **Authentication and Setup:**
   - Authenticates with the Google YouTube Data API.
   - Retrieves the playlist ID from the YouTube URL.

2. **Fetching Comments:**
   - Uses the API to fetch the latest comments.
   - Implements pagination handling to ensure all comments are retrieved.

3. **Sending Notifications:**
   - Sends the retrieved comments to a Telegram chatbot.

This project leverages Python and the YouTube Data API to create a practical solution for real-time comment monitoring, improving the ability to engage with audiences even on videos not owned by the user.

By addressing the pagination issue with efficient coding techniques like generators, the project ensures scalability and effectiveness in real-world applications.
