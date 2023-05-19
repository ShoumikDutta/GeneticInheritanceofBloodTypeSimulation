# Genetic Inheritance of Blood Type Simulation

This C program simulates the genetic inheritance of blood types across multiple generations. It creates a family tree of individuals and randomly assigns blood type alleles to each person based on their parents' alleles.

## Usage

1. Compile the program using a C compiler of your choice (e.g., GCC).
2. Run the compiled executable.
3. The program will generate a family tree and display the blood types of each family member.

## Program Logic

The program uses the following structures and functions to simulate genetic inheritance:

- `person` struct: Represents an individual with two parents and two alleles.
- `create_family(int generations)`: Creates a new individual with the specified number of generations. It recursively creates parents for each generation, assigns their alleles based on their parents, and returns the newly created person.
- `free_family(person *p)`: Frees the memory allocated for the family tree, including all ancestors of a given person.
- `print_family(person *p, int generation)`: Prints each family member and their alleles in a hierarchical format. It recursively traverses the family tree and prints the person's information along with their blood type alleles.
- `random_allele()`: Randomly chooses a blood type allele ('A', 'B', or 'O').

## Example Output

```
Child (Generation 0): blood type AB
  Parent (Generation 1): blood type O
    Grandparent (Generation 2): blood type B
    Grandparent (Generation 2): blood type O
  Parent (Generation 1): blood type A
    Grandparent (Generation 2): blood type A
    Grandparent (Generation 2): blood type O
```

This example shows a family tree with three generations. The child has blood type AB, their parents have blood types O and A, respectively, and their grandparents have blood types B, O, A, and O.

