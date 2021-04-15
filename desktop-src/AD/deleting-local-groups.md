---
title: Suppression de groupes locaux
description: Cette rubrique montre comment supprimer un groupe local d’un serveur membre ou d’un ordinateur exécutant Windows 2000 professionnel.
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- Suppression des groupes locaux Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b55f90a8e6ac5cb77bf878d5ac680a6da91f73
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462887"
---
# <a name="deleting-local-groups"></a><span data-ttu-id="6264b-104">Suppression de groupes locaux</span><span class="sxs-lookup"><span data-stu-id="6264b-104">Deleting Local Groups</span></span>

<span data-ttu-id="6264b-105">Cette rubrique montre comment supprimer un groupe local d’un serveur membre ou d’un ordinateur exécutant Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="6264b-105">This topic shows how to delete a local group from a member server or computer running on Windows 2000 Professional.</span></span>

<span data-ttu-id="6264b-106">**Pour supprimer un groupe local**</span><span class="sxs-lookup"><span data-stu-id="6264b-106">**To delete a local group**</span></span>

1.  <span data-ttu-id="6264b-107">Connectez-vous à l’ordinateur à l’aide des règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="6264b-107">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="6264b-108">Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6264b-108">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="6264b-109">Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> <computer> ».</span><span class="sxs-lookup"><span data-stu-id="6264b-109">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="6264b-110">Le &lt; paramètre « nom &gt; de l’ordinateur » est le nom du groupe d’ordinateurs auquel accéder.</span><span class="sxs-lookup"><span data-stu-id="6264b-110">The "&lt;computer name&gt;" parameter is the name of the computer group to access.</span></span> <span data-ttu-id="6264b-111">Ce paramètre indique à ADSI qu’il est lié à un ordinateur et permet à l’analyseur du fournisseur Winnt d’ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.</span><span class="sxs-lookup"><span data-stu-id="6264b-111">This parameter instruct ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="6264b-112">Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="6264b-112">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="6264b-113">Spécifiez « Group » comme classe à l’aide de [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)pour supprimer le groupe.</span><span class="sxs-lookup"><span data-stu-id="6264b-113">Specify "group" as the class using [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)to delete the group.</span></span>

    <span data-ttu-id="6264b-114">Vous n’avez pas besoin d’appeler [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) pour valider la modification apportée au conteneur.</span><span class="sxs-lookup"><span data-stu-id="6264b-114">You do not need to call [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the change to the container.</span></span> <span data-ttu-id="6264b-115">L’appel de [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) valide la suppression du groupe directement dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="6264b-115">The [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) call commits the deletion of the group directly to the directory.</span></span>

 

 