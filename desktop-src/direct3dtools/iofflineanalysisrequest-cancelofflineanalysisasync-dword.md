---
description: Demandes d’annulation de l’analyse hors connexion dans une demande d’analyse hors connexion.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_CancelOfflineAnalysisAsync\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IOfflineAnalysisRequest :: CancelOfflineAnalysisAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 20107890-DF7B-4483-9D2C-1D9164366504
api_name:
- IOfflineAnalysisRequest.CancelOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 79329d27aff74efb7d08c7cc182ddb6e21f96cba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481497"
---
# <a name="span-idvspixengineiofflineanalysisrequest_cancelofflineanalysisasync_dwordspaniofflineanalysisrequestcancelofflineanalysisasync-method"></a><span data-ttu-id="a9dcf-103"><span id="vspixengine.iofflineanalysisrequest_cancelofflineanalysisasync_dword"></span>IOfflineAnalysisRequest :: CancelOfflineAnalysisAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="a9dcf-103"><span id="vspixengine.iofflineanalysisrequest_cancelofflineanalysisasync_dword"></span>IOfflineAnalysisRequest::CancelOfflineAnalysisAsync method</span></span>

<span data-ttu-id="a9dcf-104">Demandes d’annulation de l’analyse hors connexion dans une demande d’analyse hors connexion.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-104">Requests to cancel offline analysis in an offline analysis request.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9dcf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9dcf-105">Syntax</span></span>


```C++
HRESULT CancelOfflineAnalysisAsync(
   DWORD cookie
);
```

## <a name="parameters"></a><span data-ttu-id="a9dcf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9dcf-106">Parameters</span></span>

<span data-ttu-id="a9dcf-107">*cookie* </span><span class="sxs-lookup"><span data-stu-id="a9dcf-107">*cookie* </span></span>  
<span data-ttu-id="a9dcf-108">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-108">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9dcf-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a9dcf-109">Return value</span></span>

<span data-ttu-id="a9dcf-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a9dcf-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a9dcf-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a9dcf-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9dcf-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9dcf-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a9dcf-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9dcf-113">Header</span></span></p></td><td><span data-ttu-id="a9dcf-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a9dcf-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a9dcf-115"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9dcf-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a9dcf-116">**IOfflineAnalysisRequest**</span><span class="sxs-lookup"><span data-stu-id="a9dcf-116">**IOfflineAnalysisRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
