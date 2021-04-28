---
description: <span id="vspixengine.ipipelinestagesrequest2"></span>Interface IPipeLineStagesRequest2-non utilisée. Anciennement une demande de données d’étapes de pipeline.
MS-HAID: vspixengine.IPipeLineStagesRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPipeLineStagesRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B40E0701-3F17-4B3A-B150-D4B243662042
api_name:
- IPipeLineStagesRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b9dd185ba709aa4439deb98f92be3c8f2f456cea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107067"
---
# <a name="span-idvspixengineipipelinestagesrequest2spanipipelinestagesrequest2-interface"></a><span data-ttu-id="43723-104"><span id="vspixengine.ipipelinestagesrequest2"></span>Interface IPipeLineStagesRequest2</span><span class="sxs-lookup"><span data-stu-id="43723-104"><span id="vspixengine.ipipelinestagesrequest2"></span>IPipeLineStagesRequest2 interface</span></span>

<span data-ttu-id="43723-105">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="43723-105">Not used.</span></span> <span data-ttu-id="43723-106">Anciennement une demande de données d’étapes de pipeline.</span><span class="sxs-lookup"><span data-stu-id="43723-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="43723-107">Membres</span><span class="sxs-lookup"><span data-stu-id="43723-107">Members</span></span>

<span data-ttu-id="43723-108">L’interface **IPipeLineStagesRequest2** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="43723-108">The **IPipeLineStagesRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="43723-109">**IPipeLineStagesRequest2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="43723-109">**IPipeLineStagesRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="43723-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="43723-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="43723-111"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="43723-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="43723-112">L’interface **IPipeLineStagesRequest2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="43723-112">The **IPipeLineStagesRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="43723-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="43723-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="43723-114">Description</span><span class="sxs-lookup"><span data-stu-id="43723-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="43723-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="43723-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="43723-116">Demande asynchrone d’obtenir des données de nuanceur de calcul pour la distribution spécifiée.</span><span class="sxs-lookup"><span data-stu-id="43723-116">An asynchronous request to get compute shader data for the specified dispatch.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="43723-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="43723-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="43723-118">Demande asynchrone pour obtenir si l’étape du nuanceur de calcul a été utilisée pour le frame et l’événement spécifiés.</span><span class="sxs-lookup"><span data-stu-id="43723-118">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="43723-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43723-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="43723-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="43723-120">Header</span></span></p></td><td><span data-ttu-id="43723-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="43723-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
