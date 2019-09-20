<script>
  const name = "World";
  fetch("./.netlify/functions/hello", {
    mode: "cors"
  })
    .then(response => response.text())
    .then(text => console.log(text))
    .catch(error => console.log(error));

  // Function using fetch to POST to our API endpoint
  function createTodo(data) {
    return fetch("./.netlify/functions/todos-create", {
      body: JSON.stringify(data),
      method: "POST"
    }).then(response => {
      return response.json();
    });
  }

  // Todo data
  const myTodo = {
    title: "My todo title",
    completed: false
  };

  // create it!
  createTodo(myTodo)
    .then(response => {
      console.log("API response", response);
      // set app state
    })
    .catch(error => {
      console.log("API error", error);
    });    
</script>

<style>
  h1 {
    color: #212121;
  }
</style>

<h1>Hello {name}!</h1>
