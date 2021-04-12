---
title: Création d’utilisateurs sur des serveurs membres et Windows 2000 professionnel
description: Cette rubrique décrit les étapes permettant de créer un utilisateur sur un serveur membre ou sur un ordinateur exécutant Windows 2000 professionnel.
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- Création d’utilisateurs sur des serveurs membres et Windows 2000 Professionnel AD
- utilisateurs Active Directory, création d’un utilisateur sur les serveurs membres et Windows 2000 professionnel
- Active Directory, utilisation de, utilisateurs, création d’un utilisateur sur des serveurs membres et Windows 2000 professionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050c9e8ecf68465097f2c185d2d31e0195c25a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031028"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="2327a-106">Création d’utilisateurs sur des serveurs membres et Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="2327a-106">Creating Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="2327a-107">**Pour créer un utilisateur**</span><span class="sxs-lookup"><span data-stu-id="2327a-107">**To create a user**</span></span>

1.  <span data-ttu-id="2327a-108">Connectez-vous à l’ordinateur à l’aide des règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="2327a-108">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="2327a-109">Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2327a-109">Use an account that has sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="2327a-110">Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> <computer> ».</span><span class="sxs-lookup"><span data-stu-id="2327a-110">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to tell ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="2327a-111">L' &lt; ordinateur « nom &gt; de l’ordinateur » est le nom de l’ordinateur dont vous souhaitez accéder aux groupes.</span><span class="sxs-lookup"><span data-stu-id="2327a-111">The "&lt;computer name&gt;" computer is the name of the computer whose groups you want to access.</span></span> <span data-ttu-id="2327a-112">Ce paramètre indique à ADSI qu’il est lié à un ordinateur et permet à l’analyseur du fournisseur Winnt d’ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.</span><span class="sxs-lookup"><span data-stu-id="2327a-112">This parameter tells ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="2327a-113">Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="2327a-113">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="2327a-114">Spécifiez « User » comme classe à l’aide de [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) pour ajouter l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2327a-114">Specify "user" as the class using [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) to add the user.</span></span>
3.  <span data-ttu-id="2327a-115">Écrivez l’utilisateur dans la base de données de sécurité de l’ordinateur à l’aide de [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="2327a-115">Write the user to the computer's security database using [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 