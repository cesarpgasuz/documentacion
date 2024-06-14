# Pasar un custom propierty como props

```jsx
<GaleriaImages color="#db2777" >
```

```jsx
import '@/styles/Galeria.css'

const GaleriaImages = ({ children, color = 'red' }) => {

    return (
        <div className={`flex gap-5 galeria`} style={{ '--color': color }}>
            {children}
        </div>
  )

}
export default GaleriaImages
```

```css
.galeria::-webkit-scrollbar-thumb{
    background: var(--color);
    border-radius: 20px;
}
```