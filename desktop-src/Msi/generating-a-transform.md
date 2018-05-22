---
Description: 'The following procedure describes a scenario to generate a transform that permanently hides a feature.'
ms.assetid: '43f36866-a9df-4035-a8ae-5ccbcb628a90'
title: Generating a Transform
---

# Generating a Transform

The following procedure describes a scenario to generate a transform that permanently hides a feature.

**To permanently hide a product feature**

1.  Copy the original installation package.
2.  Alter the copy by setting the value of the Display column in the [Feature table](feature-table.md) to zero. This specifies hiding the feature.
3.  Create a transform from the original installation package to the new installation packages by calling [**MsiDatabaseGenerateTransform**](msidatabasegeneratetransform.md).
4.  Create the summary information in the transform by calling [**MsiCreateTransformSummaryInfo**](msicreatetransformsummaryinfo.md).

The transform is then ready to be applied during installation. For more information, see [Applying Transforms](applying-transforms.md).

 

 


