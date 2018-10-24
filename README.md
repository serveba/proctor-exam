# proctor-exam

Golang SDK wrapper for ProctorExam v3 API

## How to install the library to be used in your golang project

You must set the following environment variables in order to be able to connect with the ProctorExam API:

``` bash
PE_API_KEY=YOUR_API_KEY
PE_API_SECRET=YOUR_API_SECRET
```

You must also install the library in your GOPATH env:

``` bash
go get -u github.com/serveba/proctor-exam
```

After having env vars configured and library installed, you can call directly the methods from your code. This is an example of how to do it:

``` golang
import (
    ...
    proctorexam "github.com/serveba/proctor-exam"
    ...
)

... 
url, _ := url.Parse("https://yoursubdomain.proctorexam.com")
api, _ := proctorexam.New(proctorexam.BaseURL(url))
exams, _ := api.Exams()
...
```

## ProctorExam Documentation

- Docs index: http://docs.proctorexam.com/
- API docs (v3): http://docs.proctorexam.com/v3/apidoc.html