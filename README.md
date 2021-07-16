Most important topics on this project 

#1 Dynamic Styling

const [isValid, setIsValid] = useState(true);

<div className={`login-form ${!isValid ? 'invalid' : ''}`}> 
  <input type="text" onChange={goalInputChangeHandler} />
</div> 

// Caso o state isValid seja falso (!isValid) adicione a string 'invalid' a classe da div, caso não, adicione nada
// Dessa forma a div vai ter ou só a classe login-form ou login-form invalid que deve estar programada no css

.form-control input {
  display: block;
  width: 100%;
  border: 1px solid #ccc;
  font: inherit;
  line-height: 1.5rem;
  padding: 0 0.25rem;
}

.form-control.invalid input {
  border-color: red;
  background: #ffd7d7;
}

