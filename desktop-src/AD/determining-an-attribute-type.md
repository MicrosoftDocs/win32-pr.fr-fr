---
title: Détermination d’un type d’attribut
description: L’attribut systemFlags d’un objet attributeSchema contient un ensemble d’indicateurs qui indiquent différentes qualités de l’objet attribut, par exemple si l’attribut est construit ou non répliqué.
ms.assetid: 58f44ea4-ecbd-4650-b366-37b05a975c68
ms.tgt_platform: multiple
keywords:
- Détermination d’une publicité de type d’attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64b4d8b0ae5d6cbac38c9c44ed8e4a7aa5d5f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031018"
---
# <a name="determining-an-attribute-type"></a>Détermination d’un type d’attribut

L’attribut [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) d’un objet [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) contient un ensemble d’indicateurs qui indiquent différentes qualités de l’objet attribut, par exemple si l’attribut est construit ou non répliqué. Le tableau suivant répertorie les indicateurs de l’attribut **systemFlags** qui affectent le type de stockage de l’attribut. 

| Valeur d’indicateur | Description                                                                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------|
| 0x00000001 | Si cet indicateur est présent dans l’attribut [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , l’attribut n’est pas répliqué. |
| 0x00000004 | Si cet indicateur est présent dans l’attribut [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , l’attribut est construit.    |



 

Il est possible de construire une chaîne de requête qui peut être utilisée pour interroger des attributs construits ou non répliqués. Par exemple, la chaîne de requête suivante recherche tous les objets [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) non répliqués. Sachez que la chaîne de requête requiert l’équivalent décimal de la valeur, et non l’équivalent hexadécimal de la valeur. Pour plus d’informations sur l’OID de règle de correspondance utilisé par cette chaîne de requête, consultez [comment spécifier des valeurs de comparaison](how-to-specify-comparison-values.md).


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=1))
```



L’attribut [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) de l’objet [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de chaque attribut définit si un attribut est indexé ; un attribut indexé a la valeur 1, un attribut non indexé a la valeur 0. Par exemple, la chaîne de requête suivante recherche les objets **attributeSchema** représentant les attributs indexés.


```C++
(&(objectCategory=attributeSchema)(searchFlags=1))
```



L’attribut [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) de l’objet [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de chaque attribut définit si un attribut est répliqué dans le catalogue global. Cet attribut a la valeur **true** si l’attribut est membre du catalogue global ou **false** si les attributs ne se trouvent pas dans le catalogue global. Par exemple, la chaîne de requête suivante recherche les objets **attributeSchema** répliqués dans le catalogue global.


```C++
(&(objectCategory=attributeSchema)(isMemberOfPartialAttributeSet=TRUE))
```



 

 