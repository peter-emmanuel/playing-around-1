# Checking rust types
## Checking rust types
### Checking rust types

**Rust** _helper_ function
```
fn type_of<T: std::fmt::Debug>(s: &str, _: &T) -> &'static str {
  let tp = std::any::type_name::<T>();
  println!("{s} has type of {tp}");
  tp
}
```

**Rust** _helper_ function
```
fn option_type<T: std::fmt::Display>(opt: &Option<T) {
  match opt {
    Some(v) => {
      let tp = std::any::type_name::<T>();
      println!("{tp} has value of {v}");
    },
    None => println!("None"),
  }
}
```
