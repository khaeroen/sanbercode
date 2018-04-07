#### Create a new App

**Create React App **adalah cara terbaik untuk memulai pembuatan SPA\(Single Page Application\). Untuk memulai instalasi dibutuhkan versi Node &gt;= 6.

```
npm install -g create-react-app
create-react-app myApp

cd myApp
npm start
```

#### Hello World & Introducing JSX

```js
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

Tag diatas bukan html ataupun string. Itu disebut sebagai JSX dan JSX adalah ekstensi sintaks untuk JavaScript. React mencakup fakta bahwa logika rendering secara inheren digabungkan dengan logika UI lainnya: bagaimana kejadian ditangani, bagaimana keadaan berubah dari waktu ke waktu, dan bagaimana data disiapkan untuk ditampilkan.

##### Menggabungkan Expressions dalam JSX

```js
formatName = (user) => {
  return user.firstName + ' ' + user.lastName;
}

const user = {
  firstName: 'Harper',
  lastName: 'Perez'
};

const element = (
  <h1>
    Hello, {formatName(user)}!
  </h1>
);

ReactDOM.render(
  element,
  document.getElementById('root')
);
```

#### Rendering an Element

Misalkan, ada tag &lt;div&gt; dalam sebuah file html dengan id "root". **React **biasanya menggunakan satu DOM node. Jika menggunakan dalam sebuah aplikasi yang sudah ada, mungkin akan banyak "root" DOM sebanyak yang akan digunakan. Untuk render sebuah **React Element**, maka harus membawa keduanya ke dalam _ReactDOM.render\(\)._

```js
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));
```

#### React hanya memperbarui apa yang dibutuhkan

```js
function tick() {
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {new Date().toLocaleTimeString()}.</h2>
    </div>
  );
  ReactDOM.render(element, document.getElementById('root'));
}

setInterval(tick, 1000);
```

#### Components dan Props

Cara paling sederhana untuk mendefinisikan component adalah dengan function :

```js
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

atau dengen menggunakan **ES6 classes :**

```js
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

##### Rendering sebuah Component

untuk render sebuah component dapat menggunakan cara :

```js

  ReactDOM.render(<Welcome />, document.getElementById('root'));
  
  // Or
  
  const Welcome = <Welcome />
  
  ReactDOM.render(Welcome, document.getElementById('root'));
```

#### Passing Props to a Component

Props adalah property sebuah component. Di **React**, Props ber status immutable\(Read-Only\). Untuk passing data props dalam sebuah component dapat menggunakan cara seperti berikut :

```js
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

function App() {
  return (
    <div>
      <Welcome name="Sara" />
      <Welcome name="Cahal" />
      <Welcome name="Edite" />
    </div>
  );
}

ReactDOM.render(
  <App />,
  document.getElementById('root')
);
```


