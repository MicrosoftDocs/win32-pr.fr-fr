---
description: 'ICE05 vérifie que certaines tables contiennent des entrées requises. Cela comprend, mais n’est pas limité à, la vérification de la table de propriétés pour les propriétés requises : ProductName, ProductLanguage, ProductVersion, ProductCode et manufacturer.'
ms.assetid: 90b35758-c9d9-4104-a352-f0b17b04b571
title: ICE05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94766ed0a311243b47c2214ea21de89576d533f0d1fa76f776dedfa3afdc7da0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142557"
---
# <a name="ice05"></a>ICE05

ICE05 vérifie que certaines tables contiennent des entrées requises. Cela comprend, mais n’est pas limité à, la vérification de la [table de propriétés](property-table.md) pour les propriétés requises : [**ProductName**](productname.md), [**ProductLanguage**](productlanguage.md), [**ProductVersion**](productversion.md), [**ProductCode**](productcode.md)et [**Manufacturer**](manufacturer.md).

## <a name="result"></a>Résultat

ICE05 publie une erreur si une entrée obligatoire est manquante.

## <a name="example"></a>Exemples

Pour l’exemple illustré, ICE05 signale que l’entrée « ProductVersion » est requise dans la table « propriété ».

[Table de propriétés](property-table.md) (partielle)



| Propriété                           | Valeur     |
|------------------------------------|-----------|
| [**ProductName**](productname.md) | MyProduct |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



