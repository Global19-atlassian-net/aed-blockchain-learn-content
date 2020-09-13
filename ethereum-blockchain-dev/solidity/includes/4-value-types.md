# Value Types

In this unit you'll learn about the main value types in Solidity. They are called value types because they will always be passed by value, which means they are copied when they are used. This unit covers the primary value types that you will be exposed to when writing contracts.

## Integers

Integers are used in every Solidity source file. They represent whole numbers and can either be signed or unsigned and range from 8 up to 256 bits.

- Signed: Include negative and positive numbers. Can represent as `int8`
- Unsigned: Includes positive numbers only. Can represent as `uint256`.

If a number of bits is not specified, the default value is 256 bits.

The following operations can be applied to integers:

- Comparisons: `<=`, `<`, `==`, `!=`, `>=`, `>`
- Bit operators: `& (and)`, `| (or)`, `^ (bitwise exclusive)`, `~ (bitwise negation)`
- Arithmetic operators" `+ (addition)`,`- (subtraction)`, `* (multiplication)`, `/ (division)`, `% (modulo)`, `** (exponential)`

Here are some examples of integer definitions:

```solidity
int32 price = 25; // signed 32 bit integer
int256 balance = 1000; // signed 256 bit integer

balance - price; // 975
2 * price; // 50
price % 2; // 0
```

## Booleans

Booleans are defined using the keyword `bool` and always have the values **true** or **false**.

They can be defined as:

```solidity
bool forSale; //true if an item is for sale
bool purchased; //true if an item has been purchased
```

Booleans are commonly used in comparison statements. For example:

 ```solidity
if(balance > 0 & balance > price) {
    return true;
}

if(price > balance) {
    return false;
}
 ```

And booleans can also be used in function parameters and return types.

```solidity
function buy(int price) returns (bool success) {
    // ...
}
```

## String literals

String literals are also used in most contract files. They are characters or words surrounded by either double or single-quotes.

```solidity
    String shipped = "shipped"; // shipped
    String delivered = 'delivered'; // delivered
    String newItem = "new" "Item"; // newItem
```

Additionally, the following escape characters can be used with string literals:

- `\<newline> escapes a new line
- `\n` new line
- `\r` carriage return
- `\t` tab

## Address

An address is a type with a 20 byte value that represents an Ethereum user account. This type can either be a regular **address** or an **address payable**.

The difference between the two is that an **address payable** type is an address that you can send Ether to, and it contains the additional members `transfer` and `send`.

```solidity
address payable public seller; // account for the seller
address payable public buyer; // account for the user

function transfer(address buyer, uint price) {
    buyer.transfer(price); // the transfer member transfers the price of the item
}
```

## Enums

Enums allow you to create a user-defined type in Solidity. It's called user-defined, because the person creating the contract decides the values to include. They present a number of choices that can be selected and require at least one selection.

An example of an **enum** is having different statuses for an item. You can think of these as representing multiple choice answers, where all the values are pre-defined and you have to select one. Enums can be declared in contract or library definitions.

```solidity
    enum StateType {
      ItemAvailable,
      ItemBought
    }

StateType public State;

constructor() public {
    State = StateType.ItemAvailable;
}
```

```solidity
    enum Status { Pending, Shipped, Delivered }
    Status public status;

    constructor() public {
        status = Status.Pending;
    }
}
```
