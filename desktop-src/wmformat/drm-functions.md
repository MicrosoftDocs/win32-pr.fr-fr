---
title: Fonctions du client Microsoft Windows Media DRM
description: Fonctions du client Microsoft Windows Media DRM
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- Windows Media Format SDK, fonctions
- gestion des droits numériques (DRM), fonctions
- DRM (gestion des droits numériques), fonctions
- API étendues du client DRM, fonctions
- API étendues clientes, fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c1730413a4918b0f748099fbd55714339a7e9b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106509487"
---
# <a name="microsoft-windows-media-drm-client-functions"></a><span data-ttu-id="288d0-108">Fonctions du client Microsoft Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="288d0-108">Microsoft Windows Media DRM Client Functions</span></span>

<span data-ttu-id="288d0-109">Les fonctions suivantes sont implémentées dans le cadre des API étendues du client Microsoft Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="288d0-109">The following functions are implemented as part of the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="288d0-110">Fonction</span><span class="sxs-lookup"><span data-stu-id="288d0-110">Function</span></span>                                                             | <span data-ttu-id="288d0-111">Description</span><span class="sxs-lookup"><span data-stu-id="288d0-111">Description</span></span>                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="288d0-112">**WMDRMCreateProvider**</span><span class="sxs-lookup"><span data-stu-id="288d0-112">**WMDRMCreateProvider**</span></span>](wmdrmcreateprovider.md)                   | <span data-ttu-id="288d0-113">Crée une fabrique de classes qui peut créer les autres objets DRM.</span><span class="sxs-lookup"><span data-stu-id="288d0-113">Creates a class factory that can create the other DRM objects.</span></span> <span data-ttu-id="288d0-114">Cette fonction ne nécessite pas de bibliothèque de stubs de la part de Microsoft et crée des objets qui ne prennent pas en charge les fonctionnalités DRM protégées.</span><span class="sxs-lookup"><span data-stu-id="288d0-114">This function does not require a stub library from Microsoft and creates objects that do not support the protected DRM features.</span></span> |
| [<span data-ttu-id="288d0-115">**WMDRMCreateProtectedProvider**</span><span class="sxs-lookup"><span data-stu-id="288d0-115">**WMDRMCreateProtectedProvider**</span></span>](wmdrmcreateprotectedprovider.md) | <span data-ttu-id="288d0-116">Crée une fabrique de classes qui peut créer les autres objets DRM.</span><span class="sxs-lookup"><span data-stu-id="288d0-116">Creates a class factory that can create the other DRM objects.</span></span> <span data-ttu-id="288d0-117">Cette fonction requiert une bibliothèque de stubs de la part de Microsoft et crée des objets qui prennent en charge les fonctionnalités DRM protégées.</span><span class="sxs-lookup"><span data-stu-id="288d0-117">This function requires a stub library from Microsoft and creates objects that support the protected DRM features.</span></span>                |
| [<span data-ttu-id="288d0-118">**WMDRMShutdown**</span><span class="sxs-lookup"><span data-stu-id="288d0-118">**WMDRMShutdown**</span></span>](wmdrmshutdown.md)                               | <span data-ttu-id="288d0-119">Libère les ressources utilisées par les API.</span><span class="sxs-lookup"><span data-stu-id="288d0-119">Releases resources used by the APIs.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="288d0-120">**WMDRMStartup**</span><span class="sxs-lookup"><span data-stu-id="288d0-120">**WMDRMStartup**</span></span>](wmdrmstartup.md)                                 | <span data-ttu-id="288d0-121">Initialise les ressources utilisées par les API.</span><span class="sxs-lookup"><span data-stu-id="288d0-121">Initializes resources used by the APIs.</span></span>                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="288d0-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="288d0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="288d0-123">**Guide de référence de programmation**</span><span class="sxs-lookup"><span data-stu-id="288d0-123">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




