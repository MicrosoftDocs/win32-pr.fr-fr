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
# <a name="enumeration"></a><span data-ttu-id="ad254-107">Énumération</span><span class="sxs-lookup"><span data-stu-id="ad254-107">Enumeration</span></span>

<span data-ttu-id="ad254-108">[L’accès aux données et leur manipulation avec ADSI](accessing-and-manipulating-data-with-adsi.md) offrent plusieurs exemples d’énumération.</span><span class="sxs-lookup"><span data-stu-id="ad254-108">[Accessing and Manipulating Data with ADSI](accessing-and-manipulating-data-with-adsi.md) provides several examples of enumeration.</span></span> <span data-ttu-id="ad254-109">Vous pouvez également énumérer les enfants des objets Container.</span><span class="sxs-lookup"><span data-stu-id="ad254-109">You can also enumerate the children of container objects.</span></span> <span data-ttu-id="ad254-110">Ces enfants sont eux-mêmes des objets, et non simplement des propriétés sur les objets.</span><span class="sxs-lookup"><span data-stu-id="ad254-110">These children are objects themselves, rather than just properties on objects.</span></span>

<span data-ttu-id="ad254-111">L’exemple suivant utilise l’interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) pour énumérer les enfants du conteneur.</span><span class="sxs-lookup"><span data-stu-id="ad254-111">The following example uses the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface to enumerate the children of the container.</span></span>


```VB
Dim Container as IADsContainer
Dim Child as IADs

Set Container = GetObject("LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com")
 
For Each Child in Container
     Debug.Print Child.Name
Next Child
```



 

 




