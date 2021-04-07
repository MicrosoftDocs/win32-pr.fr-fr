---
title: Énumération des utilisateurs sur les serveurs membres et Windows 2000 professionnel
description: Cette rubrique montre comment énumérer tous les utilisateurs, dans une base de données de sécurité locale, sur des serveurs membres et des ordinateurs s’exécutant sur Windows 2000 professionnel.
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- Énumération des utilisateurs sur les serveurs membres et la publicité Windows 2000 professionnel
- utilisateurs Active Directory, énumération des utilisateurs sur les serveurs membres et Windows 2000 professionnel
- Active Directory, utilisation de, utilisateurs, énumération des utilisateurs sur les serveurs membres et Windows 2000 professionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664af51b7feb2e0b9a683664659eefda11c9cb9d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724549"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="61f6a-106">Énumération des utilisateurs sur les serveurs membres et Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="61f6a-106">Enumerating Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="61f6a-107">Cette rubrique montre comment énumérer tous les utilisateurs, dans une base de données de sécurité locale, sur des serveurs membres et des ordinateurs s’exécutant sur Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="61f6a-107">This topic shows how to enumerate all users, in a local security database, on member servers and computers running on Windows 2000 Professional.</span></span>

<span data-ttu-id="61f6a-108">**Pour énumérer les utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="61f6a-108">**To enumerate the users**</span></span>

1.  <span data-ttu-id="61f6a-109">Connectez-vous à l’ordinateur à l’aide des règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="61f6a-109">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="61f6a-110">Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="61f6a-110">Use an account that has sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="61f6a-111">Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> <computer> ».</span><span class="sxs-lookup"><span data-stu-id="61f6a-111">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="61f6a-112">Le &lt; paramètre « nom &gt; de l’ordinateur » est le nom de l’ordinateur pour lequel les groupes doivent accéder.</span><span class="sxs-lookup"><span data-stu-id="61f6a-112">The "&lt;computer name&gt;" parameter is the name of the computer for whose groups to access.</span></span> <span data-ttu-id="61f6a-113">Ce paramètre indique à ADSI qu’il est lié à un ordinateur et permet à l’analyseur du fournisseur Winnt d’ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.</span><span class="sxs-lookup"><span data-stu-id="61f6a-113">This parameter instructs ADSI that it is binding to a computer and enables the WinNT provider parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="61f6a-114">Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="61f6a-114">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="61f6a-115">Ajoutez « user » à la propriété [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="61f6a-115">Add "user" to the [**IADsContainer.Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) property.</span></span> <span data-ttu-id="61f6a-116">L’énumération ne contient alors que les objets qui ont la classe d’objet « User ».</span><span class="sxs-lookup"><span data-stu-id="61f6a-116">This causes the enumeration to only contain objects that have the "user" object class.</span></span>
3.  <span data-ttu-id="61f6a-117">Énumérez les objets.</span><span class="sxs-lookup"><span data-stu-id="61f6a-117">Enumerate the objects.</span></span> <span data-ttu-id="61f6a-118">Pour chaque objet utilisateur, utilisez les méthodes de l’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) ou [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) pour lire les propriétés de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="61f6a-118">For each user object, use the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) interface methods to read the user properties.</span></span>

 

 