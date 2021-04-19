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
# <a name="ice73"></a>ICE73

ICE73 vérifie que votre package ne réutilise pas les codes de package, les codes de mise à niveau ou les codes de produit des exemples du kit de développement logiciel (SDK) Windows Installer. Les packages ne doivent jamais réutiliser le package, la mise à niveau ou les codes de produit d’un autre produit.

## <a name="result"></a>Résultats

ICE73 génère un avertissement si le package de votre produit réutilise un package ou un code de produit d’un Windows Installer exemple du kit de développement logiciel (SDK).

## <a name="example"></a>Exemple

ICE73 signale les erreurs suivantes pour l’exemple illustré :

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> Les astérisques ( \* \* \* \* ) du GUID représentent la plage de GUID réservée aux packages Windows Installer SDK suivants.

 

Pour corriger les erreurs, générez un nouveau GUID unique pour les codes du produit et du package de votre package. Vous aurez également besoin d’un nouveau GUID unique pour le code de mise à niveau de votre package.

[Flux d’informations de synthèse](summary-information-stream.md) (partiel)



| Propriété       | Valeur                                  |
|----------------|----------------------------------------|
| PID \_ REVNUMBER | {000C1101-0000-0000-C000-000000000047} |



 

[Table de propriétés](property-table.md) (partielle)



| Propriété                           | Valeur                                  |
|------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md) | {80F7E030-A751-11D2-A7D4-006097C99860} |
| [**UpgradeCode**](upgradecode.md) | {8FC70000-88A0-4b41-82B8-8905D4AA904C} |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codes de package](package-codes.md)
</dt> <dt>

[Codes de produit](product-codes.md)
</dt> <dt>

[**Propriété Résumé du numéro de révision**](revision-number-summary.md)
</dt> <dt>

[**UpgradeCode, propriété**](upgradecode.md)
</dt> <dt>

[**Propriété ProductCode**](productcode.md)
</dt> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



