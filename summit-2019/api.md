Application Program Interface (API)

GRPC
  - prototool
    - linter
      - ไม่ต้องใส่ comment
      ```
        service AdminAPI{
          rpc GetUser(GetUserRequest) returns(GetUserResponse)
          rpc GetUserList(GetUserListRequest) returns(GetUserListResponse)

        }
        message GetUserRequest { string id = 200; string first_name = 202; last_name = 201; }
        message GetUserResponse { }
        
        message GetUserListResponse { repeated User records = 201; }
      ```
