---
description: Fonction de rappel utilisée pour informer l’hôte d’informations sur les événements dans la liste des événements.
MS-HAID: vspixengine.IFrameEventsCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameEventsCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5AB67A11-00C1-47AF-8C8C-8B2FDD095BCF
api_name:
- IFrameEventsCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e746c54f2a82adb5042cd479e4ca04299c1b7402
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200757"
---
# <a name="span-idvspixengineiframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arrspaniframeeventscallbackresultcallback-method"></a><span data-ttu-id="30aa2-103"><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>IFrameEventsCallback :: ResultCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="30aa2-103"><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>IFrameEventsCallback::ResultCallback method</span></span>

<span data-ttu-id="30aa2-104">Fonction de rappel utilisée pour informer l’hôte d’informations sur les événements dans la liste des événements.</span><span class="sxs-lookup"><span data-stu-id="30aa2-104">A callback function used to notify the host of information about events in the event list.</span></span>

## <a name="syntax"></a><span data-ttu-id="30aa2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30aa2-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD      frameNumber,
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count1_pRowData
);
```

## <a name="parameters"></a><span data-ttu-id="30aa2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30aa2-106">Parameters</span></span>

<span data-ttu-id="30aa2-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="30aa2-107">*frameNumber* </span></span>  
<span data-ttu-id="30aa2-108">Numéro de frame associé aux événements.</span><span class="sxs-lookup"><span data-stu-id="30aa2-108">The frame number associated with the events.</span></span>

<span data-ttu-id="30aa2-109">*numElements* </span><span class="sxs-lookup"><span data-stu-id="30aa2-109">*numElements* </span></span>  
<span data-ttu-id="30aa2-110">Nombre total de champs dans toutes les colonnes de tous les événements.</span><span class="sxs-lookup"><span data-stu-id="30aa2-110">The total number of fields in all columns of all events.</span></span>

<span data-ttu-id="30aa2-111">*numRows* </span><span class="sxs-lookup"><span data-stu-id="30aa2-111">*numRows* </span></span>  
<span data-ttu-id="30aa2-112">Nombre d’événements dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="30aa2-112">The number of events in the result.</span></span>

<span data-ttu-id="30aa2-113">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="30aa2-113">*numColumns* </span></span>  
<span data-ttu-id="30aa2-114">Nombre de colonnes (champs) dans chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="30aa2-114">The number of columns (fields) in each row.</span></span>

<span data-ttu-id="30aa2-115">*count1 \_ pRowData* </span><span class="sxs-lookup"><span data-stu-id="30aa2-115">*count1\_pRowData* </span></span>  
<span data-ttu-id="30aa2-116">Informations sur les événements ; un élément pour chaque champ de chaque événement.</span><span class="sxs-lookup"><span data-stu-id="30aa2-116">Information about the events; one item for each field of each event.</span></span>

## <a name="return-value"></a><span data-ttu-id="30aa2-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30aa2-117">Return value</span></span>

<span data-ttu-id="30aa2-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="30aa2-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30aa2-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="30aa2-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="30aa2-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30aa2-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="30aa2-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="30aa2-121">Header</span></span></p></td><td><span data-ttu-id="30aa2-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="30aa2-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="30aa2-123"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30aa2-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="30aa2-124">**IFrameEventsCallback**</span><span class="sxs-lookup"><span data-stu-id="30aa2-124">**IFrameEventsCallback**</span></span>](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
