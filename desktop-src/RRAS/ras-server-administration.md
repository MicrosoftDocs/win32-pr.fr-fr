---
title: Administration du serveur RAS
description: Windows NT Server 4,0 fournit un ensemble de fonctions permettant d’administrer les autorisations et les ports des utilisateurs sur les serveurs RAS Windows NT/Windows 2000.
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- Administration de serveur, RAS
- Administration, serveur RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e096610e1cfe986c504a017f4d2b0d1033a6e6d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197224"
---
# <a name="ras-server-administration"></a><span data-ttu-id="40af3-105">Administration du serveur RAS</span><span class="sxs-lookup"><span data-stu-id="40af3-105">RAS Server Administration</span></span>

<span data-ttu-id="40af3-106">Windows NT Server 4,0 fournit un ensemble de fonctions permettant d’administrer les autorisations et les ports des utilisateurs sur les serveurs RAS Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="40af3-106">Windows NT Server 4.0 provides a set of functions for administering user permissions and ports on Windows NT/Windows 2000 RAS servers.</span></span> <span data-ttu-id="40af3-107">Windows 95 ne prend pas en charge ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="40af3-107">Windows 95 does not support these functions.</span></span> <span data-ttu-id="40af3-108">À l’aide de ces fonctions, vous pouvez développer une application d’administration de serveur RAS pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="40af3-108">Using these functions, you can develop a RAS server administration application to perform the following tasks:</span></span>

-   <span data-ttu-id="40af3-109">Énumérer les utilisateurs qui disposent d’un jeu d’autorisations RAS spécifié</span><span class="sxs-lookup"><span data-stu-id="40af3-109">Enumerate those users who have a specified set of RAS permissions</span></span>
-   <span data-ttu-id="40af3-110">Affecter ou révoquer des autorisations RAS pour un utilisateur spécifié</span><span class="sxs-lookup"><span data-stu-id="40af3-110">Assign or revoke RAS permissions for a specified user</span></span>
-   <span data-ttu-id="40af3-111">Énumérer les ports configurés sur un serveur RAS</span><span class="sxs-lookup"><span data-stu-id="40af3-111">Enumerate the configured ports on a RAS server</span></span>
-   <span data-ttu-id="40af3-112">Obtenir des informations et des statistiques sur un port spécifié sur un serveur RAS</span><span class="sxs-lookup"><span data-stu-id="40af3-112">Get information and statistics about a specified port on a RAS server</span></span>
-   <span data-ttu-id="40af3-113">Réinitialiser les compteurs de statistiques pour un port spécifié</span><span class="sxs-lookup"><span data-stu-id="40af3-113">Reset the statistics counters for a specified port</span></span>
-   <span data-ttu-id="40af3-114">Déconnecter un port spécifié</span><span class="sxs-lookup"><span data-stu-id="40af3-114">Disconnect a specified port</span></span>

<span data-ttu-id="40af3-115">Vous pouvez également installer une DLL d’administration de serveur RAS pour auditer les connexions utilisateur et affecter des adresses IP aux utilisateurs distants.</span><span class="sxs-lookup"><span data-stu-id="40af3-115">You can also install a RAS server administration DLL for auditing user connections and assigning IP addresses to dial-in users.</span></span> <span data-ttu-id="40af3-116">La DLL exporte un ensemble de fonctions que le serveur RAS appelle chaque fois qu’un utilisateur tente de se connecter ou de se déconnecter.</span><span class="sxs-lookup"><span data-stu-id="40af3-116">The DLL exports a set of functions that the RAS server calls whenever a user tries to connect or disconnect.</span></span>

 

 




