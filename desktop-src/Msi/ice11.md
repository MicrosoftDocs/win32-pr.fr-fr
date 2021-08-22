---
description: Le ICE11 est utilisé avec les installations simultanées. Les installations simultanées ne sont pas recommandées pour l’installation d’applications destinées à être communiquées au public. Pour plus d’informations sur les installations simultanées, consultez installations simultanées.
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed6e578cd6f7da09cc1894bc154ba77225f1efaafedf45f3fb7cdd3f30190e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119296489"
---
# <a name="ice11"></a>ICE11

Le ICE11 est utilisé avec les installations simultanées. Les installations simultanées ne sont pas recommandées pour l’installation d’applications destinées à être communiquées au public. Pour plus d’informations sur les installations simultanées, consultez [installations simultanées](concurrent-installations.md).

## <a name="result"></a>Résultat

ICE11 valide la colonne source de la [table CustomAction](customaction-table.md) des actions personnalisées d’installation simultanée. La colonne source doit contenir un [GUID](guid.md) valide (code de produit msi).

ICE11 publie une erreur si la colonne source de la table CustomAction est créée de manière incorrecte pour les actions personnalisées d’installation simultanée.

## <a name="example"></a>Exemples

ICE publie les messages d’erreur suivants pour l’exemple indiqué.

``` syntax
CustomAction: CA4 is a nested install of an advertised MSI.  The 'Source' must contain a valid MSI product code.  Current: ProductCode.
CustomAction: CA1 is a nested install of an advertised MSI.  It duplicates the ProductCode of the base MSI package.  Current: {BFB69273-F0AE-45C4-9853-0AF946714768}.
CustomAction: CA2 is a nested install of an advertised MSI.  The GUID must be all upper-case.  Current: {BFB69273-F0AE-55c5-9853-0AF946714768}.
```

[Table de propriétés](property-table.md) (partielle)



| Propriété        | Valeur                                  |
|-----------------|----------------------------------------|
| **ProductCode** | {BFB69273-F0AE-45C4-9853-0AF946714768} |



 

[Table CustomAction](customaction-table.md) (partielle)



| CustomAction | Type | Source                                 |
|--------------|------|----------------------------------------|
| AC1          | 39   | {BFB69273-F0AE-45C4-9853-0AF946714768} |
| CA2          | 39   | {BFB69273-F0AE-55c5-9853-0AF946714768} |
| CA3          | 39   | {BFB69273-F0AE-66C6-9853-0AF946714768} |
| CA4          | 39   | ProductCode                            |



 

Pour résoudre les erreurs, pour CA1, vous ne pouvez pas effectuer une installation simultanée du « package de base ». Cela entraînerait une installation récursive. Cette entrée doit être supprimée ou la colonne source doit être remplacée par un GUID pour un MSI publié qui diffère du GUID du package de base. Pour CA2, mettez tous les caractères du GUID en majuscules. Enfin, modifiez la colonne source CA4's pour référencer un GUID valide d’un MSI publié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Installations simultanées](concurrent-installations.md)
</dt> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



