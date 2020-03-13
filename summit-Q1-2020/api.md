Application Program Interface (API)

GRPC
  - server to server only
  - prototool
    - linter
      - ไม่ต้องใส่ comment
  - ทุก method ต้องมี Request & Response
      ```
        service AdminAPI{
          rpc GetUser(GetUserRequest) returns(GetUserResponse)
          rpc GetUserList(GetUserListRequest) returns(GetUserListResponse)

        }
        message GetUserRequest { string id = 200; string first_name = 202; last_name = 201; }
        message GetUserResponse { }
        
        message GetUserListResponse { repeated User records = 201; }
      ```
GraphQL
  - for frontend
  - convention
    - ชื่อเอาตาม code convention
    - พวก list ควรใช้ connection แทน pagination (เพราะมีปัญหาเรื่อง performance ถ้า row > 1M แล้ว offset เยอะๆ)
