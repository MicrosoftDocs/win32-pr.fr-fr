---
title: Déplacement des utilisateurs existants vers l’unité d’organisation
description: Lorsque l’administrateur d’entreprise, Joe worden, met à niveau le domaine Windows NT 4,0 vers Active Directory, tous les utilisateurs et les groupes sont migrés vers les conteneurs utilisateurs dans le domaine fabrikam.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Déplacement des utilisateurs existants vers la publicité d’unité d’organisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ff7110eaf956f108854e8442faa7386667346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190736"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a><span data-ttu-id="161b1-104">Déplacement des utilisateurs existants vers l’unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="161b1-104">Moving Existing Users to the Organizational Unit</span></span>

<span data-ttu-id="161b1-105">Lorsque l’administrateur d’entreprise, Joe worden, met à niveau le domaine Windows NT 4,0 vers Active Directory, tous les utilisateurs et les groupes sont migrés vers les conteneurs utilisateurs dans le domaine fabrikam.</span><span class="sxs-lookup"><span data-stu-id="161b1-105">When the enterprise administrator, Joe Worden, upgrades the Windows NT 4.0 domain to Active Directory, all users and groups are migrated to the Users containers in the Fabrikam domain.</span></span> <span data-ttu-id="161b1-106">Joe peut à présent déplacer ces utilisateurs et groupes vers les unités d’organisation appropriées.</span><span class="sxs-lookup"><span data-stu-id="161b1-106">Joe can now move those users and groups to the appropriate organizational units.</span></span> <span data-ttu-id="161b1-107">Un objet peut également être déplacé entre des domaines Windows 2000 associés à l’aide d’ADSI.</span><span class="sxs-lookup"><span data-stu-id="161b1-107">An object can also be moved between related Windows 2000 domains using ADSI.</span></span>

<span data-ttu-id="161b1-108">Dans l’exemple de code suivant, Joe déplace « JeffSmith » vers l’organisation Sales.</span><span class="sxs-lookup"><span data-stu-id="161b1-108">In the following code example, Joe moves "jeffsmith" to the Sales organization.</span></span>


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



<span data-ttu-id="161b1-109">La méthode [**IADsContainer. MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) prend l’ADsPath de l’objet à déplacer et le nouveau nom de l’objet (RDN).</span><span class="sxs-lookup"><span data-stu-id="161b1-109">The [**IADsContainer.MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) method takes the ADsPath of the object to be moved and the new object name (RDN).</span></span> <span data-ttu-id="161b1-110">Pour conserver le même nom, vous pouvez spécifier **null** (**vbNullString**) pour le paramètre *bstrNewName* .</span><span class="sxs-lookup"><span data-stu-id="161b1-110">To keep the same name, you can specify **NULL** (**vbNullString**) for the *bstrNewName* parameter.</span></span> <span data-ttu-id="161b1-111">Pour renommer l’objet lorsqu’il est déplacé, spécifiez le nouveau nom unique relatif pour le paramètre *bstrNewName* .</span><span class="sxs-lookup"><span data-stu-id="161b1-111">To rename the object when it is moved, specify the new relative distinguished name for the *bstrNewName* parameter.</span></span> <span data-ttu-id="161b1-112">Par exemple, pour déplacer JeffSmith vers l’organisation Sales et renommer l’objet « JeffSmith » en « Jeff \_ Smith » dans la même opération, Joe exécute le code suivant :</span><span class="sxs-lookup"><span data-stu-id="161b1-112">For example, to move jeffsmith to the sales organization and rename the "jeffsmith" object to "jeff\_smith" in the same operation, Joe would execute the following code:</span></span>


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a><span data-ttu-id="161b1-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="161b1-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="161b1-114">Création de nouveaux utilisateurs dans l’unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="161b1-114">Creating New Users in the Organizational Unit</span></span>](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 




