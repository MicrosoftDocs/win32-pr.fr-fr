---
title: Rechercher des objets par classe
description: Requête de recherche classique pour une classe d’objet spécifique.
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- Recherche d’objets par classe AD
- Active Directory, utiliser, Rechercher, par classe
- objet AD, recherche par classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172c8b150090fae83aee1cf3e0f6a63a0e21dec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512637"
---
# <a name="finding-objects-by-class"></a>Rechercher des objets par classe

Requête de recherche classique pour une classe d’objet spécifique. L’exemple de code suivant recherche des ordinateurs avec l’emplacement dans Building 7N.


```C++
(&(objectCategory=computer)(location=Building 7N))
```



Pensez à la raison pour laquelle **objectClass** n’est pas utilisé. N’utilisez pas **objectClass** sans une autre comparaison qui contient un attribut indexé. Les attributs d’index peuvent accroître l’efficacité d’une requête. L’attribut **objectClass** est à valeurs multiples et n’est pas indexé. Pour spécifier le type ou la classe d’un objet, utilisez **objectCategory**.

Moins efficace :


```C++
(objectClass=computer)
```



Plus efficace :


```C++
(objectCategory=computer)
```



Sachez qu’il existe des situations où une combinaison de **objectClass** et **objectCategory** doit être utilisée. La classe utilisateur et la classe contact doivent être spécifiées comme suit.


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



N’oubliez pas que vous pouvez rechercher les utilisateurs et les contacts avec les éléments suivants.


```C++
(objectCategory=person)
```



 

 




