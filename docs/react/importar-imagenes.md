# Diferentes Formas de Importar Imagenes en React

## Primera Forma
este metodo puede utilizarse para la creacion de links de redes sociales

```jsx
import Facebook from './components/Facebook'
import Instagram from './components/Instagram'
import Pinterest from './components/Pinterest'

//importamos los iconos

function App() {

  const INFORMACION = {
    nombre: 'cesar pablo',
    email: 'cesar@com',
    redes: [
      {
        red: 'Facebook',
        url: 'https://facebook.com'
      },
      {
        red: 'Instagram',
        url: 'https://instagram.com'
      },
      {
        red: 'Pinterest',
        url: 'https://pinterest.com'
      }
    ]
  }

  // creamos un objeto con nuestros iconos
  const SOCIALICONS = {
    Facebook,
    Instagram,
    Pinterest
  }

  return (
    <>
      {/* mapeamos nuestro objeto con la informacion del icono
       o podemos usar un nombre que sea similar al icono  */}

      {INFORMACION.redes.map(({ red, url }) => {
        //creamos nuestra variable Icon donde al mapear
        //nuestro objeto de informacion buscara en nuetro
        //objeto de icons el icono que le corresponde
        // los nombres de Iconos y los componentes de Iconos
        //deben ser iguales para que funcione
        // dejamos la I de Icon como mayuscula para utilizarlo
        //como componente, si es minuscula no funciona
        const Icon = SOCIALICONS[red]
        
          return (
            <li key={url}>{url} <Icon /></li>
          )
         }
        )
      }

    </>


    // en el codigo anterior utilizamos destructuracion por eso van
    //un parentesis y llaves dentro
     <>
      {INFORMACION.nombre}

      {INFORMACION.redes.map(item => {
          const Icon = SOCIALICONS[item.red]

          return (
            <li key={item.url}>{item.url} <Icon /></li>
          )

         }
        )
      }

    </>


  )
}

export default App



```