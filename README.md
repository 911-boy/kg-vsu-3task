# Linear Algebra Library

Объектно-ориентированная библиотека для операций линейной алгебры на Java. Библиотека предоставляет классы для работы с векторами (2D, 3D, 4D) и матрицами (3x3, 4x4).

## Структура проекта

```
src/main/java/com/yourcompany/math/
    vector/
        Vector2.java
        Vector3.java
        Vector4.java
    matrix/
        Matrix3x3.java
        Matrix4x4.java
src/test/java/com/yourcompany/math/
    vector/
        Vector2Test.java
        Vector3Test.java
        Vector4Test.java
    matrix/
        Matrix3x3Test.java
        Matrix4x4Test.java
```
## Использование

### Векторы

#### Vector2 (2D вектор)
```java
import com.yourcompany.math.vector.Vector2;

// Создание вектора
Vector2 v1 = new Vector2(1.0, 2.0);
Vector2 v2 = new Vector2(3.0, 4.0);

// Операции
Vector2 sum = v1.add(v2);
Vector2 diff = v1.subtract(v2);
Vector2 scaled = v1.multiply(2.0);
Vector2 divided = v1.divide(2.0);

// Векторные операции
double length = v1.length();
Vector2 normalized = v1.normalize();
double dot = v1.dotProduct(v2);
```

#### Vector3 (3D вектор)
```java
import com.yourcompany.math.vector.Vector3;

Vector3 v1 = new Vector3(1.0, 2.0, 3.0);
Vector3 v2 = new Vector3(4.0, 5.0, 6.0);

// Все операции Vector2 плюс:
Vector3 cross = v1.crossProduct(v2); // Векторное произведение
```

#### Vector4 (4D вектор)
```java
import com.yourcompany.math.vector.Vector4;

Vector4 v1 = new Vector4(1.0, 2.0, 3.0, 4.0);
Vector4 v2 = new Vector4(5.0, 6.0, 7.0, 8.0);

// Аналогично Vector2 и Vector3
```

### Матрицы

#### Matrix3x3
```java
import com.yourcompany.math.matrix.Matrix3x3;
import com.yourcompany.math.vector.Vector3;

// Создание матрицы
double[][] data = {
    {1.0, 2.0, 3.0},
    {4.0, 5.0, 6.0},
    {7.0, 8.0, 9.0}
};
Matrix3x3 m = new Matrix3x3(data);

// Фабричные методы
Matrix3x3 identity = Matrix3x3.identity();
Matrix3x3 zero = Matrix3x3.zero();

// Операции
Matrix3x3 sum = m1.add(m2);
Matrix3x3 diff = m1.subtract(m2);
Matrix3x3 product = m1.multiply(m2);
Matrix3x3 transposed = m.transpose();

// Умножение на вектор
Vector3 v = new Vector3(1.0, 2.0, 3.0);
Vector3 result = m.multiply(v);

// Дополнительные операции
double det = m.determinant();
Matrix3x3 inverse = m.inverse();

// Решение системы уравнений A * x = b
Vector3 x = Matrix3x3.solveSystem(A, b);
```

#### Matrix4x4
```java
import com.yourcompany.math.matrix.Matrix4x4;
import com.yourcompany.math.vector.Vector4;

// Аналогично Matrix3x3, но для 4x4 матриц и Vector4
Matrix4x4 m = new Matrix4x4(data);
Vector4 v = new Vector4(1.0, 2.0, 3.0, 4.0);
Vector4 result = m.multiply(v);
```
Как полностью звучит задание. 
<img width="700" height="776" alt="image" src="https://github.com/user-attachments/assets/4006ed4d-e77a-48c3-97f6-e76bf0368281" />

