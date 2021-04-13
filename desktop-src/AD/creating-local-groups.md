---
title: Création de groupes locaux
description: Seuls les groupes locaux peuvent être créés pour les serveurs membres et Windows 2000 professionnel.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Création de groupes locaux Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705902b0066913fcd6eed56ba7c74e299144595f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314639"
---
# <a name="creating-local-groups"></a><span data-ttu-id="37fa0-104">Création de groupes locaux</span><span class="sxs-lookup"><span data-stu-id="37fa0-104">Creating Local Groups</span></span>

<span data-ttu-id="37fa0-105">Seuls les groupes locaux peuvent être créés pour les serveurs membres et Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="37fa0-105">Only local groups can be created for member servers and Windows 2000 Professional.</span></span>

<span data-ttu-id="37fa0-106">**Pour créer un groupe local pour un serveur membre ou un ordinateur exécutant Windows 2000 professionnel**</span><span class="sxs-lookup"><span data-stu-id="37fa0-106">**To create a local group for a member server or computer running Windows 2000 Professional**</span></span>

1.  <span data-ttu-id="37fa0-107">Connectez-vous à l’ordinateur à l’aide des règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="37fa0-107">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="37fa0-108">Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="37fa0-108">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="37fa0-109">Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> <computer> ».</span><span class="sxs-lookup"><span data-stu-id="37fa0-109">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span>

        <span data-ttu-id="37fa0-110">Le &lt; paramètre « nom &gt; de l’ordinateur » est le nom des groupes d’ordinateurs auxquels accéder.</span><span class="sxs-lookup"><span data-stu-id="37fa0-110">The "&lt;computer name&gt;" parameter is the name of the computer groups to access.</span></span>

        <span data-ttu-id="37fa0-111">Dans la chaîne de liaison, le &lt; paramètre « Computer &gt; » indique à ADSI qu’il est lié à un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="37fa0-111">In the binding string, the "&lt;computer&gt;" parameter instructs ADSI that it is binding to a computer.</span></span> <span data-ttu-id="37fa0-112">ADSI met ces données à la disposition de l’analyseur du fournisseur Winnt afin qu’il puisse ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.</span><span class="sxs-lookup"><span data-stu-id="37fa0-112">ADSI makes this data available to the WinNT provider's parser so that it can skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>

    3.  <span data-ttu-id="37fa0-113">Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="37fa0-113">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>

2.  <span data-ttu-id="37fa0-114">Spécifiez « localGroup » en tant que classe à l’aide de [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) pour ajouter le groupe.</span><span class="sxs-lookup"><span data-stu-id="37fa0-114">Specify "localGroup" as the class using [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) to add the group.</span></span>
    > [!Note]  
    > <span data-ttu-id="37fa0-115">Si vous spécifiez « Group » comme classe, ADSI utilise « localGroup ».</span><span class="sxs-lookup"><span data-stu-id="37fa0-115">If you specify "group" as the class, ADSI uses "localGroup".</span></span> <span data-ttu-id="37fa0-116">Ne spécifiez pas la classe en tant que « globalGroup ».</span><span class="sxs-lookup"><span data-stu-id="37fa0-116">Do not specify the class as "globalGroup".</span></span> <span data-ttu-id="37fa0-117">Les groupes de la classe « globalGroup » ne peuvent pas être créés sur des serveurs membres ou sur un ordinateur exécutant Windows NT Workstation ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="37fa0-117">Groups of class "globalGroup" cannot be created on member servers or a computer running Windows NT Workstation/Windows 2000 Professional.</span></span> <span data-ttu-id="37fa0-118">Si vous spécifiez « globalGroup », [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) crée le groupe dans le cache de propriétés, mais [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) n’écrit pas le groupe dans la base de données de sécurité et ne retourne pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="37fa0-118">If you specify "globalGroup", [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) creates the group in the property cache, but [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) does not write the group to the security database and it does not return an error.</span></span>

     

3.  <span data-ttu-id="37fa0-119">Écrivez le groupe dans la base de données de sécurité de l’ordinateur à l’aide de [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="37fa0-119">Write the group to the computer security database using [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 