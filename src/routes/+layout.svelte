<script>
  import "carbon-components-svelte/css/g80.css";
  import Login from "carbon-icons-svelte/lib/Login.svelte";
  import { 
    Form,
    Tile,
    Button,
    TextInput,
    PasswordInput,
    Link
   } from "carbon-components-svelte";

  const handleSubmit = () => {
    fetch("/login", {
      method: "POST"
    });
  };
</script>

<div class="container">
  <div class="app">
    <Tile>
      <Form action="login" method="POST">
        <TextInput name="username" labelText="User name" placeholder="Enter user name ..."/>
        <PasswordInput name="password" labelText="Password" placeholder="Enter password ..."/>
        <Button type="submit" icon={Login}>Login</Button>
      </Form>
      <Link size="sm" href="">Forgot password?</Link>
    </Tile>
  </div>
</div>

<style>
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100vh;
  }
  .app {
    box-shadow:
    0 1.9px 2.5px rgba(0, 0, 0, 0.057),
    0 5px 6.1px rgba(0, 0, 0, 0.076),
    0 10.1px 11.4px rgba(0, 0, 0, 0.086),
    0 19.2px 19.8px rgba(0, 0, 0, 0.092),
    0 38.4px 34.8px rgba(0, 0, 0, 0.1),
    0 101px 74px rgba(0, 0, 0, 0.13);
  }
  form {
    margin-bottom: 16px;
  }
</style>
