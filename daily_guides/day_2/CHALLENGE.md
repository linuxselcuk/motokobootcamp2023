# Write a function average_array that takes an array of integers and returns the average value of the elements in the array.



```
average_array(array : [Int]) -> async Int. 

```

```

// workaround
  actor {

  let array : [var Nat] = [var 1, 2, 3, 4, 5];
  var somme : Nat = 0;
  public func average_array(array : [Int]) : async Nat {
    return array.size();
  };

  public func somme_array() : async Nat {
    for (value in array.vals()) {
      somme := somme + value;
    };
    return somme / array.size();
  };

};



```

# Character count: Write a function that takes in a string and a character, and returns the number of occurrences of that character in the string.

```
count_character(t : Text, c : Char) -> async Nat

```

# Write a function factorial that takes a natural number n and returns the factorial of n.

```
factorial(n : Nat) ->  async Nat

```

```
actor {
  public query func factorial(n : Nat) : async Nat {

    func calculate(m : Nat) : Nat {
      if (m == 0) {
        return 1;
      } else {
        return m * calculate(m - 1);
      };
    };

  return calculate(n);
  };
};
```


# Write a function number_of_words that takes a sentence and returns the number of words in the sentence.

```
number_of_words(t : Text) -> async Nat 
```
```
import Text "mo:base/Text";


actor{

  public func number_of_words(t : Text) : async Nat {
    var a : Nat = 1;
    var b : Text = " ";
      for(c in t.chars()) {
      b := Text.fromChar(c);
      if (b ==  " "){
        a := a +1;
      }
    };
    return a;
  }

};
```


# Write a function find_duplicates that takes an array of natural numbers and returns a new array containing all duplicate numbers. The order of the elements in the returned array should be the same as the order of the first occurrence in the input array.

```
find_duplicates(a : [Nat]) -> async [Nat]

```

```
public func find_duplicatese(a : [Nat]) : async [Nat]  {
  var myArray : [Nat] = Array.reverse(a);
  var finalArray : [Nat] = Array.reverse(myArray);
  return finalArray;
};
```

# Write a function convert_to_binary that takes a natural number n and returns a string representing the binary representation of n.

```
convert_to_binary(n : Nat) -> async Text

```
