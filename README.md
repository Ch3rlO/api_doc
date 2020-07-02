# The Cesspit of Baghdad 👾

## Each Request should have a token 🔒

**How to send the token**

```json
{
  "Authorization": "YOUR_TOKEN"
}
```

## You can do pagination like that

![PaginationImage](/pagination.png)

**ForExample**

- banners?s=1&p=1 will the first object in page 1

## Useful links

[POST MAN COLLECTION](https://www.getpostman.com/collections/5c320a316d119362c5f8)
[Server Link - AKA - BASEURL](http://139.162.142.73)

## EndPoints 📕

### Admin 🙎

#### Content 📃

##### Post 📄

###### Create ➕

- URL : /post
- Method : POST
- Body :

```json
{
  "title": "STRING|MAX:200|REQUIRED",
  "content": "TEXT|MAX:10000|REQUIRED"
}
```

- Params :
- Query :

###### Get All 😃

- URL : /posts
- Method : GET
- Body :
- Params :
- Query : #pagination

###### Get Single 😃

- URL : /post/:id
- Method : GET
- Body :
- Params : where id ==> postId
- Query :

###### Delete 👍

- URL : /post/:id/activation
- Method : PUT
- Body :
- Params : :id ==> postId
- Query :

###### Update

- URL : /post/:id/edit
- Method : PUT
- Body :

```json
{
  "title": "STRING|MAX:200|REQUIRED",
  "content": "TEXT|MAX:10000|REQUIRED"
}
```

- Params : :id ==> postId
- Query :

##### Banner 📄

###### Create ➕

- URL : /banner
- Method : POST
- Body :

```json
{
  "title": "STRING|MAX:200|REQUIRED",
  "content": "TEXT|MAX:1000|REQUIRED"
}
```

- Params :
- Query :

###### Get 😃

- URL : /banners
- Method : GET
- Body :
- Params :
- Query : #pagination

###### Delete 👍

- URL : /banner/:id/activation
- Method : PUT
- Body :
- Params : :id ==> bannerId
- Query :

###### Update

- URL : /post/:id/edit
- Method : PUT
- Body :

```json
{
  "title": "STRING|MAX:200|REQUIRED",
  "content": "TEXT|MAX:200|REQUIRED"
}
```

- Params : :id ==> postId
- Query :

#### Media 📷

##### Post 🔌

- URL : /add
- Method : POST
- Body :

```json
{
  "moduleType": "STRING|REQUIRED|IN:posts,banners",
  "moduleId": "STRING|REQUIRED|exist:posts,banners",
  "image": "REQUIRED|BINARY"
}
```

- Params :
- Query :

##### DELETE 🔌

- URL : /delete/:hash
- Method : DELETE
- Body :
- Params : hash => name or hash of the file
- Query :

### Applications

** EMPTY **
