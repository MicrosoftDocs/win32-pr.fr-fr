---
description: En savoir plus sur l’argument de sous-requête dans le shell Windows. Une sous-requête est un fichier de recherche enregistré que vous pouvez utiliser comme filtre pour une nouvelle requête.
title: Argument de sous-requête (shell Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ef0b37c0f473f2b86c85c18a99124be3b366f447
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010662"
---
# <a name="subquery-argument-the-windows-shell"></a>Argument de sous-requête (shell Windows)

Une sous-requête est un fichier de recherche enregistré ( \* . search-ms) que vous pouvez utiliser comme filtre pour une nouvelle requête. Les résultats de la sous-requête sont utilisés comme source pour la nouvelle requête. Par exemple, imaginons que vous ayez plusieurs fichiers de recherche enregistrés qui limitent une requête par liste de distribution de courrier électronique : myDepartment. search-ms, TeamProject. search-ms et corporatewide. search-ms. L’utilisation de l' `subquery` argument vous permet de limiter les recherches par courrier électronique à tout ou partie de ces recherches enregistrées.

## <a name="example"></a>Exemple


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Informations sur les arguments



|                          |                                         |
|--------------------------|-----------------------------------------|
| Système d’exploitation minimal | Windows Vista Service Pack 1 (SP1) |



 

 

 



