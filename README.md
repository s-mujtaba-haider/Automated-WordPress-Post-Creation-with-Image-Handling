# Automated-WordPress-Post-Creation-with-Image-Handling
This workflow starts by receiving a webhook request containing WordPress post data such as title, content, property ID, and optional images. It validates the payload to ensure required fields are present and checks if WordPress credentials are available. If validation fails, it stops the process and logs an error.

Once validated, the workflow scans the post content for inline images, extracts their URLs, downloads them, and uploads them to the WordPress media library. It then replaces the original external image URLs in the content with the newly uploaded WordPress URLs, ensuring all images are self-hosted.

Finally, it handles the featured image (either using an existing media ID or uploading a new one), cleans the HTML content, and constructs the final post payload. The workflow then creates the post in WordPress as a draft and logs the execution result for monitoring and debugging.
