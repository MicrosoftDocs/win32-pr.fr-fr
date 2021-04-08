---
title: Obtention d’informations sur les erreurs RPC étendues
description: RPC permet d’obtenir des informations d’erreur étendues. Cette section décrit comment obtenir ces informations d’erreur et propose des recommandations sur l’utilisation des informations.
ms.assetid: 7a386def-c640-42f4-9869-b6a1c522984a
keywords:
- RPC appel de procédure distante, meilleures pratiques, informations d’erreur étendues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7856dd76a86763fc3f537577f9c547508fbf34ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673145"
---
# <a name="obtaining-extended-rpc-error-information"></a><span data-ttu-id="6d6ee-105">Obtention d’informations sur les erreurs RPC étendues</span><span class="sxs-lookup"><span data-stu-id="6d6ee-105">Obtaining Extended RPC Error Information</span></span>

<span data-ttu-id="6d6ee-106">RPC permet d’obtenir des informations d’erreur étendues.</span><span class="sxs-lookup"><span data-stu-id="6d6ee-106">RPC provides the capability to obtain extended error information.</span></span> <span data-ttu-id="6d6ee-107">Cette section décrit comment obtenir ces informations d’erreur et propose des recommandations sur l’utilisation des informations.</span><span class="sxs-lookup"><span data-stu-id="6d6ee-107">This section describes how such error information can be obtained, and offers recommendations on how to use the information.</span></span>

<span data-ttu-id="6d6ee-108">Cette section se compose des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d6ee-108">This section is broken into the following topics:</span></span>

-   [<span data-ttu-id="6d6ee-109">Besoin d’informations d’erreur étendues</span><span class="sxs-lookup"><span data-stu-id="6d6ee-109">The Need For Extended Error Information</span></span>](the-need-for-extended-error-information.md)
-   [<span data-ttu-id="6d6ee-110">Sécurité et informations d’erreur étendues</span><span class="sxs-lookup"><span data-stu-id="6d6ee-110">Security and Extended Error Information</span></span>](security-and-extended-error-information.md)
-   [<span data-ttu-id="6d6ee-111">Activation des informations d’erreur étendues</span><span class="sxs-lookup"><span data-stu-id="6d6ee-111">Enabling Extended Error Information</span></span>](enabling-extended-error-information.md)
-   [<span data-ttu-id="6d6ee-112">Description des informations d’erreur étendues</span><span class="sxs-lookup"><span data-stu-id="6d6ee-112">Understanding Extended Error Information</span></span>](understanding-extended-error-information.md)
-   [<span data-ttu-id="6d6ee-113">Fiabilité des informations d’erreur étendues</span><span class="sxs-lookup"><span data-stu-id="6d6ee-113">Reliability of Extended Error Information</span></span>](reliability-of-extended-error-information.md)
-   [<span data-ttu-id="6d6ee-114">Indépendance par rapport aux autres composants</span><span class="sxs-lookup"><span data-stu-id="6d6ee-114">Independence From Other Components</span></span>](independence-from-other-components.md)
-   [<span data-ttu-id="6d6ee-115">Informations d’erreur étendues pour l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="6d6ee-115">Extended Error Information for the User</span></span>](extended-error-information-for-the-user.md)
-   [<span data-ttu-id="6d6ee-116">Informations d’erreur étendues pour le serveur ou l’application</span><span class="sxs-lookup"><span data-stu-id="6d6ee-116">Extended Error Information for the Server or Application</span></span>](extended-error-information-for-the-server-or-application.md)
-   [<span data-ttu-id="6d6ee-117">Emplacements de détection des informations d’erreur étendues</span><span class="sxs-lookup"><span data-stu-id="6d6ee-117">Extended Error Information Detection Locations</span></span>](extended-error-information-detection-locations.md)

<span data-ttu-id="6d6ee-118">Cette section est étroitement liée au débogage des applications RPC.</span><span class="sxs-lookup"><span data-stu-id="6d6ee-118">This section is closely tied with RPC application debugging.</span></span> <span data-ttu-id="6d6ee-119">Pour plus d’informations sur le débogage RPC, consultez \[ package du débogueur \] .</span><span class="sxs-lookup"><span data-stu-id="6d6ee-119">For additional information about RPC debugging, see \[debugger package\].</span></span>

 

 




