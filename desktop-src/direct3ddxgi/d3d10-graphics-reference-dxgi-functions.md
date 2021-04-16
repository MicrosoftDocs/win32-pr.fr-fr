---
description: Cette section contient des informations sur les fonctions fournies par DXGI.
ms.assetid: 209d2e65-b118-47a7-aece-fb140fdede3f
title: DXGI, fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06cb98c47ec3e2cb841aa5c27017ee6bb614f9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520876"
---
# <a name="dxgi-functions"></a><span data-ttu-id="4c7d8-103">DXGI, fonctions</span><span class="sxs-lookup"><span data-stu-id="4c7d8-103">DXGI Functions</span></span>

<span data-ttu-id="4c7d8-104">Cette section contient des informations sur les fonctions fournies par DXGI.</span><span class="sxs-lookup"><span data-stu-id="4c7d8-104">This section contains info about the functions provided by DXGI.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4c7d8-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="4c7d8-105">In this section</span></span>



| <span data-ttu-id="4c7d8-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="4c7d8-106">Topic</span></span>                                                                                   | <span data-ttu-id="4c7d8-107">Description</span><span class="sxs-lookup"><span data-stu-id="4c7d8-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c7d8-108">**CreateDXGIFactory**</span><span class="sxs-lookup"><span data-stu-id="4c7d8-108">**CreateDXGIFactory**</span></span>](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)<br/>                               | <span data-ttu-id="4c7d8-109">Crée une fabrique DXGI 1,0 que vous pouvez utiliser pour générer d’autres objets DXGI.</span><span class="sxs-lookup"><span data-stu-id="4c7d8-109">Creates a DXGI 1.0 factory that you can use to generate other DXGI objects.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="4c7d8-110">**CreateDXGIFactory1**</span><span class="sxs-lookup"><span data-stu-id="4c7d8-110">**CreateDXGIFactory1**</span></span>](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)<br/>                             | <span data-ttu-id="4c7d8-111">Crée une fabrique DXGI 1,1 que vous pouvez utiliser pour générer d’autres objets DXGI.</span><span class="sxs-lookup"><span data-stu-id="4c7d8-111">Creates a DXGI 1.1 factory that you can use to generate other DXGI objects.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="4c7d8-112">**CreateDXGIFactory2**</span><span class="sxs-lookup"><span data-stu-id="4c7d8-112">**CreateDXGIFactory2**</span></span>](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)<br/>                             | <span data-ttu-id="4c7d8-113">Crée une fabrique DXGI 1,3 que vous pouvez utiliser pour générer d’autres objets DXGI.</span><span class="sxs-lookup"><span data-stu-id="4c7d8-113">Creates a DXGI 1.3 factory that you can use to generate other DXGI objects.</span></span><br/> <span data-ttu-id="4c7d8-114">Dans Windows 8, toute fabrique DXGI créée pendant que DXGIDebug.dll était présente sur le système le chargerait et l’utiliserait.</span><span class="sxs-lookup"><span data-stu-id="4c7d8-114">In Windows 8, any DXGI factory created while DXGIDebug.dll was present on the system would load and use it.</span></span> <span data-ttu-id="4c7d8-115">À partir de Windows 8.1, les applications demandent explicitement que DXGIDebug.dll être chargé à la place.</span><span class="sxs-lookup"><span data-stu-id="4c7d8-115">Starting in Windows 8.1, apps explicitly request that DXGIDebug.dll be loaded instead.</span></span> <span data-ttu-id="4c7d8-116">Utilisez [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) et spécifiez l' \_ \_ \_ indicateur de débogage dxgi create Factory pour demander DXGIDebug.dll ; la dll sera chargée si elle est présente sur le système.</span><span class="sxs-lookup"><span data-stu-id="4c7d8-116">Use [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) and specify the DXGI\_CREATE\_FACTORY\_DEBUG flag to request DXGIDebug.dll; the DLL will be loaded if it is present on the system.</span></span><br/> |
| [<span data-ttu-id="4c7d8-117">**DXGIDeclareAdapterRemovalSupport**</span><span class="sxs-lookup"><span data-stu-id="4c7d8-117">**DXGIDeclareAdapterRemovalSupport**</span></span>](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)<br/> | <span data-ttu-id="4c7d8-118">Permet à un processus d’indiquer qu’il est résilient à l’un de ses appareils graphiques en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="4c7d8-118">Allows a process to indicate that it's resilient to any of its graphics devices being removed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="4c7d8-119">**DXGIGetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="4c7d8-119">**DXGIGetDebugInterface**</span></span>](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)<br/>                       | <span data-ttu-id="4c7d8-120">Récupère une interface de débogage.</span><span class="sxs-lookup"><span data-stu-id="4c7d8-120">Retrieves a debugging interface.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="4c7d8-121">**DXGIGetDebugInterface1**</span><span class="sxs-lookup"><span data-stu-id="4c7d8-121">**DXGIGetDebugInterface1**</span></span>](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1)<br/>                     | <span data-ttu-id="4c7d8-122">Récupère une interface que les applications du Windows Store utilisent pour déboguer l’infrastructure Microsoft DirectX Graphics (DXGI).</span><span class="sxs-lookup"><span data-stu-id="4c7d8-122">Retrieves an interface that Windows Store apps use for debugging the Microsoft DirectX Graphics Infrastructure (DXGI).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="4c7d8-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c7d8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c7d8-124">Référence DXGI</span><span class="sxs-lookup"><span data-stu-id="4c7d8-124">DXGI Reference</span></span>](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

 




