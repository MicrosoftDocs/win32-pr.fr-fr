---
description: Rappel qui avertit l’hôte des informations d’image des étapes de pipeline retournées par la requête dans.
MS-HAID: vspixengine.IPipeLineStagesCallback\_ResultCallback\_PipeLineStagesID\_EventID\_DWORD\_DWORD\_DWORD\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 922DBEE0-CE47-4292-A5E6-4503E6F77A23
api_name:
- IPipeLineStagesCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c9c09c0fe1e68dc0d0613589ff8b3d5037face9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317794"
---
# <a name="span-idvspixengineipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arrspanipipelinestagescallbackresultcallback-method"></a><span data-ttu-id="7a3fc-103"><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>IPipeLineStagesCallback :: ResultCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="7a3fc-103"><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>IPipeLineStagesCallback::ResultCallback method</span></span>

<span data-ttu-id="7a3fc-104">Rappel qui avertit l’hôte des informations d’image des étapes de pipeline retournées par la requête dans.</span><span class="sxs-lookup"><span data-stu-id="7a3fc-104">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a3fc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a3fc-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   PipeLineStagesID stageId,
   EventID          eid,
   DWORD            width,
   DWORD            height,
   DWORD            format,
   DWORD            size,
   BYTE []          count5_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="7a3fc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a3fc-106">Parameters</span></span>

<span data-ttu-id="7a3fc-107">*stageId* </span><span class="sxs-lookup"><span data-stu-id="7a3fc-107">*stageId* </span></span>  
<span data-ttu-id="7a3fc-108">Étape de pipeline représentée dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="7a3fc-108">The pipeline stage represented in the results.</span></span>

<span data-ttu-id="7a3fc-109">*Numéro* </span><span class="sxs-lookup"><span data-stu-id="7a3fc-109">*eid* </span></span>  
<span data-ttu-id="7a3fc-110">Événement représenté dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="7a3fc-110">The event represented in the results.</span></span>

<span data-ttu-id="7a3fc-111">*Largeur* </span><span class="sxs-lookup"><span data-stu-id="7a3fc-111">*width* </span></span>  
<span data-ttu-id="7a3fc-112">Largeur de l’image de visualisation du pipeline.</span><span class="sxs-lookup"><span data-stu-id="7a3fc-112">The width of the pipeline visualization image.</span></span>

<span data-ttu-id="7a3fc-113">*celle* </span><span class="sxs-lookup"><span data-stu-id="7a3fc-113">*height* </span></span>  
<span data-ttu-id="7a3fc-114">Hauteur de l’image de visualisation du pipeline.</span><span class="sxs-lookup"><span data-stu-id="7a3fc-114">The height of the pipeline visualization image.</span></span>

<span data-ttu-id="7a3fc-115">*format* </span><span class="sxs-lookup"><span data-stu-id="7a3fc-115">*format* </span></span>  
<span data-ttu-id="7a3fc-116">Format de l’image de visualisation du pipeline.</span><span class="sxs-lookup"><span data-stu-id="7a3fc-116">The format of the pipeline visualization image.</span></span>

<span data-ttu-id="7a3fc-117">*corps* </span><span class="sxs-lookup"><span data-stu-id="7a3fc-117">*size* </span></span>  
<span data-ttu-id="7a3fc-118">Taille de l’image en octets.</span><span class="sxs-lookup"><span data-stu-id="7a3fc-118">The size of the image in bytes.</span></span>

<span data-ttu-id="7a3fc-119">*\_mémoire tampon count5* </span><span class="sxs-lookup"><span data-stu-id="7a3fc-119">*count5\_buffer* </span></span>  
<span data-ttu-id="7a3fc-120">Image de visualisation du pipeline.</span><span class="sxs-lookup"><span data-stu-id="7a3fc-120">The pipeline visualization image.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a3fc-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a3fc-121">Return value</span></span>

<span data-ttu-id="7a3fc-122">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7a3fc-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7a3fc-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7a3fc-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a3fc-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a3fc-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7a3fc-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a3fc-125">Header</span></span></p></td><td><span data-ttu-id="7a3fc-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="7a3fc-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="7a3fc-127"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a3fc-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="7a3fc-128">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="7a3fc-128">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
