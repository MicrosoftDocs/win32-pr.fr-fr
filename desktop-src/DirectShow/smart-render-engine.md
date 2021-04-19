---
description: Moteur de rendu intelligent
ms.assetid: 279be879-9728-4fa1-bdf7-6b48485fc75f
title: Moteur de rendu intelligent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa727397f21aeba754cfe41f2dc4f9c1da1c91b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544555"
---
# <a name="smart-render-engine"></a><span data-ttu-id="e07ba-103">Moteur de rendu intelligent</span><span class="sxs-lookup"><span data-stu-id="e07ba-103">Smart Render Engine</span></span>

> [!Note]  
> <span data-ttu-id="e07ba-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e07ba-104">\[Deprecated.</span></span> <span data-ttu-id="e07ba-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e07ba-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e07ba-106">L’objet de moteur de rendu intelligent restitue la sortie compressée à partir d’une chronologie.</span><span class="sxs-lookup"><span data-stu-id="e07ba-106">The Smart Render Engine object renders compressed output from a timeline.</span></span> <span data-ttu-id="e07ba-107">Pour créer cet objet, appelez **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="e07ba-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="e07ba-108">Pour la sortie non compressée, utilisez le moteur de rendu de base.</span><span class="sxs-lookup"><span data-stu-id="e07ba-108">For uncompressed output, use the Basic Render Engine.</span></span> <span data-ttu-id="e07ba-109">L’identificateur de classe est CLSID \_ SmartRenderEngine.</span><span class="sxs-lookup"><span data-stu-id="e07ba-109">The class identifier is CLSID\_SmartRenderEngine.</span></span>

<span data-ttu-id="e07ba-110">Le moteur de rendu intelligent expose les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="e07ba-110">The Smart Render Engine exposes the following interfaces:</span></span>

-   [<span data-ttu-id="e07ba-111">**IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="e07ba-111">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   <span data-ttu-id="e07ba-112">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="e07ba-112">**IObjectWithSite**</span></span>
-   [<span data-ttu-id="e07ba-113">**IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="e07ba-113">**IRenderEngine**</span></span>](irenderengine.md)
-   [<span data-ttu-id="e07ba-114">**IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="e07ba-114">**IRenderEngine2**</span></span>](irenderengine2.md)
-   [<span data-ttu-id="e07ba-115">**ISmartRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="e07ba-115">**ISmartRenderEngine**</span></span>](ismartrenderengine.md)

## <a name="related-topics"></a><span data-ttu-id="e07ba-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e07ba-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e07ba-117">Rendu d’un projet</span><span class="sxs-lookup"><span data-stu-id="e07ba-117">Rendering a Project</span></span>](rendering-a-project.md)
</dt> <dt>

[<span data-ttu-id="e07ba-118">Moteur de rendu de base</span><span class="sxs-lookup"><span data-stu-id="e07ba-118">Basic Render Engine</span></span>](basic-render-engine.md)
</dt> </dl>

 

 



