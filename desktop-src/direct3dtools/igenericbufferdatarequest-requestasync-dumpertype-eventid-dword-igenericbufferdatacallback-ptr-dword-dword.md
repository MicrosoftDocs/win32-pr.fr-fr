---
description: Demande de retourner des données d’objet générique qui décrivent un objet dans le fichier. vsglog pour l’événement spécifié et dans le format spécifié.
MS-HAID: vspixengine.IGenericBufferDataRequest\_RequestAsync\_DumperType\_EventID\_DWORD\_IGenericBufferDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IGenericBufferDataRequest :: RequestAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 542E20F9-B91D-4A05-AEE8-9DD2E80B76DB
api_name:
- IGenericBufferDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6d8860b2de7c3dce5c6f8b61467bfe147530ed76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513297"
---
# <a name="span-idvspixengineigenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dwordspanigenericbufferdatarequestrequestasync-method"></a><span data-ttu-id="27a4b-103"><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>IGenericBufferDataRequest :: RequestAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="27a4b-103"><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>IGenericBufferDataRequest::RequestAsync method</span></span>

<span data-ttu-id="27a4b-104">Demande de retourner des données d’objet générique qui décrivent un objet dans le fichier. vsglog pour l’événement spécifié et dans le format spécifié.</span><span class="sxs-lookup"><span data-stu-id="27a4b-104">Requests to return generic object data that describes an object in the .vsglog file for the specified event and in the specified format.</span></span>

## <a name="syntax"></a><span data-ttu-id="27a4b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27a4b-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DumperType                   dumperType,
   EventID                      eventID,
   DWORD                        RequestedDataUID,
   IGenericBufferDataCallback * requestCallback,
   DWORD                        requestCookie,
   DWORD                        progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="27a4b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27a4b-106">Parameters</span></span>

<span data-ttu-id="27a4b-107">*dumperType* </span><span class="sxs-lookup"><span data-stu-id="27a4b-107">*dumperType* </span></span>  
<span data-ttu-id="27a4b-108">Format spécifié de la représentation textuelle de l’objet (HTML, XML, etc.)</span><span class="sxs-lookup"><span data-stu-id="27a4b-108">The specified format of the textual representation of the object (HTML, XML, etc.)</span></span>

<span data-ttu-id="27a4b-109">*1001* </span><span class="sxs-lookup"><span data-stu-id="27a4b-109">*eventID* </span></span>  
<span data-ttu-id="27a4b-110">Événement spécifié pour faire correspondre le contenu de la mémoire tampon à (par exemple, une cible de rendu peut changer au fil du temps).</span><span class="sxs-lookup"><span data-stu-id="27a4b-110">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="27a4b-111">*RequestedDataUID* </span><span class="sxs-lookup"><span data-stu-id="27a4b-111">*RequestedDataUID* </span></span>  
<span data-ttu-id="27a4b-112">Adresse de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="27a4b-112">The address of the specified object.</span></span>

<span data-ttu-id="27a4b-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="27a4b-113">*requestCallback* </span></span>  
<span data-ttu-id="27a4b-114">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="27a4b-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="27a4b-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="27a4b-115">*requestCookie* </span></span>  
<span data-ttu-id="27a4b-116">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="27a4b-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="27a4b-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="27a4b-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="27a4b-118">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="27a4b-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="27a4b-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="27a4b-119">Return value</span></span>

<span data-ttu-id="27a4b-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="27a4b-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27a4b-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="27a4b-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="27a4b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27a4b-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="27a4b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="27a4b-123">Header</span></span></p></td><td><span data-ttu-id="27a4b-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="27a4b-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="27a4b-125"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27a4b-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="27a4b-126">**IGenericBufferDataRequest**</span><span class="sxs-lookup"><span data-stu-id="27a4b-126">**IGenericBufferDataRequest**</span></span>](/windows/desktop/direct3dtools/igenericbufferdatarequest)

 

 
