---
title: Suppression d’utilisateurs sur les serveurs membres et Windows 2000 professionnel
description: Cette rubrique montre comment supprimer un utilisateur d’un serveur membre ou d’un ordinateur exécutant Windows 2000 professionnel.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- utilisateurs Active Directory, suppression d’un utilisateur sur les serveurs membres et Windows 2000 professionnel
- Active Directory, utilisation de, utilisateurs, suppression d’utilisateurs sur les serveurs membres et Windows 2000 professionnel
- suppression d’un utilisateur
- serveur, suppression d’un utilisateur
- suppression d’utilisateurs sur les serveurs membres et la publicité Windows 2000 professionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae4287c8b7d32e15e7df3e73f365409d7fe49a0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031020"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="498e2-108">Suppression d’utilisateurs sur les serveurs membres et Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="498e2-108">Deleting Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="498e2-109">Cette rubrique montre comment supprimer un utilisateur d’un serveur membre ou d’un ordinateur exécutant Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="498e2-109">This topic shows how to delete a user from a member server or computer running on Windows 2000 Professional.</span></span>

<span data-ttu-id="498e2-110">**Pour supprimer un utilisateur**</span><span class="sxs-lookup"><span data-stu-id="498e2-110">**To delete a user**</span></span>

1.  <span data-ttu-id="498e2-111">Connectez-vous à l’ordinateur à l’aide des règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="498e2-111">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="498e2-112">Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="498e2-112">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="498e2-113">Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> <computer> ».</span><span class="sxs-lookup"><span data-stu-id="498e2-113">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to tell ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="498e2-114">Le &lt; paramètre « nom &gt; de l’ordinateur » est le nom de l’ordinateur dont vous souhaitez accéder aux groupes.</span><span class="sxs-lookup"><span data-stu-id="498e2-114">The "&lt;computer name&gt;" parameter is the name of the computer whose groups you want to access.</span></span> <span data-ttu-id="498e2-115">Ce paramètre indique à ADSI qu’il est lié à un ordinateur et permet à l’analyseur du fournisseur Winnt d’ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.</span><span class="sxs-lookup"><span data-stu-id="498e2-115">This parameter notifies ADSI that it is binding to a computer and allows the WinNT provider parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="498e2-116">Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="498e2-116">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="498e2-117">Spécifiez « User » comme classe à l’aide de [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) pour supprimer l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="498e2-117">Specify "user" as the class using [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) to delete the user.</span></span>

    <span data-ttu-id="498e2-118">N’oubliez pas que vous n’avez pas besoin d’appeler [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) pour valider la modification apportée au conteneur.</span><span class="sxs-lookup"><span data-stu-id="498e2-118">Be aware that you do not need to call [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the change to the container.</span></span> <span data-ttu-id="498e2-119">L’appel de [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) valide la suppression de l’utilisateur directement dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="498e2-119">The [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) call commits the deletion of the user directly to the directory.</span></span>

 

 