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
# <a name="t-windows-installer"></a><span data-ttu-id="3f74a-103">T (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="3f74a-103">T (Windows Installer)</span></span>

<span data-ttu-id="3f74a-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="3f74a-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="3f74a-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**traitement des transactions**</span><span class="sxs-lookup"><span data-stu-id="3f74a-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**transaction processing**</span></span>
</dt> <dd>

<span data-ttu-id="3f74a-106">Une ou plusieurs opérations ont été traitées ensemble comme un unique indivisible entier appelé transaction.</span><span class="sxs-lookup"><span data-stu-id="3f74a-106">One or more operations processed together as a single indivisible whole called a transaction.</span></span> <span data-ttu-id="3f74a-107">Toutes les opérations constitutives doivent être exécutées pour que la transaction aboutisse, dans le cas contraire, toutes les opérations sont restaurées à leur état d’origine.</span><span class="sxs-lookup"><span data-stu-id="3f74a-107">All the constituent operations must succeed for the transaction to succeed, otherwise all the operations are rolled back to the original state.</span></span>

</dd> <dt>

<span data-ttu-id="3f74a-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**Modifiez**</span><span class="sxs-lookup"><span data-stu-id="3f74a-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="3f74a-109">Modèle des différences entre deux [*bases de données de programme d’installation*](i-gly.md) qui peuvent être appliquées pour produire des modifications similaires dans d’autres bases de données.</span><span class="sxs-lookup"><span data-stu-id="3f74a-109">Template of the differences between two [*installer databases*](i-gly.md) that can be applied to produce similar changes in other databases.</span></span> <span data-ttu-id="3f74a-110">Par exemple, une transformation de localisation peut être utilisée pour modifier la langue d’une application.</span><span class="sxs-lookup"><span data-stu-id="3f74a-110">For example, a localization transform can be used to change the language of an application.</span></span> <span data-ttu-id="3f74a-111">Pour plus d’informations, consultez [fusions et transformations](merges-and-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="3f74a-111">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f74a-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**indicateurs de condition d’erreur de transformation**</span><span class="sxs-lookup"><span data-stu-id="3f74a-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**transform error condition flags**</span></span>
</dt> <dd>

<span data-ttu-id="3f74a-113">Jeu de propriétés utilisé pour signaler les conditions d’erreur d’une [*transformation*](/windows).</span><span class="sxs-lookup"><span data-stu-id="3f74a-113">Set of properties used to flag the error conditions of a [*transform*](/windows).</span></span> <span data-ttu-id="3f74a-114">Pour plus d’informations, consultez [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="3f74a-114">For more information, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> <dt>

<span data-ttu-id="3f74a-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**indicateurs de validation de transformation**</span><span class="sxs-lookup"><span data-stu-id="3f74a-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**transform validation flags**</span></span>
</dt> <dd>

<span data-ttu-id="3f74a-116">Jeu de propriétés utilisé pour vérifier que la [*transformation*](/windows) peut être appliquée à la base de données.</span><span class="sxs-lookup"><span data-stu-id="3f74a-116">Set of properties used to verify that the [*transform*](/windows) can be applied to the database.</span></span> <span data-ttu-id="3f74a-117">Pour obtenir la liste de ces propriétés, consultez [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="3f74a-117">For a list of these properties, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> </dl>

 

 
