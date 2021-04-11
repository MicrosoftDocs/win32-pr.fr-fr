---
description: Rappel qui avertit l’hôte des résultats de la requête de l’historique des pixels.
MS-HAID: vspixengine.IPixelHistoryCallback\_ResultCallback\_DWORD\_PixelHistoryOperation\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1F7D0EA5-402A-49C4-A83E-91596AE9536B
api_name:
- IPixelHistoryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c43947148e2eb8139f3ad46157f19b1621a6c91e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317766"
---
# <a name="span-idvspixengineipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arrspanipixelhistorycallbackresultcallback-method"></a><span data-ttu-id="ce4da-103"><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback :: ResultCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="ce4da-103"><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback::ResultCallback method</span></span>

<span data-ttu-id="ce4da-104">Rappel qui avertit l’hôte des résultats de la requête de l’historique des pixels.</span><span class="sxs-lookup"><span data-stu-id="ce4da-104">A callback that notifies the host of pixel history request results.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce4da-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce4da-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD                    count,
   PixelHistoryOperation [] count0_pixelHistoryOperation
);
```

## <a name="parameters"></a><span data-ttu-id="ce4da-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce4da-106">Parameters</span></span>

<span data-ttu-id="ce4da-107">*saut* </span><span class="sxs-lookup"><span data-stu-id="ce4da-107">*count* </span></span>  
<span data-ttu-id="ce4da-108">Nombre de résultats.</span><span class="sxs-lookup"><span data-stu-id="ce4da-108">The number of results.</span></span>

<span data-ttu-id="ce4da-109">*count0 \_ pixelHistoryOperation* </span><span class="sxs-lookup"><span data-stu-id="ce4da-109">*count0\_pixelHistoryOperation* </span></span>  
<span data-ttu-id="ce4da-110">Résultats</span><span class="sxs-lookup"><span data-stu-id="ce4da-110">The results.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce4da-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce4da-111">Return value</span></span>

<span data-ttu-id="ce4da-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ce4da-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ce4da-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ce4da-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce4da-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce4da-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ce4da-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce4da-115">Header</span></span></p></td><td><span data-ttu-id="ce4da-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ce4da-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ce4da-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce4da-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ce4da-118">**IPixelHistoryCallback**</span><span class="sxs-lookup"><span data-stu-id="ce4da-118">**IPixelHistoryCallback**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback)

 

 
