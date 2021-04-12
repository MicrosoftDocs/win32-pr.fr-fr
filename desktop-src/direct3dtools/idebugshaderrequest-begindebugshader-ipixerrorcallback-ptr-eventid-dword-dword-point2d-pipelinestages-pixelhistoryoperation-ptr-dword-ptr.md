---
description: Demande de démarrer une session de débogage de nuanceur pour l’étape de pipeline spécifiée, le pixel/vertex, le cas échéant, l’événement et le frame.
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugShaderRequest :: BeginDebugShader, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC93D31C-8593-4B03-B974-87B886B9431D
api_name:
- IDebugShaderRequest.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b6512dc8aa67b3f4d128be3cd2dcd2b622ba2035
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109255"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span data-ttu-id="95e6f-103"><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>IDebugShaderRequest :: BeginDebugShader, méthode</span><span class="sxs-lookup"><span data-stu-id="95e6f-103"><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>IDebugShaderRequest::BeginDebugShader method</span></span>

<span data-ttu-id="95e6f-104">Demande de démarrer une session de débogage de nuanceur pour l’étape de pipeline spécifiée, le pixel/vertex, le cas échéant, l’événement et le frame.</span><span class="sxs-lookup"><span data-stu-id="95e6f-104">Requests to start a shader debugging session for the specified pipeline stage, pixel/vertex if applicable, event, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e6f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95e6f-105">Syntax</span></span>


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback *     errorCallback,
   EventID                 eventID,
   DWORD                   frameNumber,
   DWORD                   vertex,
   Point2D                 pixel,
   PipeLineStages          stage,
   PixelHistoryOperation * pPixelHistory,
   DWORD *                 pDevice
);
```

## <a name="parameters"></a><span data-ttu-id="95e6f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95e6f-106">Parameters</span></span>

<span data-ttu-id="95e6f-107">*errorCallback* </span><span class="sxs-lookup"><span data-stu-id="95e6f-107">*errorCallback* </span></span>  
<span data-ttu-id="95e6f-108">Adresse d’un rappel pour les erreurs qui peuvent se produire pendant le débogage.</span><span class="sxs-lookup"><span data-stu-id="95e6f-108">The address of a callback for errors that might occur during debugging.</span></span>

<span data-ttu-id="95e6f-109">*1001* </span><span class="sxs-lookup"><span data-stu-id="95e6f-109">*eventID* </span></span>  
<span data-ttu-id="95e6f-110">Événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="95e6f-110">The specified event.</span></span>

<span data-ttu-id="95e6f-111">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="95e6f-111">*frameNumber* </span></span>  
<span data-ttu-id="95e6f-112">Frame spécifié.</span><span class="sxs-lookup"><span data-stu-id="95e6f-112">The specified frame.</span></span>

<span data-ttu-id="95e6f-113">*vertex* </span><span class="sxs-lookup"><span data-stu-id="95e6f-113">*vertex* </span></span>  
<span data-ttu-id="95e6f-114">Vertex spécifié.</span><span class="sxs-lookup"><span data-stu-id="95e6f-114">The specified vertex.</span></span> <span data-ttu-id="95e6f-115">S’applique uniquement lors du débogage d’un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="95e6f-115">Only applies when debugging a vertex shader.</span></span>

<span data-ttu-id="95e6f-116">*pixellisé* </span><span class="sxs-lookup"><span data-stu-id="95e6f-116">*pixel* </span></span>  
<span data-ttu-id="95e6f-117">Pixel spécifié.</span><span class="sxs-lookup"><span data-stu-id="95e6f-117">The specified pixel.</span></span> <span data-ttu-id="95e6f-118">S’applique uniquement lors du débogage d’un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="95e6f-118">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="95e6f-119">*mode* </span><span class="sxs-lookup"><span data-stu-id="95e6f-119">*stage* </span></span>  
<span data-ttu-id="95e6f-120">Étape de pipeline spécifiée.</span><span class="sxs-lookup"><span data-stu-id="95e6f-120">The specified pipeline stage.</span></span>

<span data-ttu-id="95e6f-121">*pPixelHistory* </span><span class="sxs-lookup"><span data-stu-id="95e6f-121">*pPixelHistory* </span></span>  
<span data-ttu-id="95e6f-122">Adresse des résultats de l’historique des pixels utilisée pour rechercher le pixel associé à déboguer.</span><span class="sxs-lookup"><span data-stu-id="95e6f-122">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="95e6f-123">S’applique uniquement lors du débogage d’un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="95e6f-123">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="95e6f-124">*pDevice* </span><span class="sxs-lookup"><span data-stu-id="95e6f-124">*pDevice* </span></span>  
<span data-ttu-id="95e6f-125">Adresse à passer au moteur de débogage pour communiquer avec cette session de débogage (moteur de débogage ReadProcessMemory sur cette adresse).</span><span class="sxs-lookup"><span data-stu-id="95e6f-125">The address to pass to the debug engine for communicating with this debug session (debug engine readprocessmemory on this address).</span></span>

## <a name="return-value"></a><span data-ttu-id="95e6f-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95e6f-126">Return value</span></span>

<span data-ttu-id="95e6f-127">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="95e6f-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="95e6f-128">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="95e6f-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="95e6f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95e6f-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="95e6f-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="95e6f-130">Header</span></span></p></td><td><span data-ttu-id="95e6f-131">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="95e6f-131">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="95e6f-132"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95e6f-132"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="95e6f-133">**IDebugShaderRequest**</span><span class="sxs-lookup"><span data-stu-id="95e6f-133">**IDebugShaderRequest**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 
