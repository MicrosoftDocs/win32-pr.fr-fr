---
description: ICE73 vérifie que votre package ne réutilise pas les codes de package, les codes de mise à niveau ou les codes de produit des exemples du kit de développement logiciel (SDK) Windows Installer. Les packages ne doivent jamais réutiliser le package, la mise à niveau ou les codes de produit d’un autre produit.
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ac0e192f7c2ab7fb6f6236e45e0e4da70157e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517553"
---
# <a name="ice73"></a><span data-ttu-id="9d3a0-104">ICE73</span><span class="sxs-lookup"><span data-stu-id="9d3a0-104">ICE73</span></span>

<span data-ttu-id="9d3a0-105">ICE73 vérifie que votre package ne réutilise pas les codes de package, les codes de mise à niveau ou les codes de produit des exemples du kit de développement logiciel (SDK) Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9d3a0-105">ICE73 verifies that your package does not reuse package codes, upgrade codes, or product codes of the Windows Installer SDK samples.</span></span> <span data-ttu-id="9d3a0-106">Les packages ne doivent jamais réutiliser le package, la mise à niveau ou les codes de produit d’un autre produit.</span><span class="sxs-lookup"><span data-stu-id="9d3a0-106">Packages should never reuse the package, upgrade, or product codes of another product.</span></span>

## <a name="result"></a><span data-ttu-id="9d3a0-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="9d3a0-107">Result</span></span>

<span data-ttu-id="9d3a0-108">ICE73 génère un avertissement si le package de votre produit réutilise un package ou un code de produit d’un Windows Installer exemple du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="9d3a0-108">ICE73 outputs a warning if your product's package reuses a package or product code of a Windows Installer SDK sample.</span></span>

## <a name="example"></a><span data-ttu-id="9d3a0-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="9d3a0-109">Example</span></span>

<span data-ttu-id="9d3a0-110">ICE73 signale les erreurs suivantes pour l’exemple illustré :</span><span class="sxs-lookup"><span data-stu-id="9d3a0-110">ICE73 reports the following errors for the example shown:</span></span>

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> <span data-ttu-id="9d3a0-111">Les astérisques ( \* \* \* \* ) du GUID représentent la plage de GUID réservée aux packages Windows Installer SDK suivants.</span><span class="sxs-lookup"><span data-stu-id="9d3a0-111">The asterisks (\*\*\*\*) in the GUID represent the range of GUIDs reserved for subsequent Windows Installer SDK packages.</span></span>

 

<span data-ttu-id="9d3a0-112">Pour corriger les erreurs, générez un nouveau GUID unique pour les codes du produit et du package de votre package.</span><span class="sxs-lookup"><span data-stu-id="9d3a0-112">To fix the errors, generate a new unique GUID for your package's product and package codes.</span></span> <span data-ttu-id="9d3a0-113">Vous aurez également besoin d’un nouveau GUID unique pour le code de mise à niveau de votre package.</span><span class="sxs-lookup"><span data-stu-id="9d3a0-113">You will also need a new unique GUID for your package's upgrade code.</span></span>

<span data-ttu-id="9d3a0-114">[Flux d’informations de synthèse](summary-information-stream.md) (partiel)</span><span class="sxs-lookup"><span data-stu-id="9d3a0-114">[Summary Information Stream](summary-information-stream.md) (partial)</span></span>



| <span data-ttu-id="9d3a0-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="9d3a0-115">Property</span></span>       | <span data-ttu-id="9d3a0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d3a0-116">Value</span></span>                                  |
|----------------|----------------------------------------|
| <span data-ttu-id="9d3a0-117">PID \_ REVNUMBER</span><span class="sxs-lookup"><span data-stu-id="9d3a0-117">PID\_REVNUMBER</span></span> | <span data-ttu-id="9d3a0-118">{000C1101-0000-0000-C000-000000000047}</span><span class="sxs-lookup"><span data-stu-id="9d3a0-118">{000C1101-0000-0000-C000-000000000047}</span></span> |



 

<span data-ttu-id="9d3a0-119">[Table de propriétés](property-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="9d3a0-119">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="9d3a0-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="9d3a0-120">Property</span></span>                           | <span data-ttu-id="9d3a0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d3a0-121">Value</span></span>                                  |
|------------------------------------|----------------------------------------|
| [<span data-ttu-id="9d3a0-122">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="9d3a0-122">**ProductCode**</span></span>](productcode.md) | <span data-ttu-id="9d3a0-123">{80F7E030-A751-11D2-A7D4-006097C99860}</span><span class="sxs-lookup"><span data-stu-id="9d3a0-123">{80F7E030-A751-11D2-A7D4-006097C99860}</span></span> |
| [<span data-ttu-id="9d3a0-124">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="9d3a0-124">**UpgradeCode**</span></span>](upgradecode.md) | <span data-ttu-id="9d3a0-125">{8FC70000-88A0-4b41-82B8-8905D4AA904C}</span><span class="sxs-lookup"><span data-stu-id="9d3a0-125">{8FC70000-88A0-4b41-82B8-8905D4AA904C}</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9d3a0-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9d3a0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d3a0-127">Codes de package</span><span class="sxs-lookup"><span data-stu-id="9d3a0-127">Package Codes</span></span>](package-codes.md)
</dt> <dt>

[<span data-ttu-id="9d3a0-128">Codes de produit</span><span class="sxs-lookup"><span data-stu-id="9d3a0-128">Product Codes</span></span>](product-codes.md)
</dt> <dt>

[<span data-ttu-id="9d3a0-129">**Propriété Résumé du numéro de révision**</span><span class="sxs-lookup"><span data-stu-id="9d3a0-129">**Revision Number Summary Property**</span></span>](revision-number-summary.md)
</dt> <dt>

[<span data-ttu-id="9d3a0-130">**UpgradeCode, propriété**</span><span class="sxs-lookup"><span data-stu-id="9d3a0-130">**UpgradeCode Property**</span></span>](upgradecode.md)
</dt> <dt>

[<span data-ttu-id="9d3a0-131">**Propriété ProductCode**</span><span class="sxs-lookup"><span data-stu-id="9d3a0-131">**ProductCode Property**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="9d3a0-132">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="9d3a0-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



