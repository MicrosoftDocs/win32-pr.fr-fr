---
title: Énumération
description: L’accès aux données et leur manipulation avec ADSI offrent plusieurs exemples d’énumération. Vous pouvez également énumérer les enfants des objets Container. Ces enfants sont eux-mêmes des objets, et non simplement des propriétés sur les objets.
ms.assetid: 1db19b00-8e43-4fc0-9099-1a1135219600
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, exemple de code Visual Basic, utilisation de IADsContainer pour énumérer des objets
- conteneurs ADSI, à l’aide de IADsContainer pour énumérer les enfants d’un conteneur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ba90e86282939486b79ee09cd17352841e733e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939596"
---
# <a name="enumeration"></a>Énumération

[L’accès aux données et leur manipulation avec ADSI](accessing-and-manipulating-data-with-adsi.md) offrent plusieurs exemples d’énumération. Vous pouvez également énumérer les enfants des objets Container. Ces enfants sont eux-mêmes des objets, et non simplement des propriétés sur les objets.

L’exemple suivant utilise l’interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) pour énumérer les enfants du conteneur.


```VB
Dim Container as IADsContainer
Dim Child as IADs

Set Container = GetObject("LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com")
 
For Each Child in Container
     Debug.Print Child.Name
Next Child
```



 

 




