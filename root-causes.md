# Root Causes

Please copy-paste the final answer that you obtained from the AI for each question. The chat interface has a copy button that you can use to copy each message in Markdown format. Please do NOT include images or screenshots.

## Problem 1

**Problem**: The tags are broken up into individual characters on the post view page.

**Question**: What is the underlying issue that causes this problem to occur and from which component (file) of this project does this issue originate?

**Answer**: The issue occurs because the tags are being improperly processed as a single string instead of an array. When the tags are stored or retrieved, they are split incorrectly, possibly using each character as a delimiter. This issue originates from the backend file responsible for saving or returning the tags, likely apps/backend/src/articles/articles.service.ts. Additionally, the frontend component responsible for rendering the tags, such as apps/frontend/src/app/pages/article/article.component.ts, may not be interpreting the tags array correctly.


## Problem 2

**Problem**: New tags  are not shown on the home page under "Popular Tags", even after a page refresh.

**Question**: What is the underlying issue that causes this problem to occur and from which component (file) of this project does this issue originate?

**Answer**: The issue occurs because the backend is not updating the "Popular Tags" list when new tags are added during article creation. The API responsible for fetching the "Popular Tags" does not include the newly created tags, or the frontend is not updating its state correctly after a refresh. This issue originates from the backend file that handles tag creation and updates popular tags, likely apps/backend/src/tags/tags.service.ts. It may also involve the frontend component that fetches and displays the popular tags, such as apps/frontend/src/app/pages/home/home.component.ts.

