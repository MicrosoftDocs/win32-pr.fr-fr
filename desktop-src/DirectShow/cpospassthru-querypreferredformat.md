---
description: 'La méthode QueryPreferredFormat récupère le format d’heure par défaut pour le flux. Cette méthode implémente la méthode IMediaSeeking :: QueryPreferredFormat.'
ms.assetid: 8637448f-6b53-4ec9-9671-43bc8b713668
title: Méthode CPosPassThru. QueryPreferredFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c22348a10e8b9e5f241e06252c025e2ec9593486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530964"
---
# <a name="cpospassthruquerypreferredformat-method"></a><span data-ttu-id="dd1a8-104">Méthode CPosPassThru. QueryPreferredFormat</span><span class="sxs-lookup"><span data-stu-id="dd1a8-104">CPosPassThru.QueryPreferredFormat method</span></span>

<span data-ttu-id="dd1a8-105">La `QueryPreferredFormat` méthode récupère le format d’heure par défaut pour le flux.</span><span class="sxs-lookup"><span data-stu-id="dd1a8-105">The `QueryPreferredFormat` method retrieves the preferred time format for the stream.</span></span> <span data-ttu-id="dd1a8-106">Cette méthode implémente la méthode [**IMediaSeeking :: QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) .</span><span class="sxs-lookup"><span data-stu-id="dd1a8-106">This method implements the [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd1a8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd1a8-107">Syntax</span></span>


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="dd1a8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd1a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd1a8-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="dd1a8-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="dd1a8-110">Pointeur vers une variable qui reçoit un GUID de format d’heure.</span><span class="sxs-lookup"><span data-stu-id="dd1a8-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd1a8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd1a8-111">Return value</span></span>

<span data-ttu-id="dd1a8-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="dd1a8-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd1a8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd1a8-113">Requirements</span></span>



| <span data-ttu-id="dd1a8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd1a8-114">Requirement</span></span> | <span data-ttu-id="dd1a8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd1a8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd1a8-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd1a8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dd1a8-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd1a8-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dd1a8-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dd1a8-118">Library</span></span><br/> | <dl> <span data-ttu-id="dd1a8-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dd1a8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd1a8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd1a8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd1a8-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="dd1a8-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="dd1a8-122">**GUID de format d’heure**</span><span class="sxs-lookup"><span data-stu-id="dd1a8-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




