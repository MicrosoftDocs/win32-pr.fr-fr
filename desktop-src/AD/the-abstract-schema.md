---
title: Schéma abstrait
description: Le conteneur de schéma contient tous les objets classSchema et attributeSchema qui définissent les classes et les attributs qui peuvent exister dans une forêt de répertoires.
ms.assetid: 688fccf7-37ce-4eea-b4ff-b0b3223a964e
ms.tgt_platform: multiple
keywords:
- AD du schéma abstrait
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b46e4fefd52e786829e051a14714d2fec118b2ad42cdd95afcaa78b098b0f04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182780"
---
# <a name="the-abstract-schema"></a>Schéma abstrait

Le conteneur de schéma contient tous les objets **classSchema** et **attributeSchema** qui définissent les classes et les attributs qui peuvent exister dans une forêt de répertoires. Le conteneur de schéma contient également un objet nommé Aggregate of Class **Subscheme**. Cet objet de sous- **schéma** est appelé schéma abstrait.

Le schéma abstrait contient un sous-ensemble des données stockées dans les objets **classSchema** et **attributeSchema** . Son objectif est de fournir un mécanisme simple et efficace pour récupérer les éléments fréquemment utilisés des définitions de classe et d’attribut. Par exemple, pour récupérer les attributs facultatifs et obligatoires d’une classe d’objet, établissez une liaison à plusieurs objets pour collecter les valeurs **mayContain**, **mustContain**, **systemMayContain** et **systemMustContain** à partir de la classe et de toutes ses superclasses, ainsi que de toutes les classes auxiliaires de la classe et de ses superclasses. Le schéma abstrait recueille facilement toutes ces données dans un seul objet.

Comme pour tout objet dans Active Directory Domain Services, vous pouvez lier l’objet de sous- **schéma** et lire ses attributs, en analysant les valeurs de chaîne pour récupérer les données souhaitées. Toutefois, ADSI fournit un ensemble d’interfaces qui facilitent grandement la lecture du schéma abstrait. Pour plus d’informations, consultez [lecture du schéma abstrait](reading-the-abstract-schema.md).

Le tableau suivant répertorie les attributs clés d’un objet de sous- **schéma** .



| Attribut                 | Description                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **attributeTypes**        | Attribut à valeurs multiples qui contient des chaînes représentant chaque attribut du schéma. Chaque valeur contient **AttributeID**, **lDAPDisplayName**, **attributeSyntax**, **rangeLower**, **rangeUpper** et un élément qui indique si l’attribut peut avoir plusieurs valeurs. |
| **extendedAttributeInfo** | Attribut à valeurs multiples qui contient des chaînes représentant des données supplémentaires pour chaque attribut. Chaque valeur contient **AttributeID**, **lDAPDisplayName**, **schemaIDGUID** et **attributeSecurityGUID**.                                                                          |
| **extendedClassInfo**     | Attribut à valeurs multiples qui contient des chaînes représentant des données supplémentaires pour chaque classe. Chaque valeur contient les valeurs **governsID**, **lDAPDisplayName** et **schemaIDGUID** de la classe.                                                                                              |
| **objectClasses**         | Attribut à valeurs multiples qui contient des chaînes représentant chaque classe dans le schéma. Chaque valeur contient les valeurs **governsID**, **lDAPDisplayName**, **mustContain**, **mayContain**, etc.                                                                                           |



 

 

 




