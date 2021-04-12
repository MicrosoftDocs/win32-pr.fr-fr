---
description: Demandes d’obtenir le contenu brut d’un objet (mémoire tampon, texture, vue de la cible de rendu, etc.).
MS-HAID: vspixengine.IBufferObjectDataRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_BSTR\_IBufferObjectDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IBufferObjectDataRequest :: RequestAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 899954DC-6196-4F79-AFB4-5E692DAA03EC
api_name:
- IBufferObjectDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 97d35f656f373f2f0040d49a78a2c0d376bc4266
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108947"
---
# <a name="span-idvspixengineibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dwordspanibufferobjectdatarequestrequestasync-method"></a><span data-ttu-id="55e4e-103"><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>IBufferObjectDataRequest :: RequestAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="55e4e-103"><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>IBufferObjectDataRequest::RequestAsync method</span></span>

<span data-ttu-id="55e4e-104">Demandes d’obtenir le contenu brut d’un objet (mémoire tampon, texture, vue de la cible de rendu, etc.)</span><span class="sxs-lookup"><span data-stu-id="55e4e-104">Requests to get the raw contents of an object (buffer, texture, render target view, etc.)</span></span>

## <a name="syntax"></a><span data-ttu-id="55e4e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55e4e-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   BSTR                        Format,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="55e4e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55e4e-106">Parameters</span></span>

<span data-ttu-id="55e4e-107">*1001* </span><span class="sxs-lookup"><span data-stu-id="55e4e-107">*eventID* </span></span>  
<span data-ttu-id="55e4e-108">Événement spécifié pour faire correspondre le contenu de la mémoire tampon à (par exemple, une cible de rendu peut changer au fil du temps).</span><span class="sxs-lookup"><span data-stu-id="55e4e-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="55e4e-109">*RequestedDataUID* </span><span class="sxs-lookup"><span data-stu-id="55e4e-109">*RequestedDataUID* </span></span>  
<span data-ttu-id="55e4e-110">Adresse de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="55e4e-110">The address of the specified object.</span></span>

<span data-ttu-id="55e4e-111">*Txt* </span><span class="sxs-lookup"><span data-stu-id="55e4e-111">*File* </span></span>  
<span data-ttu-id="55e4e-112">Chaîne COM qui contient le nom du chemin d’accès du fichier dans lequel les résultats sont écrits.</span><span class="sxs-lookup"><span data-stu-id="55e4e-112">A COM string that contains the pathname of the file where results are written.</span></span>

<span data-ttu-id="55e4e-113">*Format* </span><span class="sxs-lookup"><span data-stu-id="55e4e-113">*Format* </span></span>  
<span data-ttu-id="55e4e-114">Pas utilisé pour l'instant.</span><span class="sxs-lookup"><span data-stu-id="55e4e-114">Not currently used.</span></span> <span data-ttu-id="55e4e-115">Chaîne COM qui spécifie le format de sortie.</span><span class="sxs-lookup"><span data-stu-id="55e4e-115">A COM string that specifies the output format.</span></span>

<span data-ttu-id="55e4e-116">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="55e4e-116">*requestCallback* </span></span>  
<span data-ttu-id="55e4e-117">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="55e4e-117">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="55e4e-118">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="55e4e-118">*requestCookie* </span></span>  
<span data-ttu-id="55e4e-119">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="55e4e-119">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="55e4e-120">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="55e4e-120">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="55e4e-121">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="55e4e-121">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="55e4e-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="55e4e-122">Return value</span></span>

<span data-ttu-id="55e4e-123">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="55e4e-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="55e4e-124">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="55e4e-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="55e4e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55e4e-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="55e4e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="55e4e-126">Header</span></span></p></td><td><span data-ttu-id="55e4e-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="55e4e-127">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="55e4e-128"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55e4e-128"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="55e4e-129">**IBufferObjectDataRequest**</span><span class="sxs-lookup"><span data-stu-id="55e4e-129">**IBufferObjectDataRequest**</span></span>](/windows/desktop/direct3dtools/ibufferobjectdatarequest)

 

 
