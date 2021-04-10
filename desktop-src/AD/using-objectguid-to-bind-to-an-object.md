---
title: Utilisation d’objectGUID pour la liaison à un objet
description: Un nom unique d’objet change si l’objet est renommé ou déplacé, par conséquent, le nom unique n’est pas un identificateur d’objet fiable.
ms.assetid: 6c038005-3ecb-4c00-b1a3-a231d3aea64e
ms.tgt_platform: multiple
keywords:
- Utilisation d’objectGUID pour la liaison à un objet AD
- Active Directory objectGUID
- objectGUID Active Directory, utilisant pour effectuer une liaison à un objet
- Active Directory, utilisation de, liaison, utilisation d’objectGUID pour la liaison à l’objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045c6194cf27b1697cc478b547105fb10335c219
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104030973"
---
# <a name="using-objectguid-to-bind-to-an-object"></a><span data-ttu-id="65f23-107">Utilisation d’objectGUID pour la liaison à un objet</span><span class="sxs-lookup"><span data-stu-id="65f23-107">Using objectGUID to Bind to an Object</span></span>

<span data-ttu-id="65f23-108">Un nom unique d’objet change si l’objet est renommé ou déplacé, par conséquent, le nom unique n’est pas un identificateur d’objet fiable.</span><span class="sxs-lookup"><span data-stu-id="65f23-108">An object distinguished name changes if the object is renamed or moved, therefore the distinguished name is not a reliable object identifier.</span></span> <span data-ttu-id="65f23-109">Dans Active Directory Domain Services, la propriété **objectGUID** d’un objet ne change jamais, même si l’objet est renommé ou déplacé.</span><span class="sxs-lookup"><span data-stu-id="65f23-109">In Active Directory Domain Services, an object's **objectGUID** property never changes, even if the object is renamed or moved.</span></span> <span data-ttu-id="65f23-110">Pour plus d’informations sur **objectGUID** et les identificateurs, consultez [noms d’objets et identités](object-names-and-identities.md).</span><span class="sxs-lookup"><span data-stu-id="65f23-110">For more information about **objectGUID** and identifiers, see [Object Names and Identities](object-names-and-identities.md).</span></span>

<span data-ttu-id="65f23-111">Le fournisseur LDAP Active Directory fournit une méthode pour établir une liaison à un objet à l’aide du GUID de l’objet.</span><span class="sxs-lookup"><span data-stu-id="65f23-111">The Active Directory LDAP provider provides a method to bind to an object using the object GUID.</span></span> <span data-ttu-id="65f23-112">Le format de la chaîne de liaison est le suivant :</span><span class="sxs-lookup"><span data-stu-id="65f23-112">The binding string format is as follows:</span></span>


```C++
LDAP://servername/<GUID=XXXXX>
```



<span data-ttu-id="65f23-113">Dans cet exemple, « ServerName » est le nom du serveur d’annuaire et « XXXXX » est la représentation sous forme de chaîne de la valeur hexadécimale du GUID.</span><span class="sxs-lookup"><span data-stu-id="65f23-113">In this example, "servername" is the name of the directory server and "XXXXX" is the string representation of the hexadecimal value of the GUID.</span></span> <span data-ttu-id="65f23-114">Le « servername » est facultatif.</span><span class="sxs-lookup"><span data-stu-id="65f23-114">The "servername" is optional.</span></span> <span data-ttu-id="65f23-115">La chaîne GUID est spécifiée dans le formulaire « XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX ».</span><span class="sxs-lookup"><span data-stu-id="65f23-115">The GUID string is specified in the "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" form.</span></span> <span data-ttu-id="65f23-116">La chaîne GUID peut également prendre la forme « XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX », qui est le même formulaire que la chaîne produite par la fonction [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , sans les accolades « {} ».</span><span class="sxs-lookup"><span data-stu-id="65f23-116">The GUID string can also take the form "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", which is the same form as the string produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function, without the surrounding braces "{}".</span></span> <span data-ttu-id="65f23-117">Pour plus d’informations et pour obtenir un exemple de code qui montre comment créer une chaîne pouvant être liée à partir d’un GUID, consultez l' [exemple de code permettant de créer une représentation sous forme de chaîne pouvant être liée d’un GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span><span class="sxs-lookup"><span data-stu-id="65f23-117">For more information and a code example that shows how to create a bindable string from a GUID, see [Example Code for Creating a Bindable String Representation of a GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span></span> <span data-ttu-id="65f23-118">La propriété [**IADs. Guid**](/windows/desktop/ADSI/iads-property-methods) peut être utilisée pour extraire la forme de chaîne correcte du GUID.</span><span class="sxs-lookup"><span data-stu-id="65f23-118">The [**IADs.GUID**](/windows/desktop/ADSI/iads-property-methods) property can be used to retrieve the proper string form of the GUID.</span></span>

<span data-ttu-id="65f23-119">Lors de la liaison à l’aide du GUID d’objet, certaines méthodes et propriétés [**IADs**](/windows/desktop/api/iads/nn-iads-iads) et [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="65f23-119">When binding using the object GUID, some [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) methods and properties are not supported.</span></span> <span data-ttu-id="65f23-120">Les propriétés **IADs** suivantes ne sont pas prises en charge par les objets obtenus par la liaison à l’aide du GUID de l’objet :</span><span class="sxs-lookup"><span data-stu-id="65f23-120">The following **IADs** properties are not supported by objects obtained by binding using the object GUID:</span></span>

-   [<span data-ttu-id="65f23-121">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="65f23-121">**ADsPath**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="65f23-122">**Nom**</span><span class="sxs-lookup"><span data-stu-id="65f23-122">**Name**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="65f23-123">**Parent**</span><span class="sxs-lookup"><span data-stu-id="65f23-123">**Parent**</span></span>](/windows/desktop/ADSI/iads-property-methods)

<span data-ttu-id="65f23-124">Les méthodes **IADsContainer** suivantes ne sont pas prises en charge par les objets obtenus par la liaison à l’aide du GUID de l’objet :</span><span class="sxs-lookup"><span data-stu-id="65f23-124">The following **IADsContainer** methods are not supported by objects obtained by binding using the object GUID:</span></span>

-   [<span data-ttu-id="65f23-125">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="65f23-125">**GetObject**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [<span data-ttu-id="65f23-126">**Créés**</span><span class="sxs-lookup"><span data-stu-id="65f23-126">**Create**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [<span data-ttu-id="65f23-127">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="65f23-127">**Delete**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [<span data-ttu-id="65f23-128">**CopyHere**</span><span class="sxs-lookup"><span data-stu-id="65f23-128">**CopyHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [<span data-ttu-id="65f23-129">**MoveHere**</span><span class="sxs-lookup"><span data-stu-id="65f23-129">**MoveHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

<span data-ttu-id="65f23-130">Pour utiliser ces méthodes et propriétés après avoir effectué une liaison à un objet à l’aide du GUID d’objet, utilisez la méthode [**IADs. obtenir**](/windows/desktop/api/iads/nf-iads-iads-get) pour récupérer le nom unique de l’objet, puis utilisez le nom unique pour effectuer une nouvelle liaison à l’objet.</span><span class="sxs-lookup"><span data-stu-id="65f23-130">To use these methods and properties after binding to an object using the object GUID, use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve the object distinguished name and then use the distinguished name to bind to the object again.</span></span>

<span data-ttu-id="65f23-131">Si une application stocke ou met en cache des identificateurs ou des références à des objets stockés dans Active Directory Domain Services, le GUID de l’objet est le meilleur identificateur à utiliser pour plusieurs raisons :</span><span class="sxs-lookup"><span data-stu-id="65f23-131">If an application stores or caches identifiers or references to objects stored in Active Directory Domain Services, the object GUID is the best identifier to use for several reasons:</span></span>

-   <span data-ttu-id="65f23-132">La propriété **objectGUID** de on Object ne change jamais même si l’objet est renommé ou déplacé.</span><span class="sxs-lookup"><span data-stu-id="65f23-132">The **objectGUID** property of on object never changes even if the object is renamed or moved.</span></span>
-   <span data-ttu-id="65f23-133">Il est facile de lier l’objet à l’aide du GUID de l’objet.</span><span class="sxs-lookup"><span data-stu-id="65f23-133">It is easy to bind to the object using the object GUID.</span></span>
-   <span data-ttu-id="65f23-134">Si l’objet est renommé ou déplacé, la propriété **objectGUID** fournit un identificateur unique qui peut être utilisé pour rechercher et identifier rapidement l’objet plutôt que d’avoir à composer une requête qui a des conditions pour toutes les propriétés qui identifieraient cet objet.</span><span class="sxs-lookup"><span data-stu-id="65f23-134">If the object is renamed or moved, the **objectGUID** property provides a single identifier that can be used to quickly find and identify the object rather than having to compose a query that has conditions for all properties that would identify that object.</span></span>

 

 