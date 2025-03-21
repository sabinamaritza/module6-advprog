## Reflection

#### Commit 2
![commit 2 screen capture](/assets/images/commit2.png)

#### Commit 3
![commit 3 screen capture](/assets/images/commit3.png)

#### Commit 4
```
"GET /sleep HTTP/1.1" => {
            thread::sleep(Duration::from_secs(10));
            ("HTTP/1.1 200 OK", "hello.html")
        }
```
Because of the code snippet above, when opening `127.0.0.1/sleep` the server would sleep for 10 seconds before responding. Because the code only has a single thread and is working synchronously, if you try to open `127.0.0.1/` right after, it would also have to wait 10 seconds, even though it should've opened straight away had it not been for the sleep request.