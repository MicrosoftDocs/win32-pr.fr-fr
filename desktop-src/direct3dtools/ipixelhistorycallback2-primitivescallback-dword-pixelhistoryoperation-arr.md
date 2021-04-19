---
description: Rappel qui avertit l’hôte des informations d’opération primitives de l’historique des pixels retournées par la requête associée.
MS-HAID: vspixengine.IPixelHistoryCallback2\_PrimitivesCallback\_DWORD\_PixelHistoryOperation\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixelHistoryCallback2 ::P méthode rimitivesCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2A67EC3B-72F2-4347-AD23-961CDE0D456F
api_name:
- IPixelHistoryCallback2.PrimitivesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8512bde1acd96ebbe132eeb91872d04ce043b44f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522359"
---
# <a name="span-idvspixengineipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arrspanipixelhistorycallback2primitivescallback-method"></a><span data-ttu-id="65227-103"><span id="vspixengine.ipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback2 ::P méthode rimitivesCallback</span><span class="sxs-lookup"><span data-stu-id="65227-103"><span id="vspixengine.ipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback2::PrimitivesCallback method</span></span>

<span data-ttu-id="65227-104">Rappel qui avertit l’hôte des informations d’opération primitives de l’historique des pixels retournées par la requête associée.</span><span class="sxs-lookup"><span data-stu-id="65227-104">A callback that notifies the host of pixel history primitive operation information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="65227-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65227-105">Syntax</span></span>


```C++
HRESULT PrimitivesCallback(
   DWORD                    count,
   PixelHistoryOperation [] count0_primitives
);
```

## <a name="parameters"></a><span data-ttu-id="65227-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65227-106">Parameters</span></span>

<span data-ttu-id="65227-107">*saut* </span><span class="sxs-lookup"><span data-stu-id="65227-107">*count* </span></span>  
<span data-ttu-id="65227-108">Nombre de Primitives.</span><span class="sxs-lookup"><span data-stu-id="65227-108">The number of primitives.</span></span>

<span data-ttu-id="65227-109">*\_primitives count0* </span><span class="sxs-lookup"><span data-stu-id="65227-109">*count0\_primitives* </span></span>  
<span data-ttu-id="65227-110">Primitives.</span><span class="sxs-lookup"><span data-stu-id="65227-110">The primitives.</span></span>

## <a name="return-value"></a><span data-ttu-id="65227-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65227-111">Return value</span></span>

<span data-ttu-id="65227-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="65227-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65227-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="65227-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="65227-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65227-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="65227-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="65227-115">Header</span></span></p></td><td><span data-ttu-id="65227-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="65227-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="65227-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65227-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="65227-118">**IPixelHistoryCallback2**</span><span class="sxs-lookup"><span data-stu-id="65227-118">**IPixelHistoryCallback2**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback2)

 

 
