---
title: À propos de l’administration du service d’accès à distance
description: Les systèmes d’exploitation Windows 2000 et versions ultérieures fournissent un ensemble de fonctions permettant d’administrer les autorisations et les ports des utilisateurs sur les serveurs RAS.
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- Routage et accès à distance service RRAS, administration RAS
- Routage et accès à distance service RRAS, administration RAS, Description
- Administration RAS RRAS
- Administration RAS RRAS, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bdb55049e99b6d3df9980fc35879341b488531
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510210"
---
# <a name="about-remote-access-service-administration"></a><span data-ttu-id="1d902-107">À propos de l’administration du service d’accès à distance</span><span class="sxs-lookup"><span data-stu-id="1d902-107">About Remote Access Service Administration</span></span>

<span data-ttu-id="1d902-108">Les systèmes d’exploitation Windows 2000 et versions ultérieures fournissent un ensemble de fonctions permettant d’administrer les autorisations et les ports des utilisateurs sur les serveurs RAS.</span><span class="sxs-lookup"><span data-stu-id="1d902-108">Windows 2000 and later operating systems provide a set of functions for administering user permissions and ports on RAS servers.</span></span> <span data-ttu-id="1d902-109">À l’aide de ces fonctions, vous pouvez développer une application d’administration de serveur RAS pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="1d902-109">Using these functions, you can develop a RAS server administration application to perform the following tasks:</span></span>

-   <span data-ttu-id="1d902-110">Énumérer les utilisateurs qui disposent d’un jeu d’autorisations RAS spécifié</span><span class="sxs-lookup"><span data-stu-id="1d902-110">Enumerate those users who have a specified set of RAS permissions</span></span>
-   <span data-ttu-id="1d902-111">Affecter ou révoquer des autorisations RAS pour un utilisateur spécifié</span><span class="sxs-lookup"><span data-stu-id="1d902-111">Assign or revoke RAS permissions for a specified user</span></span>
-   <span data-ttu-id="1d902-112">Énumérer les ports configurés sur un serveur RAS</span><span class="sxs-lookup"><span data-stu-id="1d902-112">Enumerate the configured ports on a RAS server</span></span>
-   <span data-ttu-id="1d902-113">Obtenir des informations et des statistiques sur un port spécifié sur un serveur RAS</span><span class="sxs-lookup"><span data-stu-id="1d902-113">Get information and statistics about a specified port on a RAS server</span></span>
-   <span data-ttu-id="1d902-114">Réinitialiser les compteurs de statistiques pour un port spécifié</span><span class="sxs-lookup"><span data-stu-id="1d902-114">Reset the statistics counters for a specified port</span></span>
-   <span data-ttu-id="1d902-115">Déconnecter un port spécifié</span><span class="sxs-lookup"><span data-stu-id="1d902-115">Disconnect a specified port</span></span>

<span data-ttu-id="1d902-116">Vous pouvez également installer une DLL d’administration de serveur RAS pour auditer les connexions utilisateur et affecter des adresses IP aux utilisateurs distants.</span><span class="sxs-lookup"><span data-stu-id="1d902-116">You can also install a RAS server administration DLL to audit user connections and assign IP addresses to dial-in users.</span></span> <span data-ttu-id="1d902-117">La DLL exporte un ensemble de fonctions que le serveur RAS appelle chaque fois qu’un utilisateur tente de se connecter ou de se déconnecter.</span><span class="sxs-lookup"><span data-stu-id="1d902-117">The DLL exports a set of functions that the RAS server calls whenever a user tries to connect or disconnect.</span></span>

<span data-ttu-id="1d902-118">Cette documentation décrit les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="1d902-118">This documentation describes the following topics:</span></span>

-   [<span data-ttu-id="1d902-119">Comparaison de fonctions : Windows 2000 et le package redistribuable RRAS</span><span class="sxs-lookup"><span data-stu-id="1d902-119">Function Comparison: Windows 2000 vs. RRAS Redistributable</span></span>](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [<span data-ttu-id="1d902-120">Administration des utilisateurs RAS</span><span class="sxs-lookup"><span data-stu-id="1d902-120">RAS User Administration</span></span>](ras-user-administration.md)
-   [<span data-ttu-id="1d902-121">Administration du serveur et du port RAS</span><span class="sxs-lookup"><span data-stu-id="1d902-121">RAS Server and Port Administration</span></span>](ras-server-and-port-administration.md)
-   [<span data-ttu-id="1d902-122">DLL d’administration RAS</span><span class="sxs-lookup"><span data-stu-id="1d902-122">RAS Administration DLL</span></span>](ras-administration-dll.md)
-   [<span data-ttu-id="1d902-123">Configuration du registre des DLL d’administration RAS</span><span class="sxs-lookup"><span data-stu-id="1d902-123">RAS Administration DLL Registry Setup</span></span>](ras-administration-dll-registry-setup.md)

 

 




