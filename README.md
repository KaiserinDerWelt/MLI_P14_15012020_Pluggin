# Converted jQuery modal

## Simple Modal

a)1.	Import the “Modal” component from “jquery-modal/Modal”

   import Modal from "./jquery-modal/Modal";
   
b)2.	Initialize a state to save modal show/hide state:

    const [isOpen, setIsOpen] = useState(false);

c) 3.	Use it in JSX

      <Modal open={isOpen} onClose={handleClose}>
        Hello world!
        </Modal>

### The “Modal” component requires 2 important props (open, onClose)

open: is the state of modal show/hide, when it equals true the modal shows and when it equal false the modal hides
onClose: is a function which set the open state to false for example:

      function handleClose() {
    setIsOpen(false)
       }


## Disable Close
To disable modal close just add “disableClose” to the modal component props:

      <Modal open={isOpen} onClose={handleClose} disableClose>
        Hello world!
</Modal>


## Finally (Login Form)

a) 1. To add the login form style first you need to add “loginForm” to the modal component props:

      <Modal open={isOpen} onClose={handleClose} loginForm>
b) 2. Use h3 as the modal header and p for each section, for example:

      <Modal open={isOpen} onClose={handleClose} loginForm>
    <form onSubmit={handleSubmit}>
        <h3>Login Form</h3>
        <p>
            <label>Username:</label>
            <input type="text" />
        </p>
        <p>
            <label>Password:</label>
            <input type="password" />
        </p>
        <p>
            <button type="submit">Login</button>
        </p>
    </form>
</Modal>


