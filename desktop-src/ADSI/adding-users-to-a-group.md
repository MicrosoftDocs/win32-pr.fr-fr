---
title: Ajout d’utilisateurs à un groupe
description: Joe worden, administrateur d’entreprise, ajoutera désormais Julie Bankert au groupe d’administration. Pour ajouter un objet à un groupe, utilisez la méthode IADsGroup. Add.
ms.assetid: 57a9f5b2-2e48-401d-8d3b-eceb711a1df9
ms.tgt_platform: multiple
keywords:
- Ajout d’utilisateurs à un groupe ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea0ac78c0175248cb12e0f47a94ae60e7f1d16c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309270"
---
# <a name="adding-users-to-a-group"></a><span data-ttu-id="f8631-105">Ajout d’utilisateurs à un groupe</span><span class="sxs-lookup"><span data-stu-id="f8631-105">Adding Users to a Group</span></span>

<span data-ttu-id="f8631-106">Joe worden, administrateur d’entreprise, ajoutera désormais Julie Bankert au groupe d’administration.</span><span class="sxs-lookup"><span data-stu-id="f8631-106">Joe Worden, the enterprise administrator, will now add Julie Bankert to the Management group.</span></span> <span data-ttu-id="f8631-107">Pour ajouter un objet à un groupe, utilisez la méthode [**IADsGroup. Add**](/windows/desktop/api/Iads/nf-iads-iadsgroup-add) .</span><span class="sxs-lookup"><span data-stu-id="f8631-107">To add an object to a group, use the [**IADsGroup.Add**](/windows/desktop/api/Iads/nf-iads-iadsgroup-add) method.</span></span>


```VB
Dim grp as IADsGroup

Set grp = GetObject("LDAP://CN=Management,OU=Sales,DC=Fabrikam,DC=COM") 
grp.Add ("LDAP://CN=Julie Bankert,OU=Sales,DC=Fabrikam,DC=COM")
```



## <a name="related-topics"></a><span data-ttu-id="f8631-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f8631-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8631-109">Création d’un nouveau groupe</span><span class="sxs-lookup"><span data-stu-id="f8631-109">Creating a New Group</span></span>](creating-a-new-group.md)
</dt> </dl>

 

 




