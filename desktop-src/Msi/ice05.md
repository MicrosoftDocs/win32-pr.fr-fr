---
description: 'ICE05 vérifie que certaines tables contiennent des entrées requises. Cela comprend, mais n’est pas limité à, la vérification de la table de propriétés pour les propriétés requises : ProductName, ProductLanguage, ProductVersion, ProductCode et manufacturer.'
ms.assetid: 90b35758-c9d9-4104-a352-f0b17b04b571
title: ICE05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9710a81eca3da7ac947afb90a1d6788c0ddd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536485"
---
# <a name="ice05"></a>ICE05

ICE05 vérifie que certaines tables contiennent des entrées requises. Cela comprend, mais n’est pas limité à, la vérification de la [table de propriétés](property-table.md) pour les propriétés requises : [**ProductName**](productname.md), [**ProductLanguage**](productlanguage.md), [**ProductVersion**](productversion.md), [**ProductCode**](productcode.md)et [**Manufacturer**](manufacturer.md).

## <a name="result"></a>Résultats

ICE05 publie une erreur si une entrée obligatoire est manquante.

## <a name="example"></a>Exemple

Pour l’exemple illustré, ICE05 signale que l’entrée « ProductVersion » est requise dans la table « propriété ».

[Table de propriétés](property-table.md) (partielle)



| Propriété                           | Valeur     |
|------------------------------------|-----------|
| [**ProductName**](productname.md) | MyProduct |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



