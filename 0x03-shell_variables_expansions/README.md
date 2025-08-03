# 0x03. Shell, init files, variables and expansions

This directory contains scripts that demonstrate usage of shell variables, environment variables, local variables, expansions, and basic arithmetic using Bash.

---

## Tasks

### 0. `<o>`  
**File:** `0-alias`  
Creates an alias named `ls` with the value `rm *`.

### 1. Hello you  
**File:** `1-hello_you`  
Prints `hello <user>`, where `<user>` is the current Linux user.

### 2. The path to success is to take massive, determined action  
**File:** `2-path`  
Adds `/action` to the `PATH` environment variable.

### 3. If the path be beautiful, let us not ask where it leads  
**File:** `3-paths`  
Counts the number of directories in the `PATH` environment variable.

### 4. Global variables  
**File:** `4-global_variables`  
Prints all global environment variables.

### 5. Local variables  
**File:** `5-local_variables`  
Lists all local variables, environment variables, and shell functions.

### 6. Local variable  
**File:** `6-create_local_variable`  
Creates a new local variable `BEST` with the value `School`.

### 7. Global variable  
**File:** `7-create_global_variable`  
Creates a global environment variable `BEST` with the value `School`.

### 8. Every addition to true knowledge is an addition to human power  
**File:** `8-true_knowledge`  
Adds 128 to the value stored in the environment variable `TRUEKNOWLEDGE`.

### 9. Divide and rule  
**File:** `9-divide_and_rule`  
Divides the value in the variable `POWER` by the value in `DIVIDE`.

### 10. Love is anterior to life, posterior to death, initial of creation, and the exponent of breath  
**File:** `10-love_exponent_breath`  
Raises the value of `BREATH` to the power of `LOVE`.

### 11. There are 10 types of people in the world -- Those who understand binary, and those who don't  
**File:** `11-binary_to_decimal`  
Converts a binary number stored in the variable `BINARY` to a decimal number.

### 12. Combination  
**File:** `12-combinations`  
Prints all possible combinations of two lowercase letters (except `oo`), one per line.

### 13. Floats  
**File:** `13-print_float`  
Prints a floating-point number stored in `NUM` with two decimal places.

---

## Advanced Tasks

### 14. Decimal to Hexadecimal  
**File:** `100-decimal_to_hexadecimal`  
Converts a number from base 10 (stored in `DECIMAL`) to hexadecimal.

### 15. Everyone is a proponent of strong encryption  
**File:** `101-rot13`  
Encodes/decode text using ROT13 encryption.

### 16. The eggs of the brood need to be an odd number  
**File:** `102-odd`  
Prints every other line from input, starting with the first.

### 17. I'm an instant star. Just add water and stir.  
**File:** `103-water_and_stir`  
Adds two numbers from custom bases: `WATER` (base "water") and `STIR` (base "stir") and prints the result in base `"bestchol"`.

---

## Usage

To run any of the scripts:
```bash
chmod +x <script_name>
./<script_name>
