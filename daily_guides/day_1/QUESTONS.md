# question_1

// How much is the current memory capacity of a canister?

# answer_1

{
    "answer_1": "Current memory capacity of a canister 48gb."
}


# question_2

// What is the issue with the following code sample?

actor {
  let counter : Nat = 0;
  public func increment_counter() : async () {
    counter := counter + 1;
  };
}

# answer_2

// var counter : Nat = 0;

{
    "answer_2": "expected mutable assignment target: Variables declared with "let" are immutable. onversely, variables declared with (var) are mutable, which means that their value can be reassigned to a new value at any time using the reassignment operator :=."
}

# question_3

//What is the issue with the following code sample?

actor {
  var message : Text = 0;

  public query func change_message(new_message : Text) : async () {
    message := new_message;
    return;
  };
  
  public query func see_message() : async Text {
    return(message);
  };
}

# answer_3

// var message : Text = "0";

{
    "question_3": "Nat is used for unbounded natural numbers. The type Text is used to represent sequences of characters, such as words or sentences.
}

# question_4

# False or True: we can remove the keyword async for return argument of a query function since queries are faster to answer.

// true

{
    "question_3": "Async: the "async" keyword before the return value indicates that the function will take some time to complete and the caller will have to wait for a response. This is in line with the actor model of canisters, which means that they always respond to requests with a delay."
}