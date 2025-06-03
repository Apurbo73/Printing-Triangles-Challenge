### Printing Triangles Challenge:



---

### 🎯 Goal:

Print this pattern using loops:

```
    *
   ***
  *****
 *******
```

This is a **centered pyramid** with 4 rows.

---

### ✅ Code Breakdown:

```c
int rows = 4;
```

We define `rows = 4` because the pyramid has 4 levels.

```c
for(i = 1; i <= rows; i++) {
```

Outer loop (`i`) controls the **row number**, from 1 to 4.

---

#### 1. **Printing spaces:**

```c
for(space = 1; space <= rows - i; space++) {
    printf(" ");
}
```

* For each row, we need to **center-align** the stars.
* So we print `(rows - i)` spaces before printing stars.

  * Row 1: 3 spaces
  * Row 2: 2 spaces
  * Row 3: 1 space
  * Row 4: 0 spaces

---

#### 2. **Printing stars:**

```c
for(j = 1; j <= (2 * i - 1); j++) {
    printf("*");
}
```

* For each row, we print an **odd number of stars**:
  `(2 * i - 1)` gives:

  * Row 1: 1 star
  * Row 2: 3 stars
  * Row 3: 5 stars
  * Row 4: 7 stars

---

#### 3. **Moving to the next line:**

```c
printf("\n");
```

After printing each row (spaces + stars), we go to the next line.

---

### ✅ Output:

Combining all the loops, we get:

```
    *     ← 3 spaces + 1 star
   ***     ← 2 spaces + 3 stars
  *****     ← 1 space + 5 stars
 *******     ← 0 spaces + 7 stars
```

