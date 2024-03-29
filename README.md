**SENG 637 - Software Testing, Reliability, and Quality**

**Lab. Report \#2 – Requirements-Based Test Generation**

| Group \#:      | 20  |
| -------------- | --- |
| Student Names: |     |
| Usman          |     |
| Gopal          |     |
| Jubayer        |     |
| Robby          |     |
| Ehsan          |     |

# 1 Introduction

In this lab exercise, our goal is to implement unit testing for two Java classes within a program, with detailed specifications provided in the Java documentation. To accomplish this, we utilized JUnit frameworks to construct a testing environment comprising mock objects and test cases. The primary objectives of the lab are to get familar with Eclipse, set up a project incorporating specified JAR files, and gain proficiency in Eclipse's JUnit functionality. Additionally, the lab focused on analyzing Java documentation, guiding us to create test cases for the specified classes. During the test case creation process, we were assigned the task of constructing partitions for the selected methods under test. These partitions served as the foundation for developing comprehensive test cases, ensuring a thorough and accurate assessment of each method's functionality.

# 2 Detailed description of unit test strategy

Our unit test strategy draws inspiration from black-box testing principles, particularly Equivalence Class Testing (ECT) and Boundary Value Testing, to ensure comprehensive coverage of our software components. We adopt a systematic approach to partition test inputs into distinct subsets, including generalized legal inputs, inputs near boundaries (encompassing both legal and illegal inputs), and explicit testing of boundary conditions.

This structured approach allows us to design test cases that address various scenarios and edge cases, enhancing the robustness and reliability of our testing process. By adhering to established testing techniques, we aim to uncover potential defects and vulnerabilities within our codebase, thereby mitigating risks and ensuring the overall quality of our software.

Furthermore, we prioritize a thorough understanding of the Java documentation pertaining to the classes and methods under test, enabling us to make informed decisions about the selection and prioritization of test cases. Through this iterative process of analysis and testing, we strive to deliver software that meets the highest standards of functionality and reliability.

Overall, our unit test strategy is characterized by a disciplined approach to test case design, informed by industry best practices and tailored to the specific requirements of our software project.

### Test Plan

# 3 Test cases developed

### Test Methods for RangeTest Class

#### `getLength()`

- `testGetLengthZero` - belongs to the generalized legal inputs partition (valid)
- `testGetLengthLargePositive` - belongs to the generalized legal inputs partition (valid)
- `testGetLengthLargeNegative` - belongs to the generalized legal inputs partition (valid)
- `testGetLengthRangeIsDecimal` - belongs to the generalized legal inputs partition (valid)
- `testGetLengthRangeIsNotDecimal` - belongs to the generalized legal inputs partition (valid)

#### `shift(Range base, double delta)`

- `shiftNullUpperBound` - belongs to the generalized illegal inputs partition (invalid)
- `shiftByPositiveDoubleUpperBound` - belongs to the generalized legal inputs partition (valid)
- `shiftByPositiveDoubleLowerBound` - belongs to the generalized legal inputs partition (valid)
- `shiftByNegativeDoubleUpperBound` - belongs to the generalized legal inputs partition (valid)
- `shiftByNegativeDoubleLowerBound` - belongs to the generalized legal inputs partition (valid)
- `shiftByNegativeDoubleToGetNegativeValueUpperBound` - belongs to the illegal boundary inputs partition (invalid)
- `shiftByNegativeDoubleToGetNegativeValueLowerBound` - belongs to the illegal boundary inputs partition (invalid)

#### `combine(Range range1, Range range2)`

- `combineFirstParameterNullUpperBound` - belongs to the generalized legal inputs partition (valid)
- `combineFirstParameterNullLowerBound` - belongs to the generalized legal inputs partition (valid)
- `combineSecondParameterNullUpperBound` - belongs to the generalized legal inputs partition (valid)
- `combineSecondParameterNullLowerBound` - belongs to the generalized legal inputs partition (valid)
- `combineBothParametersNullLowerBound` - belongs to the generalized legal inputs partition (valid)
- `combineParametersPostiveNegativeUpperBound` - belongs to the generalized legal inputs partition (valid)
- `combineParametersPostiveNegativeLowerBound` - belongs to the generalized legal inputs partition (valid)
- `combineParametersNearZeroBound` - belongs to the legal boundary inputs partition (valid)

#### `getCentralValue()`

- `centralValueAtZero` - belongs to the generalized legal inputs partition (valid)
- `centralValueBetweenPostiveBounds` - belongs to the generalized legal inputs partition (valid)
- `centralValueBetweenNegativeBounds` - belongs to the generalized legal inputs partition
- `centralValuewithLargeBounds` - belongs to the generalized legal inputs partition

#### `getLowerBound()`

- `lowerBoundShouldBeNegOne` - belongs to the generalized legal inputs partition (valid)
- `lowerBoundShouldBePostiveOne` - belongs to the generalized legal inputs partition (valid)
- `lowerBoundShouldBeBigNeg` - belongs to the generalized legal inputs partition (valid)
- `lowerBoundShouldBeBigPositive` - belongs to the generalized legal inputs partition (valid)
- `lowerBoundShouldBeDecimal` - belongs to the generalized legal inputs partition (valid)

### Test Methods for DataUtilitiesTest Class

#### `calculateColumnTotal()`

- `calculateColumnTotalForTwoValues` - belongs to the generalized legal inputs partition (valid)
- `testCalculateColumnTotal_ValidInput` - belongs to the generalized legal inputs partition (valid)
- `testCalculateColumnTotal_NullData` - belongs to the generalized illegal inputs partition (invalid)
- `testCalculateColumnTotal_EmptyTable` - belongs to the generalized legal inputs partition (valid)
- `testCalculateColumnTotal_SingleRow` - belongs to the generalized legal inputs partition (valid)

#### `calculateRowTotal()`

- `testCalculateRowTotal_ValidInput` - belongs to the generalized legal inputs partition (valid)
- `testCalculateRowTotal_NullData` - belongs to the generalized illegal inputs partition (invalid)
- `testCalculateRowTotal_EmptyTable` - belongs to the generalized legal inputs partition (valid)
- `testCalculateRowTotal_SingleColumn` - belongs to the boundary legal inputs partition (valid)

#### `createNumberArray()`

- `testCreateNumberArray_ValidInput` - belongs to the generalized legal inputs partition (valid)
- `testCreateNumberArray_EmptyArray` - belongs to the generalized legal inputs partition (valid)
- `testCreateNumberArray_SingleElement` - belongs to the boundary legal inputs partition (valid)
- `testCreateNumberArray_NullInput` - belongs to the generalized illegal inputs partition (invalid)
- `testCreateNumberArray_NegativeValues` - belongs to the generalized legal inputs partition (valid)

#### `calculateColumnTotal2D()`

- `testCreateNumberArray2D_ValidInput` - belongs to the generalized legal inputs partition (valid)
- `testCreateNumberArray2D_EmptyArray` - belongs to the generalized legal inputs partition (valid)
- `testCreateNumberArray2D_SingleElement` - belongs to the boundary legal inputs partition (valid)
- `testCreateNumberArray2D_NullInput` - belongs to the generalized illegal inputs partition (invalid)

#### `getCumulativePercentages()`

- `testGetCumulativePercentages_ValidInput` - belongs to the generalized legal inputs partition (valid)
- `testGetCumulativePercentages_Empty()` - belongs to the generalized legal inputs partition (valid)
- `testGetCumulativePercentages_NullInput` - belongs to the generalized illegal inputs partition (invalid)
- `testGetCumulativePercentages_NegativeValues` - belongs to the generalized legal inputs partition (valid)
- `testGetCumulativePercentages_AllZeros` - belongs to the generalized legal inputs partition (valid)

# 4 How the teamwork/effort was divided and managed

## Team Work and Effort Division:

As a team comprising Usman, Gopal, Jubayer, Robby, and Ehsan, we organized our efforts effectively to tackle the lab assignment. Recognizing the importance of collaboration and division of labor, we structured our approach accordingly.

### Pair #1 (Usman/Gopal):

This pair took on the responsibility of developing test cases for selected methods in the Range class:

- `getLength()`
- `shift(Range base, double delta)`
- `combine(Range range1, Range range2)`
- `getCentralValue()`
- `getLowerBound()`

### Pair #2 (Jubayer/Robby/Ehsan):

Jubayer, Robby & Ehsan collaborated to develop test cases for the remaining methods in the DataUtilitiesTest class:

- `calculateColumnTotal()`
- `calculateRowTotal()`
- `createNumberArray()`
- `calculateColumnTotal2D()`
- `getCumulativePercentages()`

### Report (Gopal/Ehsan):

The report was developed collaboratively by Gopal & Ehsan and reveiwed by all team members.

## Test Case Development Strategy:

Our approach to creating test cases was inspired by the outlined partitions and specifications provided in the lab documentation. Each pair focused on specific methods within the Range class, ensuring thorough coverage of all partitions identified.

For the `getLength()`, `shift()`, `combine()`, `getCentralValue()` and `getLowerBound()` methods, Pair #1 (Usman/Gopal) meticulously designed test cases corresponding to the generalized legal inputs partition, covering various scenarios such as zero values, largely positive and negative values, decimal ranges, and null inputs. This comprehensive approach aimed to validate the functionality of these methods under different conditions.

Meanwhile, Pair #2 (Jubayer/Robb/Ehsany) concentrated on crafting test cases for the `calculateColumnTotal()`, `calculateRowTotal()`, `createNumberArray()`, `calculateColumnTotal2D()` and `getCumulativePercentages()` methods, targeting the generalized legal inputs partition as well. By ensuring that test cases encompassed a wide range of input values, including zero, positive, negative, nul and decimal values, they aimed to verify the correctness and robustness of these methods.

Throughout the process, all members provided valuable insights and feedback to refine the test cases, ensuring that they were exhaustive and aligned with the objectives of the lab assignment. Overall, by adopting a collaborative and organized approach, we successfully divided and managed the workload, resulting in the comprehensive development of test cases for the specified methods in the Range class.

# 5 Difficulties encountered, challenges overcome, and lessons learned

During the course of our lab work, we encountered several significant challenges that tested our problem-solving skills and teamwork abilities. One of the foremost difficulties we faced was Understanding how to create and effectively utilize mocking objects posed a notable challenge, especially considering the intricacies involved in their implementation.

Another challenge we encountered revolved around effectively splitting the workload among team members. Initially, we struggled to find a balanced approach that would allow each member to contribute meaningfully to the project while ensuring that tasks were completed efficiently. To address this challenge, we decided to divide ourselves into pairs, with each pair responsible for specific tasks. This division of labor not only helped us allocate responsibilities more effectively but also fostered collaboration and communication among team members. By pairing individuals for coding and reviewing tasks, we were able to leverage each other's strengths and expertise, resulting in a more cohesive and productive workflow.

In addition to these internal challenges, we also faced external obstacles that required innovative solutions. One such challenge was the compatibility issues we encountered while attempting to run the JFreeChart demo on MacBook laptops. The windows would not consistently pop up as expected, necessitating a switch to Windows machines for creating the Eclipse project. While this adjustment posed a temporary setback, it underscored the importance of adaptability and resourcefulness in overcoming unforeseen obstacles.

Despite the challenges we encountered, our team was able to navigate through them by leveraging our collective problem-solving skills and resourcefulness. The experience not only strengthened our understanding of software testing principles but also honed our ability to collaborate effectively as a team. By confronting and overcoming these challenges head-on, we emerged from the lab with valuable lessons learned and a greater sense of confidence in our abilities to tackle complex software development tasks in the future.

# 6 Discussion about the Benefits and Drawbacks of Using Mocking

The use of mocking during our lab work offered several benefits, including:

- Facilitating isolated testing: Mock objects allowed us to test individual components in isolation, enabling focused testing of specific methods without relying on the entire system.
- Enhancing test control: By simulating the behavior of complex real objects, mocking provided greater control over test scenarios, allowing us to replicate various edge cases and error conditions.
- Enabling early testing: Mocking enabled us to test components even before the complete system was available, facilitating early detection of defects and integration issues.

However, there were also drawbacks associated with mocking, such as:

- Overriding class logic: Mocking can override the actual logic of a class, potentially masking defects or inaccuracies in the implementation.
- Limited realism: Mock objects may not accurately represent the behavior of real objects, leading to discrepancies between test results and actual system behavior.
- Increased complexity: Creating and managing mock objects can introduce additional complexity to the testing process, requiring careful design and maintenance of test cases.

Despite these drawbacks, the benefits of mocking outweighed the challenges in our testing process, allowing us to conduct thorough and efficient unit testing of our software components.

# 7 Comments/feedback on the lab itself

Initially, we encountered challenges in understanding the lab instructions solely from the provided document. The content was complex, and some aspects were unclear, prompting us to seek additional resources for clarification. Turning to supplementary materials outside the lab document proved beneficial, as they provided insights and explanations that facilitated our understanding of the concepts and tasks at hand.

With the aid of these additional resources, we were able to overcome the initial difficulties and gain a clearer comprehension of the requirements. As a result, the tasks became more manageable, and we felt more confident in approaching the lab exercises. This experience underscored the importance of leveraging diverse sources of information to enhance learning and problem-solving processes, especially when faced with challenging or ambiguous instructions.
