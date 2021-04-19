---
description: 'La méthode GetPreroll récupère la quantité de données qui seront placées en file d’attente avant la position de début. Cette méthode implémente la méthode IMediaSeeking :: GetPreroll.'
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: Méthode CPosPassThru. GetPreroll (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e72d7c83c8cdb0fa08a4b395fd65c80edbe3fb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545550"
---
# <a name="cpospassthrugetpreroll-method"></a><span data-ttu-id="0e724-104">Méthode CPosPassThru. GetPreroll</span><span class="sxs-lookup"><span data-stu-id="0e724-104">CPosPassThru.GetPreroll method</span></span>

<span data-ttu-id="0e724-105">La `GetPreroll` méthode récupère la quantité de données qui seront placées en file d’attente avant la position de début.</span><span class="sxs-lookup"><span data-stu-id="0e724-105">The `GetPreroll` method retrieves the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="0e724-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .</span><span class="sxs-lookup"><span data-stu-id="0e724-106">This method implements the [**IMediaSeeking::GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e724-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e724-107">Syntax</span></span>


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="0e724-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e724-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e724-109">*pllPreroll*</span><span class="sxs-lookup"><span data-stu-id="0e724-109">*pllPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="0e724-110">Pointeur vers une variable qui reçoit le temps de préroll, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="0e724-110">Pointer to a variable that receives the preroll time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e724-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e724-111">Return value</span></span>

<span data-ttu-id="0e724-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="0e724-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e724-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e724-113">Requirements</span></span>



| <span data-ttu-id="0e724-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e724-114">Requirement</span></span> | <span data-ttu-id="0e724-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e724-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e724-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e724-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0e724-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e724-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0e724-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0e724-118">Library</span></span><br/> | <dl> <span data-ttu-id="0e724-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0e724-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e724-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e724-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e724-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="0e724-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




