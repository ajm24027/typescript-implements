# typescript-implements

### Implements

I'm not sure fully what the difference between implement(ation) of an interface and extends is in practice, or with context. But I know that the main difference is that extends is used to create a child class of a class that's created. Thinking of the protected attributes in the class from last lesson, and how children can access those from a parent class.

Implements here, seem to be dictating behavior of a class, whether a child or not. In our case, implements of the interface are being used on a Magazine and Book Class telling them to contain a "Print" function which we use to just console log information about the printable object.

```typescript
interface Printable {
  print: () => void
}

class Book implements Printable {
  private _title: string
  private _author: string

  constructor(title: string, author: string) {
    this._title = title
    this._author = author
  }

  print() {
    console.log('title' + this._title, ' author ', this._author)
  }
}

class Magazine implements Printable {
  private _name: string

  constructor(name: string) {
    this._name = name
  }

  print() {
    console.log('title' + this._name)
  }
}

const book = new Book('The Great Gatsby', 'F. Scott Fitzgerald')

const magazine = new Magazine('Time Magazine')
```
