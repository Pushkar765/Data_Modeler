1.  Schema: This project uses a Star Schema. Sales_Fact is the main
    table, and all dimension tables (Customer, Product, Region, Date)
    are connected to it.

2.  Relationships: All relationships are Many-to-One (*:1). Sales_Fact
    connects to all dimensions. Returns_Fact connects to Sales_Fact and
    also to Date_Dim.

3.  Cardinality: Fact tables have many records, and dimension tables
    have unique values. So, *:1 relationships are used.

4.  Cross Filter Direction: Single direction is used for all
    relationships to keep the model simple and avoid errors.

5.  Inactive Relationship: The relationship between Returns_Fact and
    Date_Dim is inactive. It is used in DAX with USERELATIONSHIP.

6.  Data Cleaning: Data was cleaned by removing blanks, fixing data
    types, removing duplicates, and handling null values.

7.  Hierarchies: Hierarchies were created for Date (Year → Month →
    Date), Product (Category → Subcategory → Product), and Region.

8.  Issues & Solution: Ambiguity issue was solved by keeping only one
    active relationship and making others inactive.

9.  Conclusion: The model is clean, efficient, and ready for reporting.
    All visuals, filters, and calculations are working correctly.
