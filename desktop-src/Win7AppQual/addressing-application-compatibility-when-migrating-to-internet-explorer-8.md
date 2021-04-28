---
description: Problèmes de compatibilité des applications lors de la migration vers Internet Explorer 8
ms.assetid: 3F79CF5F-416D-4C06-AAAE-D935F36CD2E2
title: Problèmes de compatibilité des applications lors de la migration vers Internet Explorer 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24fb4b0cbfb946f2385ddbd13ddc697987e659d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088767"
---
# <a name="addressing-application-compatibility-when-migrating-to-internet-explorer-8"></a><span data-ttu-id="328fa-103">Problèmes de compatibilité des applications lors de la migration vers Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="328fa-103">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>

<span data-ttu-id="328fa-104">Cette section fournit une vue d’ensemble du test des problèmes de compatibilité des applications et de la résolution de ces problèmes dans les applications Web pour Windows Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="328fa-104">This section provides an overview of testing for application compatibility issues and fixing those issues in web applications for Windows Internet Explorer 8.</span></span> <span data-ttu-id="328fa-105">Les rubriques suivantes décrivent les modifications apportées à Internet Explorer 8 et les outils et technologies pour garantir la compatibilité de votre application.</span><span class="sxs-lookup"><span data-stu-id="328fa-105">The following topics describe the changes in Internet Explorer 8 and the tools and technologies to ensure compatibility for your application.</span></span>



| <span data-ttu-id="328fa-106">Section</span><span class="sxs-lookup"><span data-stu-id="328fa-106">Section</span></span>                                                                                                                                              | <span data-ttu-id="328fa-107">Description</span><span class="sxs-lookup"><span data-stu-id="328fa-107">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="328fa-108">Introduction</span><span class="sxs-lookup"><span data-stu-id="328fa-108">Introduction</span></span>](introduction.md)                                                                                                                     | <span data-ttu-id="328fa-109">Fournit une vue d’ensemble des considérations sur la compatibilité d’Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="328fa-109">Provides an overview of Internet Explorer 8 compatibility considerations.</span></span>                 |
| [<span data-ttu-id="328fa-110">Présentation du défi de la compatibilité des applications</span><span class="sxs-lookup"><span data-stu-id="328fa-110">Understanding the Application Compatibility Challenge</span></span>](understanding-the-application-compatibility-challenge.md)                                   | <span data-ttu-id="328fa-111">Fournit des informations générales sur la compatibilité d’Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="328fa-111">Provides background about Internet Explorer 8 compatibility.</span></span>                              |
| [<span data-ttu-id="328fa-112">Normes Web et compatibilité des applications</span><span class="sxs-lookup"><span data-stu-id="328fa-112">Web Standards and Application Compatibility</span></span>](web-standards-and-application-compatibility.md)                                                       | <span data-ttu-id="328fa-113">Fournit des informations générales sur les raisons pour lesquelles les normes Web sont importantes.</span><span class="sxs-lookup"><span data-stu-id="328fa-113">Provides background about why web standards are important.</span></span>                                |
| [<span data-ttu-id="328fa-114">Concevoir des mises à jour qui ont un impact sur la compatibilité entre les navigateurs</span><span class="sxs-lookup"><span data-stu-id="328fa-114">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)                           | <span data-ttu-id="328fa-115">Fournit des informations topiques sur les mises à jour de conception qui ont un impact sur la compatibilité.</span><span class="sxs-lookup"><span data-stu-id="328fa-115">Provides topical information about design updates that impact compatibility.</span></span>              |
| [<span data-ttu-id="328fa-116">Résolution des problèmes de compatibilité dans les applications Web et les modules complémentaires</span><span class="sxs-lookup"><span data-stu-id="328fa-116">Fixing Compatibility Issues in Web Applications and Add-Ons</span></span>](remediating-web-applications-and-add-ons.md)                                          | <span data-ttu-id="328fa-117">Propose des suggestions pour résoudre les problèmes de compatibilité avec les applications Web et les modules complémentaires.</span><span class="sxs-lookup"><span data-stu-id="328fa-117">Offers suggestions for addressing compatibility issues with web applications and add-ons.</span></span> |
| [<span data-ttu-id="328fa-118">Outils de débogage d’applications Web et de modules complémentaires</span><span class="sxs-lookup"><span data-stu-id="328fa-118">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)                                             | <span data-ttu-id="328fa-119">Répertorie les outils disponibles pour le débogage d’applications Web et de modules complémentaires.</span><span class="sxs-lookup"><span data-stu-id="328fa-119">Lists tools that are available for debugging web applications and add-ons.</span></span>                |
| [<span data-ttu-id="328fa-120">Annexe 1 : modifications apportées à Internet Explorer 6 et au navigateur Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="328fa-120">Appendix 1: Internet Explorer 6 to Internet Explorer 8 browser changes</span></span>](appendix-1--internet-explorer-6-to-internet-explorer-8-browser-changes.md) | <span data-ttu-id="328fa-121">Répertorie les modifications de Microsoft Internet Explorer 6 vers Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="328fa-121">Lists changes from Microsoft Internet Explorer 6 to Internet Explorer 8.</span></span>                  |
| [<span data-ttu-id="328fa-122">Annexe 2 : scénarios de script de test</span><span class="sxs-lookup"><span data-stu-id="328fa-122">Appendix 2: Test Script Scenarios</span></span>](appendix-2--test-script-scenarios.md)                                                                           | <span data-ttu-id="328fa-123">Répertorie les scénarios recommandés pour le test de la compatibilité des sites.</span><span class="sxs-lookup"><span data-stu-id="328fa-123">Lists recommended scenarios for testing sites for compatibility.</span></span>                          |



 

 

 



