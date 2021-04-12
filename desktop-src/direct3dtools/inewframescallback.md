---
description: Rappel à partir du moteur indiquant qu’il a terminé l’analyse de tous les nouveaux frames ajoutés au journal.
MS-HAID: vspixengine.INewFramesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface INewFramesCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A73E1EA4-F9D5-43F1-B363-20B3F7B3D8B0
api_name:
- INewFramesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 134de14d95ceb625f1c5d4461c0b379b7f9e8a0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392867"
---
# <a name="span-idvspixengineinewframescallbackspaninewframescallback-interface"></a><span data-ttu-id="19e74-103"><span id="vspixengine.inewframescallback"></span>Interface INewFramesCallback</span><span class="sxs-lookup"><span data-stu-id="19e74-103"><span id="vspixengine.inewframescallback"></span>INewFramesCallback interface</span></span>

<span data-ttu-id="19e74-104">Rappel à partir du moteur indiquant qu’il a terminé l’analyse de tous les nouveaux frames ajoutés au journal.</span><span class="sxs-lookup"><span data-stu-id="19e74-104">Callback from engine indicating that it is done parsing any new frames added to the log.</span></span>

## <a name="members"></a><span data-ttu-id="19e74-105">Membres</span><span class="sxs-lookup"><span data-stu-id="19e74-105">Members</span></span>

<span data-ttu-id="19e74-106">L’interface **INewFramesCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="19e74-106">The **INewFramesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="19e74-107">**INewFramesCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="19e74-107">**INewFramesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="19e74-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="19e74-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="19e74-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="19e74-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="19e74-110">L’interface **INewFramesCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="19e74-110">The **INewFramesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="19e74-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="19e74-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="19e74-112">Description</span><span class="sxs-lookup"><span data-stu-id="19e74-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="19e74-113"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="19e74-113"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="19e74-114">Rappel qui avertit l’hôte que toutes les demandes ont été annulées.</span><span class="sxs-lookup"><span data-stu-id="19e74-114">A callback that notifies the host that all requests have been cancelled.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="19e74-115"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="19e74-115"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="19e74-116">Rappel qui avertit l’hôte d’une demande annulée.</span><span class="sxs-lookup"><span data-stu-id="19e74-116">A callback that notifies the host of a canceled request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="19e74-117"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></span><span class="sxs-lookup"><span data-stu-id="19e74-117"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="19e74-118">Rappel qui avertit l’hôte d’une demande annulée à l’aide d’un cookie qui identifie de façon unique la demande.</span><span class="sxs-lookup"><span data-stu-id="19e74-118">A callback that notifies the host of a canceled request by using a cookie that uniquely identifies the request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="19e74-119"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></span><span class="sxs-lookup"><span data-stu-id="19e74-119"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="19e74-120">Rappel qui avertit l’hôte que de nouveaux frames sont disponibles pour être traités.</span><span class="sxs-lookup"><span data-stu-id="19e74-120">A callback that notifies the host that new frames are available to be processed.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="19e74-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19e74-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="19e74-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="19e74-122">Header</span></span></p></td><td><span data-ttu-id="19e74-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="19e74-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
