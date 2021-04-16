---
description: Moteur de rendu de base
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Moteur de rendu de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9b51240b43c58de99b7d6fe1f7ad61f754c7ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522220"
---
# <a name="basic-render-engine"></a><span data-ttu-id="2eeda-103">Moteur de rendu de base</span><span class="sxs-lookup"><span data-stu-id="2eeda-103">Basic Render Engine</span></span>

> [!Note]  
> <span data-ttu-id="2eeda-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="2eeda-104">\[Deprecated.</span></span> <span data-ttu-id="2eeda-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2eeda-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2eeda-106">L’objet de moteur de rendu de base restitue la sortie non compressée d’une chronologie.</span><span class="sxs-lookup"><span data-stu-id="2eeda-106">The Basic Render Engine object renders uncompressed output from a timeline.</span></span> <span data-ttu-id="2eeda-107">Pour créer cet objet, appelez **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="2eeda-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="2eeda-108">Pour la sortie compressée, utilisez le moteur de rendu intelligent.</span><span class="sxs-lookup"><span data-stu-id="2eeda-108">For compressed output, use the Smart Render Engine.</span></span> <span data-ttu-id="2eeda-109">L’identificateur de classe est CLSID \_ RenderEngine.</span><span class="sxs-lookup"><span data-stu-id="2eeda-109">The class identifier is CLSID\_RenderEngine.</span></span>

<span data-ttu-id="2eeda-110">Le moteur de rendu de base expose les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="2eeda-110">The Basic Render Engine exposes the following interfaces:</span></span>

-   [<span data-ttu-id="2eeda-111">**IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="2eeda-111">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   <span data-ttu-id="2eeda-112">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="2eeda-112">IObjectWithSite</span></span>
-   [<span data-ttu-id="2eeda-113">**IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="2eeda-113">**IRenderEngine**</span></span>](irenderengine.md)
-   [<span data-ttu-id="2eeda-114">**IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="2eeda-114">**IRenderEngine2**</span></span>](irenderengine2.md)

## <a name="related-topics"></a><span data-ttu-id="2eeda-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2eeda-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2eeda-116">Rendu d’un projet</span><span class="sxs-lookup"><span data-stu-id="2eeda-116">Rendering a Project</span></span>](rendering-a-project.md)
</dt> <dt>

[<span data-ttu-id="2eeda-117">Moteur de rendu intelligent</span><span class="sxs-lookup"><span data-stu-id="2eeda-117">Smart Render Engine</span></span>](smart-render-engine.md)
</dt> </dl>

 

 



