---
description: Demande asynchrone d’obtenir des images d’aperçu pour la fenêtre étapes de canalisation Graphics.
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestAsync\_EventID\_DWORD\_PipeLineStagesID\_arr\_DWORD\_DWORD\_IPipeLineStagesCallback\_ptr\_BOOL\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesRequest :: RequestAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B725E541-EAC8-49DE-9EE7-C20698FE4A1F
api_name:
- IPipeLineStagesRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 89c67689668aa1c4227b33d861495c2504e5d626
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521852"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dwordspanipipelinestagesrequestrequestasync-method"></a><span data-ttu-id="ae3aa-103"><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>IPipeLineStagesRequest :: RequestAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="ae3aa-103"><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>IPipeLineStagesRequest::RequestAsync method</span></span>

<span data-ttu-id="ae3aa-104">Demande asynchrone d’obtenir des images d’aperçu pour la fenêtre étapes de canalisation Graphics.</span><span class="sxs-lookup"><span data-stu-id="ae3aa-104">An asynchronous request to get preview images for the graphics pipeline stages window.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae3aa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae3aa-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   DWORD                     numStages,
   PipeLineStagesID []       count1_stageIds,
   DWORD                     width,
   DWORD                     height,
   IPipeLineStagesCallback * requestCallback,
   BOOL                      getMeshData,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="ae3aa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae3aa-106">Parameters</span></span>

<span data-ttu-id="ae3aa-107">*1001* </span><span class="sxs-lookup"><span data-stu-id="ae3aa-107">*eventID* </span></span>  
<span data-ttu-id="ae3aa-108">ID de l’événement graphique pour lequel des images sont demandées.</span><span class="sxs-lookup"><span data-stu-id="ae3aa-108">The ID of the graphics event that images are being requested for.</span></span>

<span data-ttu-id="ae3aa-109">*numStages* </span><span class="sxs-lookup"><span data-stu-id="ae3aa-109">*numStages* </span></span>  
<span data-ttu-id="ae3aa-110">Nombre d’étapes de pipeline pour lesquelles des images sont demandées.</span><span class="sxs-lookup"><span data-stu-id="ae3aa-110">The number of pipeline stages that images are being requested for.</span></span>

<span data-ttu-id="ae3aa-111">*count1 \_ stageIds* </span><span class="sxs-lookup"><span data-stu-id="ae3aa-111">*count1\_stageIds* </span></span>  
<span data-ttu-id="ae3aa-112">ID des étapes de pipeline pour lesquelles des images sont demandées.</span><span class="sxs-lookup"><span data-stu-id="ae3aa-112">IDs of the pipeline stages that images are being requested for.</span></span>

<span data-ttu-id="ae3aa-113">*Largeur* </span><span class="sxs-lookup"><span data-stu-id="ae3aa-113">*width* </span></span>  
<span data-ttu-id="ae3aa-114">Largeur des images demandées.</span><span class="sxs-lookup"><span data-stu-id="ae3aa-114">The width of the requested images.</span></span>

<span data-ttu-id="ae3aa-115">*celle* </span><span class="sxs-lookup"><span data-stu-id="ae3aa-115">*height* </span></span>  
<span data-ttu-id="ae3aa-116">Hauteur des images demandées.</span><span class="sxs-lookup"><span data-stu-id="ae3aa-116">The height of the requested images.</span></span>

<span data-ttu-id="ae3aa-117">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="ae3aa-117">*requestCallback* </span></span>  
<span data-ttu-id="ae3aa-118">Adresse du rappel utilisé pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="ae3aa-118">The address of the callback used to notify the host of results.</span></span>

<span data-ttu-id="ae3aa-119">*getMeshData* </span><span class="sxs-lookup"><span data-stu-id="ae3aa-119">*getMeshData* </span></span>  
<span data-ttu-id="ae3aa-120">true pour retourner les données de maillage ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="ae3aa-120">true to return mesh data; otherwise false.</span></span>

<span data-ttu-id="ae3aa-121">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="ae3aa-121">*requestCookie* </span></span>  
<span data-ttu-id="ae3aa-122">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="ae3aa-122">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="ae3aa-123">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="ae3aa-123">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="ae3aa-124">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ae3aa-124">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae3aa-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae3aa-125">Return value</span></span>

<span data-ttu-id="ae3aa-126">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ae3aa-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ae3aa-127">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ae3aa-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae3aa-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae3aa-128">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ae3aa-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae3aa-129">Header</span></span></p></td><td><span data-ttu-id="ae3aa-130">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ae3aa-130">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ae3aa-131"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae3aa-131"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ae3aa-132">**IPipeLineStagesRequest**</span><span class="sxs-lookup"><span data-stu-id="ae3aa-132">**IPipeLineStagesRequest**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 
