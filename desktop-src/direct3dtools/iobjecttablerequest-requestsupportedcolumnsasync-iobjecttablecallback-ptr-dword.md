---
description: Demandes pour obtenir des informations sur les colonnes (champs) prises en charge par ce type de demande de table d’objets.
MS-HAID: vspixengine.IObjectTableRequest\_RequestSupportedColumnsAsync\_IObjectTableCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IObjectTableRequest :: RequestSupportedColumnsAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0931C81A-65D5-493E-9F54-C7E98FA2FA6F
api_name:
- IObjectTableRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6773a69061e7a17d2271e1a53f89f6f2def1a6c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522748"
---
# <a name="span-idvspixengineiobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dwordspaniobjecttablerequestrequestsupportedcolumnsasync-method"></a><span data-ttu-id="92387-103"><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>IObjectTableRequest :: RequestSupportedColumnsAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="92387-103"><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>IObjectTableRequest::RequestSupportedColumnsAsync method</span></span>

<span data-ttu-id="92387-104">Demandes pour obtenir des informations sur les colonnes (champs) prises en charge par ce type de demande de table d’objets.</span><span class="sxs-lookup"><span data-stu-id="92387-104">Requests to get information about what columns (fields) this object table request type supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="92387-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92387-105">Syntax</span></span>


```C++
HRESULT RequestSupportedColumnsAsync(
   IObjectTableCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="92387-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92387-106">Parameters</span></span>

<span data-ttu-id="92387-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="92387-107">*requestCallback* </span></span>  
<span data-ttu-id="92387-108">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="92387-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="92387-109">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="92387-109">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="92387-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="92387-110">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="92387-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92387-111">Return value</span></span>

<span data-ttu-id="92387-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="92387-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="92387-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="92387-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="92387-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92387-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="92387-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="92387-115">Header</span></span></p></td><td><span data-ttu-id="92387-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="92387-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="92387-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92387-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="92387-118">**IObjectTableRequest**</span><span class="sxs-lookup"><span data-stu-id="92387-118">**IObjectTableRequest**</span></span>](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
