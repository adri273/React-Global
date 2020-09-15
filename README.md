# React-Global

## HTML elements
 - ``<> </> == <Fragment></Fragment>``
## Handle elements
- Handle Errors:
```<>
<Input type="text" name="email" aria-describedby="email-errors" />
<Errors id="email-errors" errors={errors} />
</>```
```<div role="alert">
  {props.errors.map((error, index) => (
    <Error {...error} />
  ))}
</div>```

- Handle disabled:
``{
  this.props.disabled && (
    <button type="submit" aria-disabled className="btn-base-primary">
      Submit
    </button>
  );
}``

## Hide content visually accessible to screen readers
``port const visuallyHidden = {
  borderWidth: '0 !important',
  clip: 'rect(1px, 1px, 1px, 1px) !important',
  height: '1px !important',
  width: '1px !important',
  overflow: 'hidden !important',
  padding: '0 !important',
  position: 'absolute !important',
  whiteSpace: 'nowrap !important',  
}``

Hide Visually
``port {visuallyHidden} from '@styles/helper';

const wrapper = {
  ...visuallyHidden,
};

const reviewForm = {
  ...visuallyHidden,
};``
Component
``port VisuallyHidden from '@components/VisuallyHidden';

const Component = props => <VisuallyHidden>Hide this Visually</VisuallyHidden>``

## react-a11y

## react-axe
``showing accessibility errors in the dev console
if(process.env.NODE_ENV !== 'production') {
  import('react-axe').then(axe => {
    axe.(React, ReactDOM, 1000);
    ReactDOM.render(<App />, document.getElementById('root'));
  });
}else {
  ReactDOM.render(<App />, document.getElementById('root'));
}``
## agnostic-axe
Hace lo mismo que react-axe pero consume menos. Buscar más info sobre esto...


## Micro interactions
 - anton skvortsov
 
## GraphQL
Charly POLY @whereischarly 
- ApolloClient
- https://noti.st/charlypoly/y1XzOV/graphql-in-2020#s9UuIba


