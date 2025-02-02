# Testing

### 7 Testing Principles

| Principle                         | Description                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------|
| Testing is context dependent      |                                                                                        | 
| Exhaustive testing is impossible  | Perfect testing does not exist                                                         | 
| Defect clustering                 |                                                                                        | 
| Early testing is always preferred | Test as early as possible                                                              | 
| Pesticide paradox                 | When we repeat the same tests, they become ineffective over time                       | 
| Testing shows presence of defects | - Testing can show us that there are problems <br> - CANNOT say that there are no bugs |
| Absence-of-errors fallacy         |                                                                                        | 


### Unit testing

- Each test is `public void`
- `@Before`
  - Gets executed before each test
  - Prepares data for the test


### 3 A Pattern
`Arrange` - Preconditions - The data should correspond to the situation we want to recreate. <br>
`Act` - Test a single behavior. <br>
`Assert` - Post conditions - Expected behavior. <br>

```
@Test
public void depositShouldAddMoney() {
    BankAccount account = new BankAccount(); // Arrange
    account.deposit(50); // Act
    Assert.assertTrue(account.getBalance() == 50); // Assert
}
```

<br>

Exception testing
```
@Test(expected - IllegalArgumentException.class) // Assert
public void depositNegativeShouldNotaddMoney() {
    BankAccount account = new BankAccount(); // Arrange
    account.deposit(-50); // Act
}
```

- [Unit and Integration testing COMPARED](https://www.youtube.com/watch?v=pf6Zhm-PDfQ)

- [Unit testing in Java: Mockist vs classical style](https://www.youtube.com/watch?v=dOVz-VE06X4&list=WL&index=4&t=6s)

- [What is JUnit? | Why Mockito?](https://www.youtube.com/watch?v=eILy4p99ac8&list=WL&index=57)
