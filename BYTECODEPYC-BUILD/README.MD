# 

```c
(1)|(2)|(3)|(4)|          (5)         |(6)|  (7)
---|---|---|---|----------------------|---|-------
  2|   |   |  0|LOAD_FAST             |  0|(num)
   |-->|   |  2|LOAD_CONST            |  1|(42)
   |   |   |  4|COMPARE_OP            |  2|(==)
   |   |   |  6|POP_JUMP_IF_FALSE     | 12|
   |   |   |   |                      |   |
  3|   |   |  8|LOAD_CONST            |  2|(True)
   |   |   | 10|RETURN_VALUE          |   |
   |   |   |   |                      |   |
  4|   |>> | 12|LOAD_CONST            |  3|(False)
   |   |   | 14|RETURN_VALUE          |   |
```

### 1.The corresponding line number in the source code
### 2.Optionally indicates the current instruction executed (when the bytecode comes from a frame object for example)
### 3.A label which denotes a possible JUMP from an earlier instruction to this one
### 4.The address in the bytecode which corresponds to the byte index (those are multiples of 2 because Python 3.6 use 2 bytes for each instruction, while it could vary in previous versions)
### 5.The instruction name (also called opname), each one is briefly explained in the dis module and their implementation can be found in ceval.c (the core loop of CPython)
### 6.The argument (if any) of the instruction which is used internally by Python to fetch some constants or variables, manage the stack, jump to a specific instruction, etc.
### 7.The human-friendly interpretation of the instruction argument




### 1.Số dòng tương ứng trong mã nguồn
### 2.Tùy chọn cho biết lệnh hiện tại được thực thi (ví dụ: khi mã byte đến từ một đối tượng khung)
### 3.Một nhãn biểu thị một JUMP có thể có từ lệnh trước đó tới lệnh này
### 4.Địa chỉ trong bytecode tương ứng với chỉ số byte (đó là bội số của 2 vì Python 3.6 sử dụng 2 byte cho mỗi lệnh, trong khi nó có thể khác nhau ở các phiên bản trước)
### 5.Tên lệnh (còn gọi là opname), mỗi tên được giải thích ngắn gọn trong mô-đun dis và cách triển khai chúng có thể được tìm thấy trong ceval.c (vòng lặp cốt lõi của CPython)
### 6.Đối số (nếu có) của lệnh được Python sử dụng nội bộ để tìm nạp một số hằng hoặc biến, quản lý ngăn xếp, chuyển đến một lệnh cụ thể, v.v.
### 7.Cách giải thích đối số hướng dẫn thân thiện với con người
