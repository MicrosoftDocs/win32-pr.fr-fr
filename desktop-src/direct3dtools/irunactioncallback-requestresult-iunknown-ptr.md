---
description: Fonction de rappel utilisée pour informer l’hôte de résultats d’une action (par exemple, capturer un frame) qu’elle a demandée.
MS-HAID: vspixengine.IRunActionCallback\_RequestResult\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IRunActionCallback :: RequestResult, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5D6B1599-2CF4-46E7-92DB-5D93DD5AD0EE
api_name:
- IRunActionCallback.RequestResult
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8f2d5eea98b167af30bfe0412acb10f83f83d3db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109743"
---
# <a name="span-idvspixengineirunactioncallback_requestresult_iunknown_ptrspanirunactioncallbackrequestresult-method"></a><span data-ttu-id="54713-103"><span id="vspixengine.irunactioncallback_requestresult_iunknown_ptr"></span>IRunActionCallback :: RequestResult, méthode</span><span class="sxs-lookup"><span data-stu-id="54713-103"><span id="vspixengine.irunactioncallback_requestresult_iunknown_ptr"></span>IRunActionCallback::RequestResult method</span></span>

<span data-ttu-id="54713-104">Fonction de rappel utilisée pour informer l’hôte de résultats d’une action (par exemple, capturer un frame) qu’elle a demandée.</span><span class="sxs-lookup"><span data-stu-id="54713-104">A callback function used to notify the host of results from an action (for example, capture a frame) that it requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="54713-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54713-105">Syntax</span></span>


```C++
HRESULT RequestResult(
   IUnknown * actionResult
);
```

## <a name="parameters"></a><span data-ttu-id="54713-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54713-106">Parameters</span></span>

<span data-ttu-id="54713-107">*actionResult* </span><span class="sxs-lookup"><span data-stu-id="54713-107">*actionResult* </span></span>  
<span data-ttu-id="54713-108">Résultat de l’action.</span><span class="sxs-lookup"><span data-stu-id="54713-108">The result of the action.</span></span>

## <a name="return-value"></a><span data-ttu-id="54713-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54713-109">Return value</span></span>

<span data-ttu-id="54713-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="54713-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="54713-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="54713-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="54713-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54713-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="54713-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="54713-113">Header</span></span></p></td><td><span data-ttu-id="54713-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="54713-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="54713-115"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54713-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="54713-116">**IRunActionCallback**</span><span class="sxs-lookup"><span data-stu-id="54713-116">**IRunActionCallback**</span></span>](/windows/desktop/direct3dtools/irunactioncallback)

 

 
