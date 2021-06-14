# Django and React http requests :rocket:

This is a list of http requests with http-headers.

:suspect: Just to remind that you can allocate these request both in `componentDidMount()` for class based component or `UseEffect()` function based component. 
### React with Fetch and Axios:

:arrow_forward: GET + Fetch
```javascript
const headers = { 'Content-Type': 'application/json' }
fetch('https://api.npms.io/v2/search?q=react', { headers })
    .then(response => response.json())
    .then(data => this.setState({ totalReactPackages: data.total }));
```

:arrow_forward: GET + Axios
```javascript
const headers = {
    'Authorization': 'Bearer my-token',
    'My-Custom-Header': 'foobar'
};
axios.get('https://api.npms.io/v2/search?q=react', { headers })
    .then(response => this.setState({ totalReactPackages: response.data.total }));
```
\
&nbsp;

:arrow_forward: POST + Fetch
```javascript
const requestOptions = {
    method: 'POST',
    headers: { 
        'Content-Type': 'application/json',
        'Authorization': 'Bearer my-token',
        'My-Custom-Header': 'foobar'
    },
    body: JSON.stringify({ title: 'React POST Request Example' })
};
fetch('https://reqres.in/api/posts', requestOptions)
    .then(response => response.json())
    .then(data => this.setState({ postId: data.id }));
```

:arrow_forward: POST + Axios
```javascript
const article = { title: 'React POST Request Example' };
const headers = { 
    'Authorization': 'Bearer my-token',
    'My-Custom-Header': 'foobar'
};
axios.post('https://reqres.in/api/articles', article, { headers })
    .then(response => this.setState({ articleId: response.data.id }));
```
\
&nbsp;

:arrow_forward: PUT + Fetch
```javascript
const requestOptions = {
    method: 'PUT',
    headers: { 
        'Content-Type': 'application/json',
        'Authorization': 'Bearer my-token',
        'My-Custom-Header': 'foobar'
    },
    body: JSON.stringify({ title: 'React Hooks PUT Request Example' })
};
fetch('https://jsonplaceholder.typicode.com/posts/1', requestOptions)
    .then(response => response.json())
    .then(data => setPostId(data.id));
```

:arrow_forward: PUT + Axios
```javascript
const article = { title: 'React PUT Request Example' };
const headers = { 
    'Authorization': 'Bearer my-token',
    'My-Custom-Header': 'foobar'
};
axios.put('https://reqres.in/api/articles/1', article, { headers })
    .then(response => this.setState({ updatedAt: response.data.updatedAt }));
```
\
&nbsp;

:arrow_forward: DELETE + Fetch
```javascript
const requestOptions = {
    method: 'DELETE',
    headers: { 
        'Authorization': 'Bearer my-token',
        'My-Custom-Header': 'foobar'
    }
};
fetch('https://jsonplaceholder.typicode.com/posts/1', requestOptions)
    .then(() => setStatus('Delete successful'));
```

:arrow_forward: DELETE + Axios
```javascript
const headers = { 
    'Authorization': 'Bearer my-token',
    'My-Custom-Header': 'foobar'
};
axios.delete('https://reqres.in/api/posts/1', { headers })
    .then(() => setStatus('Delete successful'));
```

Author: [Elias Prado](https://github.com/EliasOPrado) :neckbeard:
