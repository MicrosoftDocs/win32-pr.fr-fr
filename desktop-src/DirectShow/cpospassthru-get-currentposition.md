---
description: 'La \_ méthode obtenir CurrentPosition récupère la position actuelle, par rapport à la durée totale du flux. Cette méthode implémente la méthode IMediaPosition :: obten \_ CurrentPosition.'
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: Méthode CPosPassThru.get_CurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c146eb1ee3d0a48da90973ab181a4bd02182331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525229"
---
# <a name="cpospassthruget_currentposition-method"></a><span data-ttu-id="bfdbc-104">Méthode CPosPassThru. obten \_ CurrentPosition</span><span class="sxs-lookup"><span data-stu-id="bfdbc-104">CPosPassThru.get\_CurrentPosition method</span></span>

<span data-ttu-id="bfdbc-105">La `get_CurrentPosition` méthode récupère la position actuelle, par rapport à la durée totale du flux.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-105">The `get_CurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="bfdbc-106">Cette méthode implémente la méthode [**IMediaPosition :: obten \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) .</span><span class="sxs-lookup"><span data-stu-id="bfdbc-106">This method implements the [**IMediaPosition::get\_CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfdbc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfdbc-107">Syntax</span></span>


```C++
HRESULT get_CurrentPosition(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="bfdbc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfdbc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfdbc-109">*pllTime*</span><span class="sxs-lookup"><span data-stu-id="bfdbc-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="bfdbc-110">Pointeur vers une variable qui reçoit la position actuelle, en secondes.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-110">Pointer to a variable that receives the current position, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfdbc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bfdbc-111">Return value</span></span>

<span data-ttu-id="bfdbc-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="bfdbc-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfdbc-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfdbc-113">Requirements</span></span>



| <span data-ttu-id="bfdbc-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfdbc-114">Requirement</span></span> | <span data-ttu-id="bfdbc-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfdbc-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfdbc-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="bfdbc-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bfdbc-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfdbc-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bfdbc-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bfdbc-118">Library</span></span><br/> | <dl> <span data-ttu-id="bfdbc-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bfdbc-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfdbc-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfdbc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfdbc-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="bfdbc-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




