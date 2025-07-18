<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "4d5b044c0924d393af3066e03d7d89c5",
  "translation_date": "2025-07-16T09:48:06+00:00",
  "source_file": "03-GettingStarted/01-first-server/README.md",
  "language_code": "vi"
}
-->
### -2- Tạo dự án

Bây giờ bạn đã cài đặt SDK, hãy tiếp tục tạo một dự án mới:

### -3- Tạo các tệp dự án

### -4- Viết mã cho server

### -5- Thêm một công cụ và một tài nguyên

Thêm một công cụ và một tài nguyên bằng cách thêm đoạn mã sau:

### -6 Mã hoàn chỉnh

Hãy thêm đoạn mã cuối cùng cần thiết để server có thể khởi động:

### -7- Kiểm tra server

Khởi động server với lệnh sau:

### -8- Chạy bằng inspector

Inspector là một công cụ tuyệt vời giúp bạn khởi động server và tương tác với nó để kiểm tra hoạt động. Hãy khởi động nó:
> [!NOTE]  
> nó có thể trông khác trong trường "command" vì nó chứa lệnh để chạy một server với runtime cụ thể của bạn/
Bạn sẽ thấy giao diện người dùng sau:

![Connect](/03-GettingStarted/01-first-server/assets/connect.png)

1. Kết nối với server bằng cách chọn nút Connect  
   Khi bạn kết nối với server, bạn sẽ thấy như sau:

   ![Connected](/03-GettingStarted/01-first-server/assets/connected.png)

1. Chọn "Tools" và "listTools", bạn sẽ thấy "Add" xuất hiện, chọn "Add" và điền các giá trị tham số.

   Bạn sẽ thấy phản hồi sau, tức là kết quả từ công cụ "add":

   ![Result of running add](/03-GettingStarted/01-first-server/assets/ran-tool.png)

Chúc mừng, bạn đã tạo và chạy thành công server đầu tiên của mình!

### SDK chính thức

MCP cung cấp các SDK chính thức cho nhiều ngôn ngữ:

- [C# SDK](https://github.com/modelcontextprotocol/csharp-sdk) - Được duy trì phối hợp với Microsoft  
- [Java SDK](https://github.com/modelcontextprotocol/java-sdk) - Được duy trì phối hợp với Spring AI  
- [TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk) - Triển khai TypeScript chính thức  
- [Python SDK](https://github.com/modelcontextprotocol/python-sdk) - Triển khai Python chính thức  
- [Kotlin SDK](https://github.com/modelcontextprotocol/kotlin-sdk) - Triển khai Kotlin chính thức  
- [Swift SDK](https://github.com/modelcontextprotocol/swift-sdk) - Được duy trì phối hợp với Loopwork AI  
- [Rust SDK](https://github.com/modelcontextprotocol/rust-sdk) - Triển khai Rust chính thức  

## Những điểm chính cần nhớ

- Thiết lập môi trường phát triển MCP rất đơn giản với các SDK theo ngôn ngữ  
- Xây dựng server MCP bao gồm tạo và đăng ký các công cụ với các schema rõ ràng  
- Kiểm thử và gỡ lỗi là rất quan trọng để đảm bảo triển khai MCP đáng tin cậy  

## Mẫu ví dụ

- [Máy tính Java](../samples/java/calculator/README.md)  
- [Máy tính .Net](../../../../03-GettingStarted/samples/csharp)  
- [Máy tính JavaScript](../samples/javascript/README.md)  
- [Máy tính TypeScript](../samples/typescript/README.md)  
- [Máy tính Python](../../../../03-GettingStarted/samples/python)  

## Bài tập

Tạo một server MCP đơn giản với một công cụ bạn chọn:

1. Triển khai công cụ bằng ngôn ngữ bạn thích (.NET, Java, Python hoặc JavaScript).  
2. Định nghĩa các tham số đầu vào và giá trị trả về.  
3. Chạy công cụ inspector để đảm bảo server hoạt động đúng.  
4. Kiểm thử triển khai với nhiều đầu vào khác nhau.  

## Giải pháp

[Giải pháp](./solution/README.md)

## Tài nguyên bổ sung

- [Xây dựng Agents sử dụng Model Context Protocol trên Azure](https://learn.microsoft.com/azure/developer/ai/intro-agents-mcp)  
- [Remote MCP với Azure Container Apps (Node.js/TypeScript/JavaScript)](https://learn.microsoft.com/samples/azure-samples/mcp-container-ts/mcp-container-ts/)  
- [.NET OpenAI MCP Agent](https://learn.microsoft.com/samples/azure-samples/openai-mcp-agent-dotnet/openai-mcp-agent-dotnet/)  

## Tiếp theo

Tiếp theo: [Bắt đầu với MCP Clients](../02-client/README.md)

**Tuyên bố từ chối trách nhiệm**:  
Tài liệu này đã được dịch bằng dịch vụ dịch thuật AI [Co-op Translator](https://github.com/Azure/co-op-translator). Mặc dù chúng tôi cố gắng đảm bảo độ chính xác, xin lưu ý rằng các bản dịch tự động có thể chứa lỗi hoặc không chính xác. Tài liệu gốc bằng ngôn ngữ gốc của nó nên được coi là nguồn chính xác và đáng tin cậy. Đối với các thông tin quan trọng, nên sử dụng dịch vụ dịch thuật chuyên nghiệp do con người thực hiện. Chúng tôi không chịu trách nhiệm về bất kỳ sự hiểu lầm hoặc giải thích sai nào phát sinh từ việc sử dụng bản dịch này.