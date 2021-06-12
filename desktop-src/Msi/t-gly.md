---
description: En savoir plus sur les concepts de Windows Installer qui commencent par la lettre T, tels que le traitement et la transformation des transactions.
ms.assetid: 06fd0284-5af9-409a-8748-c0b40e0fa317
title: T (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9489455f880ba558e5a9f8584be19718823035
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011262"
---
# <a name="t-windows-installer"></a>T (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**traitement des transactions**
</dt> <dd>

Une ou plusieurs opérations ont été traitées ensemble comme un unique indivisible entier appelé transaction. Toutes les opérations constitutives doivent être exécutées pour que la transaction aboutisse, dans le cas contraire, toutes les opérations sont restaurées à leur état d’origine.

</dd> <dt>

<span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**Modifiez**
</dt> <dd>

Modèle des différences entre deux [*bases de données de programme d’installation*](i-gly.md) qui peuvent être appliquées pour produire des modifications similaires dans d’autres bases de données. Par exemple, une transformation de localisation peut être utilisée pour modifier la langue d’une application. Pour plus d’informations, consultez [fusions et transformations](merges-and-transforms.md).

</dd> <dt>

<span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**indicateurs de condition d’erreur de transformation**
</dt> <dd>

Jeu de propriétés utilisé pour signaler les conditions d’erreur d’une [*transformation*](/windows). Pour plus d’informations, consultez [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).

</dd> <dt>

<span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**indicateurs de validation de transformation**
</dt> <dd>

Jeu de propriétés utilisé pour vérifier que la [*transformation*](/windows) peut être appliquée à la base de données. Pour obtenir la liste de ces propriétés, consultez [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).

</dd> </dl>

 

 
