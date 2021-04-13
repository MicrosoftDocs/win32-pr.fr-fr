---
title: Interrogation des objets de schéma de catégorie 1 ou 2
description: L’attribut systemFlags des objets attributeSchema et classSchema est un masque de passe entier qui contient des indicateurs qui indiquent des qualités système supplémentaires de l’attribut ou de la classe.
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- Interrogation des objets de schéma de catégorie 1 ou 2 AD
- objet AD, interrogation des objets de schéma de catégorie 1 ou 2
- Active Directory de schéma, interrogation des objets de schéma de catégorie 1 ou 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c67b57821cbebc80b3b6e93d158bbb8af8f7103
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314621"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a>Interrogation des objets de schéma de catégorie 1 ou 2

L’attribut **systemFlags** des objets **attributeSchema** et **classSchema** est un masque de passe entier qui contient des indicateurs qui indiquent des qualités système supplémentaires de l’attribut ou de la classe. L’énumération d’énumérations [**\_ systemFlags \_ ADS**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) contient des valeurs qui correspondent aux bits que vous pouvez définir dans l’attribut **systemFlags** . Vous ne pouvez pas définir d’autres bits de **systemFlags** , tels que le bit 0x10, qui indique si l’attribut ou la classe est une catégorie 1 ou 2. Le bit 0x10 est défini pour les objets catégorie 1, qui sont les classes et les attributs inclus dans le schéma de base inclus dans le système. Le bit n’est pas défini pour les classes et les attributs de catégorie 2, qui sont des extensions du schéma. Si aucune propriété **systemFlags** n’existe sur un objet **attributeSchema** ou **classSchema** , il s’agit de la catégorie 2.

Le **\_ bit de règle de correspondance LDAP \_ \_ \_ et** la règle de correspondance peuvent être utilisés pour rechercher des objets dont l’indicateur 0X10 est défini dans l’attribut **systemFlags** . Pour plus d’informations, consultez [syntaxe de filtre de recherche](/windows/desktop/ADSI/search-filter-syntax).

## <a name="querying-for-category-1"></a>Interrogation de la catégorie 1

La chaîne de requête suivante recherche les attributs de catégorie 1 (objets **attributeSchema** avec le bit 0x10 défini dans la propriété **systemFlags** ).


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



Sachez que, dans l’exemple ci-dessus, la syntaxe de requête LDAP requiert des valeurs décimales ; par conséquent, la valeur hexadécimale de l’indicateur doit être convertie en valeur décimale. Dans ce cas, la catégorie 1 bit est 0x10, de sorte que la valeur du filtre doit être spécifiée en tant que 16.

## <a name="querying-for-category-2"></a>Interrogation de la catégorie 2

La chaîne de requête suivante recherche les attributs de catégorie 2 (objets **attributeSchema** pour lesquels le bit 0x10 n’est pas défini dans la propriété **systemFlags** ).


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



Sachez que cette requête retourne également des objets **attributeSchema** qui n’ont pas de propriété **systemFlags** et, par conséquent, n’ont pas l’indicateur spécifié défini.

 

 