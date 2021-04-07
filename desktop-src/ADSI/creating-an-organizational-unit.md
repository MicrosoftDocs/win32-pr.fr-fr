---
title: Création d'une unité d'organisation
description: Maintenant que vous disposez de l’objet domaine, vous pouvez commencer à créer des unités d’organisation.
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- Création d’une unité d’organisation ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ec0da1efe78d54eba8bc0dc05a998717aaf91f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939599"
---
# <a name="creating-an-organizational-unit"></a><span data-ttu-id="ddf6a-104">Création d'une unité d'organisation</span><span class="sxs-lookup"><span data-stu-id="ddf6a-104">Creating an Organizational Unit</span></span>

<span data-ttu-id="ddf6a-105">Maintenant que vous disposez de l’objet domaine, vous pouvez commencer à créer des unités d’organisation.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-105">Now that you have the domain object, you can start creating organizational units.</span></span> <span data-ttu-id="ddf6a-106">Fabrikam a deux divisions : ventes et production.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-106">Fabrikam has two divisions: Sales and Production.</span></span> <span data-ttu-id="ddf6a-107">L’entreprise envisage d’embaucher deux administrateurs Windows 2000 pour gérer chaque division.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-107">The company is planning to hire two Windows 2000 administrators to manage each division.</span></span> <span data-ttu-id="ddf6a-108">Joe worden, en tant qu’administrateur d’entreprise, crée deux nouvelles unités d’organisation sous le domaine fabrikam.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-108">Joe Worden, as the enterprise administrator, will create two new organizational units under the Fabrikam domain.</span></span> <span data-ttu-id="ddf6a-109">En créant une unité d’organisation, Joe peut regrouper plusieurs objets et permettre à quelqu’un d’autre de gérer ces objets.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-109">By creating an organizational unit, Joe can group multiple objects together and let someone else manage these objects.</span></span> <span data-ttu-id="ddf6a-110">L’exemple de code suivant crée l’unité d’organisation Sales (UO).</span><span class="sxs-lookup"><span data-stu-id="ddf6a-110">The following code example creates the Sales Organizational Unit (OU).</span></span>


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



<span data-ttu-id="ddf6a-111">La méthode [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) accepte le nom de la classe et le nom du nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-111">The [**IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) method accepts the class name and the name of the new object.</span></span> <span data-ttu-id="ddf6a-112">À ce stade, l’objet n’est pas validé pour Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-112">At this point the object is not committed to Active Directory.</span></span> <span data-ttu-id="ddf6a-113">Toutefois, vous aurez une référence d’objet ADSI/COM sur le client.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-113">You, however, will have an ADSI/COM object reference on the client.</span></span> <span data-ttu-id="ddf6a-114">Avec cet objet ADSI, vous pouvez définir ou modifier des attributs à l’aide de la méthode [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) .</span><span class="sxs-lookup"><span data-stu-id="ddf6a-114">With this ADSI object, you can set or modify attributes using the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method.</span></span> <span data-ttu-id="ddf6a-115">La méthode **IADs. put** accepte le nom d’attribut et la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-115">The **IADs.Put** method accepts the attribute name and the value of the attribute.</span></span> <span data-ttu-id="ddf6a-116">Toujours, rien n’est validé dans le répertoire ; tout est mis en cache au niveau du client.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-116">Still, nothing is committed to the directory; everything is cached at the client.</span></span> <span data-ttu-id="ddf6a-117">Quand vous appelez la méthode [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , les modifications, dans ce cas, la création d’un objet et la modification d’attribut, sont validées dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-117">When you call the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method, the changes, in this case, object creation and attribute modification, are committed to the directory.</span></span> <span data-ttu-id="ddf6a-118">Ces modifications sont traitées, ce qui signifie que vous verrez soit le nouvel objet avec tous les attributs que vous définissez, soit aucun objet.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-118">These changes are transacted, meaning that you will see either the new object with all attributes you set, or no object at all.</span></span>

<span data-ttu-id="ddf6a-119">Vous pouvez également imbriquer des unités d’organisation.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-119">You can also nest organizational units.</span></span> <span data-ttu-id="ddf6a-120">L’exemple de code suivant suppose que la Division Sales est divisée dans les régions est et ouest.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-120">The following code example assumes that the Sales division is divided further into the East and West regions.</span></span>


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



<span data-ttu-id="ddf6a-121">Cela s’applique également à la région ouest.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-121">This also applies for the West region.</span></span>

<span data-ttu-id="ddf6a-122">Pour établir une liaison directe avec la région est de l’organisation Sales, spécifiez le nom unique.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-122">To bind directly to the East region in the Sales organization, specify the distinguished name.</span></span>


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



<span data-ttu-id="ddf6a-123">Si vous avez déjà lié l’objet parent (ventes), vous pouvez effectuer une liaison à l’objet enfant (est) à partir de l’objet parent à l’aide du nom relatif de l’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-123">If you have already bound to the parent object (Sales), you can bind to the child object (East) from the parent object using the relative name of the child object.</span></span>


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



<span data-ttu-id="ddf6a-124">Pour vous assurer que les objets ont été créés, utilisez le composant logiciel enfichable MMC utilisateurs et ordinateurs Active Directory pour afficher les nouvelles unités d’organisation.</span><span class="sxs-lookup"><span data-stu-id="ddf6a-124">To ensure that the objects have been created, use the Active Directory Users and Computers MMC snap-in to view the new organizational units.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ddf6a-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ddf6a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddf6a-126">Déplacement des utilisateurs existants vers l’unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="ddf6a-126">Moving Existing Users to the Organizational Unit</span></span>](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 




