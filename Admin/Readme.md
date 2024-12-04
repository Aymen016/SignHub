# 📋 **SignHub - Admin Role Management**

Welcome to the **Admin Dashboard** of **SignHub**, a platform that allows users to learn sign language through video gestures. As an Admin, you have the ability to manage all user-contributed content. This includes adding, editing, and deleting videos submitted by contributors, ensuring that only the most relevant and accurate content is available on the platform.

---

## 🌟 **Admin Features**

- **🎥 Add New Videos**: Admins can add new sign language videos for different gestures and dialects.
- **✏️ Edit Videos**: Edit video details such as title, category, dialect, and video URL.
- **🗑️ Delete Videos**: Remove videos from the platform if they are no longer relevant or do not meet the platform’s standards.
- **📂 Manage Categories**: Create, update, or remove categories for easier video organization.
- **🔧 Video Approval**: Review and approve video content before it becomes publicly visible.

---

## 🛠️ **Admin Endpoints**

Here are the API endpoints specifically for the **Admin Role** in **SignHub**:

### 1. **🎥 Add New Video**
- **Endpoint**: `/admin/videos`
- **Method**: `POST`
- **Description**: Allows the admin to add a new sign language video to the platform.
- **Parameters**:
  - `title (string)`: The title of the video.
  - `dialect (string)`: The dialect of sign language (e.g., Punjabi, Sindhi).
  - `category (string)`: The category of the gesture (e.g., Greetings, Politeness).
  - `video_url (string)`: The URL of the video to be uploaded.
  
- **Example Request**:
  ```json
  {
    "title": "Good Morning Gesture",
    "dialect": "Punjabi",
    "category": "Greetings",
    "video_url": "http://example.com/videos/goodmorning.mp4"
  }
  ```
- **Example Response**:
```json
  {
  "message": "Video added successfully",
  "video_id": 3
  }
```
---

## 2. ✏️ Edit Video
- **Endpoint**: `/admin/videos/<video_id>`
- **Method**: `PUT`
- **Description**: Allows the admin to edit the details of an existing video.
  
### Parameters:
- `title (string)`: New title for the video.
- `dialect (string)`: New dialect for the video.
- `category (string)`: New category for the video.
- `video_url (string)`: New URL for the video.
  
### Example Request:
```json
{
  "title": "Updated Good Morning Gesture",
  "dialect": "Punjabi",
  "category": "Greetings",
  "video_url": "http://example.com/videos/updatedgoodmorning.mp4"
}
```
- **Example Response**:
```json
  {
  "message": "Video details updated successfully",
  }
```
---

## 3. 🗑️ Delete Video
- **Endpoint**: `/admin/videos/<video_id>`
- **Method**: `DELETE`
- **Description**: Allows the admin to delete a video from the platform.

### Example Request:
```plaintext
DELETE /admin/videos/3
```
- **Example Response**:
```json
  {
  "message": "Video deleted successfully",
  }
```

- **Example Response**:
```json
  {
  "message": "Video details updated successfully",
  }
```
---

## 4. 📂 Manage Video Categories

### Endpoint: `/admin/categories`
- **Method**: `POST`
- **Description**: Allows the admin to create a new video category.

### Parameters:
- `category_name (string)`: The name of the new category.

### Example Request:
```json
{
  "category_name": "Emergency Signs"
}
```
- **Example Response**:
```json
  {
  "message": "Category added successfully",
  }
```
---
## Endpoint: `/admin/categories/<category_name>`
- **Method**: `DELETE`
- **Description**: Allows the admin to delete an existing video category.

### Example Request:
```plaintext
DELETE /admin/categories/Emergency Signs
```
- **Example Response**:
```json
  {
  "message": "Category deleted successfully",
  }
```
---
## 📋 **Notes**
- **Video Approval**: Admins should review each user-submitted video for relevance, accuracy, and quality before they are added to the platform.
- **Moderation**: Admins have full control over video content, including the ability to delete inappropriate or low-quality videos.
- **Video Metadata**: All video metadata, including title, dialect, category, and URL, should be updated and maintained for consistency.

---

## 💡 **Future Enhancements**
- **User Feedback**: Introduce a system for users to report inappropriate or low-quality videos.
- **Analytics Dashboard**: Provide admins with a dashboard for video performance analytics (views, ratings, etc.).
- **Batch Editing**: Add functionality for bulk editing or deleting multiple videos at once.

---

## 🎯 **Getting Started**
1. **Login** as an Admin (assuming login functionality is in place).
2. Use the provided API endpoints to manage the video content.
3. Review and approve video submissions from contributors to ensure quality content on the platform.
