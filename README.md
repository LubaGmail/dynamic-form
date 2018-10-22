# Form

## ATTR vs PROPERTY
  Attributes are defined by HTML. Properties are defined by DOM. 
    Some HTML attributes have 1:1 mapping onto properties. ... Some do not 
    - the value attribute specifies the initial value of an input, but the value property specifies the current value

    name='user[full-name]'  - creates user param with [full-name] as its attribute

## this
  Can reference a function
    handleChange(e) {
      this. ..
    }

  or an instance of a class
    handleChange = (e) => {
      this.setState...
    }

## [attr] - variable key 
  handleChange = (e, attr) => {
    this.setState({
      // turns attr param into key in the key/value pair 
      [attr]: e.target.value,
    })
  }