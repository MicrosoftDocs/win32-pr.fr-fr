---
description: Rappel pour retourner une cible de rendu. Le format de la cible de rendu retournée est R8G8B8A8 \_ UNORM, quel que soit le format du renderTarget dans le moteur.
MS-HAID: vspixengine.IFrameBufferCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IFrameBufferCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 613AD7AC-0732-49E2-8155-AE0A76597BE9
api_name:
- IFrameBufferCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 565813999cda898f693aab37b24f7979896a8497
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392664"
---
# <a name="span-idvspixengineiframebuffercallbackspaniframebuffercallback-interface"></a><span data-ttu-id="a5e21-104"><span id="vspixengine.iframebuffercallback"></span>Interface IFrameBufferCallback</span><span class="sxs-lookup"><span data-stu-id="a5e21-104"><span id="vspixengine.iframebuffercallback"></span>IFrameBufferCallback interface</span></span>

<span data-ttu-id="a5e21-105">Rappel pour retourner une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="a5e21-105">Callback to return a render target.</span></span> <span data-ttu-id="a5e21-106">Le format de la cible de rendu retournée est R8G8B8A8 \_ UNORM, quel que soit le format du renderTarget dans le moteur.</span><span class="sxs-lookup"><span data-stu-id="a5e21-106">The format of the returned render target is R8G8B8A8\_UNORM regardless of the format of the in-engine rendertarget.</span></span>

## <a name="members"></a><span data-ttu-id="a5e21-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a5e21-107">Members</span></span>

<span data-ttu-id="a5e21-108">L’interface **IFrameBufferCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a5e21-108">The **IFrameBufferCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a5e21-109">**IFrameBufferCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a5e21-109">**IFrameBufferCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="a5e21-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a5e21-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="a5e21-111"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="a5e21-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="a5e21-112">L’interface **IFrameBufferCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a5e21-112">The **IFrameBufferCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="a5e21-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="a5e21-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="a5e21-114">Description</span><span class="sxs-lookup"><span data-stu-id="a5e21-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="a5e21-115"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="a5e21-115"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a5e21-116">Rappel qui avertit l’hôte des informations trame retournées par la requête associée.</span><span class="sxs-lookup"><span data-stu-id="a5e21-116">A callback that notifies the host of framebuffer information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="a5e21-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5e21-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a5e21-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5e21-118">Header</span></span></p></td><td><span data-ttu-id="a5e21-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a5e21-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
