# Technical language definitions
In the document you'll find the definitions of acronyms technical language and word definitions. 

## Definitions:
#### BOM (Bill of materials)
A complete list of all parts, materials and quantities required to build a product

#### EBOM (Engineering Bill of Materials)
The BOM created by engineering that defines a product's design and components from a technical perspective.

#### MBOM (Manufacturing Bill of Materials)
The BOM used in production, showing how the product will be manufactured and assembled

#### MPN (Manufacturer Part Number)
A unique identifier assigned by a manufacturer to a specific component or product

#### SKU (Stock Keeping Unit)
A company-defined identifier used to track and manage inventory

#### BOM Hierarchy
The parent-child structure showing how assemblies, subassemblies, and components relate within a BOM

#### MOQ (Minimum Order Quantity)
The smallest quantity of a product or component that a supplier is willing to sell

#### RFQ (Request for Quotation)
A formal request sent to suppliers asking for pricing and commercial terms for specified items

#### Lead Time
The total time required from placing an order until the product or component is delivered

#### Capacity 
The maximum quantity of a products a supplier or factory can produce within a given time period

#### Landed Cost
The total cost of obtaining a product, including purchase price, shipping, duties, taxes and handling fees

## Relationship Model

```mermaid
    flowchart TD
        EBOM[EBOM]
        BOM[BOM]
        RFQ[RFQ]
        SUPPLIER[MOQ, Lead Time, 
        Capacity, Unit Price]
        LANDEDCOST[Landed Cost]
        APPROVED[Approved Supplier Selection]
        PURCHASE[Purchase using MPNs and SKUs]

        EBOM --> BOM 
        BOM --> RFQ
        RFQ --> SUPPLIER
        SUPPLIER --> LANDEDCOST
        LANDEDCOST --> APPROVED
        APPROVED --> PURCHASE


