<h1 align="center">Git flow 👋</h1>
<p>
  <img src="https://img.shields.io/badge/version-1.0.0-blue.svg?cacheSeconds=2592000" />
</p>

### Git flow diagram

1. Khi bắt đầu project hãy fork repo project về github của mình sau đó clone repo project về máy local
2. Tạo thêm remote với repo đã fork của mình 
3. Nhận task và tạo branch làm các task
4. Sau khi làm xong task hãy dùng lệnh `git fetch`để cập nhật các code mới nhất từ repo chính
5. Sử dụng lệnh `git rebase master` hoặc merge vs branch master vì nếu trong quá trình làm task có người khác làm xong task và đã được merge vào branch master thì dễ có thể tạo **conflicts** khi mình tạo pull request đến repo project
6. Cách làm trên sẽ đảm khi tạo pull request sẽ luôn trong trạng thái **This branch has no conficts with the base branch**
7. Sau khi đã **rebase** hoặc merge vs branch master và sử lý xong conficts (nếu có) thì dùng lệnh git push <'remote đến repo fork của mình'> <'tên branch'>
8. Gửi full request từ repo fork của mình đến branch master của project
9. Khi tạo full request tạo commit dưới dạng checklist có mấu ở cuối bài
10. Nếu branch master hoặc một ai khác chạy thấy ổn thì sẽ merge pull request **ko tự ý merge** vì có thể có phát sinh lỗi trên máy khác hoặc code tiềm ẩn gây lỗi đến các issue khác

### How to project management

- Mình sẽ sử dụng tính năng tạo issue và project của git để quản lý và lên kế hoạch phát triển
- Ai cũng có thể tạo issue để trao đổi, hoặc sử dụng issue để tạo task 
- Tạo task có thể tạo các lables như bug, documentation,question, ... để dễ hiểu task muốn làm gì
- Khi nhận task hãy kéo task từ TODO qua cột In Progress và Assignees bản thân để ng khác biết ai đang nhận task này
- Sau khi làm xong đợi branch master review rồi merge code và kéo từ cột In Progress qua Done

### Pull request checklist
---

### Description
 (description here)

### Type of change
  (Implement/Fixbug/Release)
### Checklist:
- [ ] I have selected the correct base branch.
- [ ] I have performed a self-review of my own code.
- [ ]  I have commented my code, particularly in hard-to-understand areas.
- [ ]  I have made corresponding changes to the documentation.
- [ ]  My changes generate no warnings.
- [ ]  I ran `yarn test` in the root folder with success and extended the tests to cover all changes.
- [ ]  I have tested my code with an ethereum test network.
