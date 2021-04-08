---
description: Demande l’extraction des informations spécifiées à partir de la table des objets pour l’événement spécifié.
MS-HAID: vspixengine.IObjectTableRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IObjectTableCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IObjectTableRequest :: RequestAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: EE40F584-CDDE-465D-B4CB-A98B917DD0EE
api_name:
- IObjectTableRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2c9108708475b27a7a1882051c7f0177e14470f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746725"
---
# <a name="span-idvspixengineiobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dwordspaniobjecttablerequestrequestasync-method"></a><span data-ttu-id="1b232-103"><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>IObjectTableRequest :: RequestAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="1b232-103"><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>IObjectTableRequest::RequestAsync method</span></span>

<span data-ttu-id="1b232-104">Demande l’extraction des informations spécifiées à partir de la table des objets pour l’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="1b232-104">Requests to get specified information from the object table for the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b232-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b232-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  eventID,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IObjectTableCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="1b232-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b232-106">Parameters</span></span>

<span data-ttu-id="1b232-107">*1001* </span><span class="sxs-lookup"><span data-stu-id="1b232-107">*eventID* </span></span>  
<span data-ttu-id="1b232-108">Événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="1b232-108">The specified event.</span></span>

<span data-ttu-id="1b232-109">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="1b232-109">*numColumns* </span></span>  
<span data-ttu-id="1b232-110">Nombre de colonnes (champs) d’informations à récupérer.</span><span class="sxs-lookup"><span data-stu-id="1b232-110">The number of columns (fields) of information to get.</span></span>

<span data-ttu-id="1b232-111">*\_colonnes count1* </span><span class="sxs-lookup"><span data-stu-id="1b232-111">*count1\_columns* </span></span>  
<span data-ttu-id="1b232-112">Colonnes spécifiées (champs).</span><span class="sxs-lookup"><span data-stu-id="1b232-112">The specified columns (fields).</span></span>

<span data-ttu-id="1b232-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="1b232-113">*requestCallback* </span></span>  
<span data-ttu-id="1b232-114">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="1b232-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="1b232-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="1b232-115">*requestCookie* </span></span>  
<span data-ttu-id="1b232-116">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="1b232-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="1b232-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="1b232-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="1b232-118">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="1b232-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="1b232-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1b232-119">Return value</span></span>

<span data-ttu-id="1b232-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1b232-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b232-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1b232-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b232-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b232-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1b232-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b232-123">Header</span></span></p></td><td><span data-ttu-id="1b232-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1b232-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1b232-125"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b232-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1b232-126">**IObjectTableRequest**</span><span class="sxs-lookup"><span data-stu-id="1b232-126">**IObjectTableRequest**</span></span>](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
