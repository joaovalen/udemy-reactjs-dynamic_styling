Projeto trabalha com estilização dinâmica baseada em componentes css - EDITA O ARQUIVO PRA VER AS ANOTAÇÕES PQ EM .MD NÃO PEGA
![image](https://user-images.githubusercontent.com/44881948/126157590-31c53293-1c71-47dd-b90f-907e3dc218a5.png)

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

#2 CSS MODULES

import styles from './Button.module.css'

const Button = props => {
  return (
    <button type={props.type} className={styles.button} onClick={props.onClick}>
      {props.children}
    </button>
  );
};
export default Button;

E O ARQUIVO DE CSS TEM QUE TER O .module
