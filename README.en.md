# Shhs Project

## Introduction

Shhs is a project based on a custom functional programming language, providing a core set of standard library definitions that emulate Haskell's classic data structures and type classes. It offers foundational tools for common scenarios such as mathematical logic, set operations, and numerical computation. The project uses plain text `.shhs` files as source code, uniformly stored in the repository root directory and the `Data/` subdirectory for modular management and easy extension.

## Project Scale and Structure

```
.
├── Data/
│   ├── Logic.shhs     # Definitions related to logical operations
│   ├── M.shhs         # Types and functions related to Monads
│   ├── Num.shhs       # Numeric type classes and basic arithmetic operations
│   ├── P.shhs         # Support for polymorphism and parametric types
│   └── Set.shhs       # Set data types and set operation functions
├── Prelude.shhs       # Core Prelude definitions containing commonly used general functions
├── haskelldef.shhs    # Definition layer compatible with Haskell syntax
├── all.txt            # Module import summary
└── LICENSE            # Open source license file
```

Where:

- Each module under the **Data/** directory corresponds to a distinct functional domain, implementing foundational abstractions for logic, sets, numbers, etc.;
- **Prelude.shhs** serves as the entry point for the entire language environment, providing core functions and types relied upon by all other modules;
- **haskelldef.shhs** bridges this language’s type system with standard Haskell, enabling reuse of existing Haskell code;
- **LICENSE** specifies the project’s open-source licensing terms.

## Key Features

- **Pure Functional**: All implementations are side-effect-free and adhere to the immutability principle of functional programming;
- **Type Classes**: Polymorphism is achieved via type classes, including common ones such as `Eq`, `Ord`, `Functor`, and `Monad`;
- **Set Operations**: Provides basic set data types and operations such as intersection, union, and complement;
- **Numerical Support**: Implements common arithmetic operations for integer and rational number types;
- **Modular Design**: Functional modules are independent and can be imported on-demand;
- **Haskell Compatibility**: Through the `haskelldef.shhs` layer, interoperability with Haskell’s standard library is enabled.

## Quick Start

### System Requirements

- Any text editor supporting UTF-8 encoding;
- An interpreter or compiler (if an official `shhs` runtime environment is provided);
- Git (for cloning the repository).

### Installation Steps

```bash
# 1. Clone the repository
git clone https://gitee.com/shuangsystem/shhs.git
cd shhs

# 2. View project structure (optional)
ls -R
```

If the project provides an executable script, follow the instructions in the `README` or `INSTALL` file in the repository root to compile or interpret the code.

### Simple Usage Example

Below is the minimal example of loading `Prelude` and performing basic numerical calculations (see internal comments in each module for specific syntax):

```shhs
-- Import the numeric type classes from Prelude
import Prelude

-- Use addition (&#43;) and multiplication (*) defined in Num.shhs
let result = 3 &#43; 4 * 2
in  show result
```

## Module Descriptions

| File | Description |
|------|-------------|
| **Data/Logic.shhs** | Implements boolean values (`Bool`) and common logical operators (`&&`, `||`, `not`, etc.). |
| **Data/M.shhs** | Defines the `Monad` type class and related operators for chained computations and state passing. |
| **Data/Num.shhs** | Implements arithmetic and comparison operators for integers and rationals, along with type class instances. |
| **Data/P.shhs** | Provides support for polymorphic functions and parametric types to build generic algorithm templates. |
| **Data/Set.shhs** | Offers creation and basic set operations: intersection, union, difference, etc. |
| **Prelude.shhs** | The common dependency for all other modules, containing fundamental functions, data types, and type classes. |
| **haskelldef.shhs** | Provides aliases and bridging definitions to support Haskell’s type inference, reducing migration effort. |

> **Tip**: Each `.shhs` file includes inline comments and examples. We recommend reading the documentation strings within each file before practical use.

## License

License information for this project is detailed in the `LICENSE` file. Please comply with its terms when using, modifying, or redistributing the project.

## Contribution Guidelines

We welcome contributions from developers! The main workflow is as follows:

1. **Fork** this repository;
2. Create a new branch off `master` (e.g., `feature/xxx`);
3. After completing development, submit a **Pull Request** with a brief description of your changes;
4. Project maintainers will review and merge your contribution as soon as possible.

Please ensure your code follows the project’s coding style and maintains adequate test coverage before submission.

## Contact

If you have questions or suggestions, please submit an issue via Gitee’s Issues page, or contact the project maintainers directly.

---

Happy coding! Feel free to reach out if you need further assistance.