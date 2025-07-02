---
sidebar_position: 8
---

# 8. Comming soon...

First table, session and report in **INFOR LN**.

### Table

First we are going to create table, based od this scheme.

![Items Table](./img-lesson1/table-items.png)

#### 1. Right click activity → New → Infor LN Component.

![STEP 1](./img-lesson1/step-001.png)

#### 2. Choose component type "Table" and click next.

![STEP 2](./img-lesson1/step-002.png)

#### 3. Enter table name and descrption as "Items" then click Finish.

:::info

We using package tx and module zpl (polish extension) which is reserved for us. You can use whatever module and code you need.
Table number should be beetween 000-999. In our case we pick 400 so it makes "txzpl400".

:::


![STEP 3](./img-lesson1/step-003.png)

## Table Fields
### Domains

:::note

Domain is defined datatype. It is applicable to fields and variables.

:::

#### 4. Add table field

![STEP 4](./img-lesson1/step-004.png)

#### 5. It will ask if you want to check-out component. Click yes.

:::info

If you want to modify component within activity you need to check-out component first.
Check-in if you finish your modifications.

:::

![STEP 5](./img-lesson1/step-005.png)

#### 6. Now click Add once more. We need to enter fields Name, Label and Domain.

### Labels

:::note

Label is language based component. Example: label tcibd.item appears in english as 'Item' and in polish as 'Pozycja'.

:::
:::tip

You can you first 4 letters of table field name as field name ID → .iden or make it smoother like Order Number → .orno , 
it will be more natural as you start working with LN.

:::

![STEP 6](./img-lesson1/step-006.png)

#### 7. Click Browse...


![STEP 7](./img-lesson1/step-007.png)

#### 8. Now click New.

:::info

Labels are codes that are used instead of language-dependent text in
forms, reports, domains, and menus. We want

:::
![STEP 8](./img-lesson1/step-008.png)

#### 9. Fill Name and Description.

:::tip

Best practice is naming label as table fields which they are aplied to.

:::
![STEP 9](./img-lesson1/step-009.png)

#### 10. It will ask you if you want to create new label with same description.

:::warning

Best practice is use already defined labels to not making tons of same 'ID's and other common used labels. However for this tutorial we are going to create them to show process.

:::
![STEP 10](./img-lesson1/step-010.png)

#### 11. Click Browse...

![STEP 11](./img-lesson1/step-011.png)

#### 12. Now click New.

![STEP 12](./img-lesson1/step-012.png)

#### 13. Now enter data based on table diagram.

![STEP 13](./img-lesson1/step-013.png)

#### 14. Here is how we create enumerated field.

![STEP 14](./img-lesson1/step-014.png)

#### 15. We go to our domain (1) then on 'Enum - Set Data' (2). Let's set our Step size = 1 (3) and Add (4).
:::info

Step size is constant step for enum. It's usually 10 for LN enums.

:::
![STEP 15](./img-lesson1/step-015.png)

#### 16. Enter rest of enum data.

![STEP 16](./img-lesson1/step-016.png)

#### 17. Set default value for enum field in table.

![STEP 17](./img-lesson1/step-017.png)

#### 18. Finish table, set 'Creation Date' domain as date and 'Last Modification Date' domain as UTC/TIME.

![STEP 18](./img-lesson1/step-018.png)

#### 19. Check in our changes.
:::info

Every component we modify we first check-out, then we modify it and last we check-in it.
Check-in and Check-out allows only one user to modify object, so developers don't colide.

:::
![STEP 19](./img-lesson1/step-019.png)

#### 20. Now Enter commit message.

![STEP 20](./img-lesson1/step-020.png)

### Indices
:::info

Index allows us to retrive table faster and guarantee record uniqueness. Table requires at least one index.

:::
#### 21. We overlook creating index for table. Go to 'Indices' tab (1) and add index as on screen.

![STEP 21](./img-lesson1/step-021.png)

#### 22. Now 'Active' and 'Unique' checkbox are marked.

![STEP 22](./img-lesson1/step-022.png)

#### 23. We need to check-in our changes once again.

![STEP 23](./img-lesson1/step-023.png)

#### 24. Now we right click on activity to end it.

![STEP 24](./img-lesson1/step-024.png)

#### 25. Make sure checkbox 'Close activity' is unmarked and click 'OK'.
:::warning

If you close actvity you need to create new one.

:::
![STEP 25](./img-lesson1/step-025.png)

#### 26. Here are displayed errors for ending activity.

![STEP 26](./img-lesson1/step-026.png)
### Admin mode

#### 27. To create table we need to turn on admin mode. Go to LN and run session 'ttmtm3501m000'. Turn admin mode on and set maintenance mode. It will take a while.
:::danger

Turning on active mode logout all non superusers, stops all jobs that are running on normal user. Make sure you can turn it on and turn it off when You finish.

:::
![STEP 27](./img-lesson1/step-027.png)

#### 28. Now go to session ttadv5215m000 and convert. Specify options as on screen. We usually want to convert all in case other developers forget to convert their work.

![STEP 28](./img-lesson1/step-028.png)
#### 29. Now go to session ttadv1243m000 and compile. Specify options as on screen. We usually want to compile all in case other developers forget to convert their work.

![STEP 29](./img-lesson1/step-029.png)
#### 30. You can also convert and create from LN Studio.

![STEP 30](./img-lesson1/step-030.png)
#### 31. Convert.

![STEP 31](./img-lesson1/step-031.png)
#### 32. Now create table. In example we use company 2100.

![STEP 32](./img-lesson1/step-032.png)
#### 33. Create tables session in LN is 'ttaad4230m000'.

![STEP 33](./img-lesson1/step-033.png)
#### 34. Remember to turn off admin mode.

![STEP 34](./img-lesson1/step-034.png)

#### 35. You can look at new created table in session ttaad4100.

![STEP 35](./img-lesson1/step-035.png)

## TO DO 

Create Tables based on schemes.
Role enum should have 'Buyer' and 'Seller'.

![TO DO Tables](./img-lesson1/tables-to-do.png)