# puff-adder::

<div align="center"><img src="./puff-adder.png" width="100" /></div>

<div align="center">
    <img alt="MIT Licensed" src="https://img.shields.io/badge/license-MIT-blue.svg">
    <img alt="Version Badge" src="https://img.shields.io/badge/version-1..0.0-brightgreen.svg">
</div>

<br>

> **puff_adder** is a small, simple library for intergrating reactivity concepts like signals and observables.

## Installation

```bash
pip install puff-adder
```

## Getting Started

### Making Values Reactive

```python
from puff_adder import signal

name = signal('oarabile')

# this method takes in a function and
# when the value is changed, it passes
# the new variable into that function.
name.subscribe(lambda x: print(x))

# this is both our setter and getter
name.value = 'averylongnamecausewhynot'

# the "name" is printed onto the console
```

### Observing Changes To A Dict

```python
from puff_adder import observe

user = { "name": "oarabile", "age": 19 }

user = observe(user)

user.observer(lambda prop, value: print('The Prop Is ${prop}, and Value Of ${value}'))

user.name = 'john'

# we can even add custom properties
user.location = 'botswana'

# this is printed to the console 👇
# The Prop Is name, and Value Of john
```

## Contributing

We welcome contributions to **rosana.ds**! To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make changes and commit (`git commit -am 'Add new feature'`).
4. Push to your fork (`git push origin feature-branch`).
5. Open a Pull Request.

Feel free to suggest new features and improvements.

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.