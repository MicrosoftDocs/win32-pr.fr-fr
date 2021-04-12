---
description: Demande d’obtenir le contenu d’une texture sous la forme d’un. Fichier DDS (surface DirectDraw).
MS-HAID: vspixengine.ITextureRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ITextureRequest :: RequestAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 89A9F230-D296-43CD-A2A6-747057750EED
api_name:
- ITextureRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5abfee1b26fd2145aef8e01239cc0b874ee54e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482568"
---
# <a name="span-idvspixengineitexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dwordspanitexturerequestrequestasync-method"></a><span data-ttu-id="c3916-103"><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>ITextureRequest :: RequestAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="c3916-103"><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>ITextureRequest::RequestAsync method</span></span>

<span data-ttu-id="c3916-104">Demande d’obtenir le contenu d’une texture sous la forme d’un. Fichier DDS (surface DirectDraw).</span><span class="sxs-lookup"><span data-stu-id="c3916-104">Requests to get the contents of a texture as a .DDS (DirectDraw Surface) file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3916-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3916-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="c3916-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3916-106">Parameters</span></span>

<span data-ttu-id="c3916-107">*1001* </span><span class="sxs-lookup"><span data-stu-id="c3916-107">*eventID* </span></span>  
<span data-ttu-id="c3916-108">Événement spécifié pour faire correspondre le contenu de la mémoire tampon à (par exemple, une cible de rendu peut changer au fil du temps).</span><span class="sxs-lookup"><span data-stu-id="c3916-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="c3916-109">*textureFileptr* </span><span class="sxs-lookup"><span data-stu-id="c3916-109">*textureFileptr* </span></span>  
<span data-ttu-id="c3916-110">Adresse de l’objet de texture.</span><span class="sxs-lookup"><span data-stu-id="c3916-110">The address of the texture object.</span></span>

<span data-ttu-id="c3916-111">*ddsFilename* </span><span class="sxs-lookup"><span data-stu-id="c3916-111">*ddsFilename* </span></span>  
<span data-ttu-id="c3916-112">Chaîne COM qui contient le chemin d’accès du fichier. DDS dans lequel les résultats sont écrits.</span><span class="sxs-lookup"><span data-stu-id="c3916-112">A COM string that contains the pathname of the .dds file where results are written.</span></span>

<span data-ttu-id="c3916-113">*pRequestCallback* </span><span class="sxs-lookup"><span data-stu-id="c3916-113">*pRequestCallback* </span></span>  
<span data-ttu-id="c3916-114">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="c3916-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="c3916-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="c3916-115">*requestCookie* </span></span>  
<span data-ttu-id="c3916-116">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="c3916-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="c3916-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="c3916-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="c3916-118">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="c3916-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3916-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3916-119">Return value</span></span>

<span data-ttu-id="c3916-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c3916-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c3916-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c3916-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3916-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3916-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c3916-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3916-123">Header</span></span></p></td><td><span data-ttu-id="c3916-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c3916-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c3916-125"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3916-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c3916-126">**ITextureRequest**</span><span class="sxs-lookup"><span data-stu-id="c3916-126">**ITextureRequest**</span></span>](/windows/desktop/direct3dtools/itexturerequest)

 

 
