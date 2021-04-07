---
title: Énumération des groupes locaux
description: Sur les serveurs membres et les ordinateurs qui exécutent Windows 2000 professionnel, vous pouvez énumérer tous les groupes locaux.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Énumération des groupes locaux Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e106fc2517cfedd8fb5fa40e4b99798ee32de8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724556"
---
# <a name="enumerating-local-groups"></a><span data-ttu-id="c2823-104">Énumération des groupes locaux</span><span class="sxs-lookup"><span data-stu-id="c2823-104">Enumerating Local Groups</span></span>

<span data-ttu-id="c2823-105">Sur les serveurs membres et les ordinateurs qui exécutent Windows 2000 professionnel, vous pouvez énumérer tous les groupes locaux.</span><span class="sxs-lookup"><span data-stu-id="c2823-105">On member servers and computers running on Windows 2000 Professional, you can enumerate all local groups.</span></span>

<span data-ttu-id="c2823-106">Seuls les groupes locaux peuvent être créés sur les serveurs membres et Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="c2823-106">Only local groups can be created on member servers and Windows 2000 Professional.</span></span> <span data-ttu-id="c2823-107">Toutefois, ces groupes locaux peuvent contenir :</span><span class="sxs-lookup"><span data-stu-id="c2823-107">However, those local groups can contain:</span></span>

-   <span data-ttu-id="c2823-108">Groupes universels et globaux de la forêt qui contient le domaine dont l’ordinateur est membre.</span><span class="sxs-lookup"><span data-stu-id="c2823-108">Universal and Global groups from the forest that contains the domain to which the computer is a member.</span></span>
-   <span data-ttu-id="c2823-109">Groupes locaux de domaine à partir du domaine de cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c2823-109">Domain local groups from that computer's domain.</span></span>
-   <span data-ttu-id="c2823-110">Utilisateurs de n’importe quel domaine de la forêt.</span><span class="sxs-lookup"><span data-stu-id="c2823-110">Users from any domain in the forest.</span></span>

<span data-ttu-id="c2823-111">**Pour énumérer les groupes locaux sur un serveur membre ou un ordinateur exécutant Windows 2000 professionnel**</span><span class="sxs-lookup"><span data-stu-id="c2823-111">**To enumerate the local groups on a member server or computer running Windows 2000 Professional**</span></span>

1.  <span data-ttu-id="c2823-112">Connectez-vous à l’ordinateur à l’aide des règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="c2823-112">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="c2823-113">Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c2823-113">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="c2823-114">Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> <computer> ».</span><span class="sxs-lookup"><span data-stu-id="c2823-114">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span>

        <span data-ttu-id="c2823-115">Le paramètre « the <computer name> » est le nom du groupe d’ordinateurs auquel accéder.</span><span class="sxs-lookup"><span data-stu-id="c2823-115">"The <computer name>" parameter is the name of the computer group to access.</span></span> <span data-ttu-id="c2823-116">Ce paramètre indique à ADSI qu’il est lié à un ordinateur et permet à l’analyseur du fournisseur Winnt d’ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.</span><span class="sxs-lookup"><span data-stu-id="c2823-116">This parameter instruct ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>

    3.  <span data-ttu-id="c2823-117">Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="c2823-117">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>

2.  <span data-ttu-id="c2823-118">Définissez un filtre qui contient des « groupes » à l’aide de la propriété [**IADsContainer. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="c2823-118">Set a filter that contains "groups" using the [**IADsContainer.Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) property.</span></span> <span data-ttu-id="c2823-119">Cela vous permet d’énumérer le conteneur et de récupérer uniquement les groupes.</span><span class="sxs-lookup"><span data-stu-id="c2823-119">This enables you to enumerate the container and retrieve only groups.</span></span>
3.  <span data-ttu-id="c2823-120">Énumérez les objets de groupe à l’aide de la méthode [**IADsContainer :: obten \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) .</span><span class="sxs-lookup"><span data-stu-id="c2823-120">Enumerate the group objects, using the [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) method.</span></span>
4.  <span data-ttu-id="c2823-121">Pour chaque objet Group, utilisez l’interface [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) pour lire le nom et les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="c2823-121">For each the group object, use the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interface to read the name and members of the group.</span></span>

 

 