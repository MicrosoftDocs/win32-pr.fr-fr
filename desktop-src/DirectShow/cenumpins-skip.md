---
description: 'La méthode Skip ignore un nombre spécifié de codes confidentiels dans la séquence d’énumération. Cette méthode implémente la méthode IEnumPins :: Skip.'
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: CEnumPins. Skip, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1865453a89130303f28f338d8b7567e856c64173
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539938"
---
# <a name="cenumpinsskip-method"></a><span data-ttu-id="4ab29-104">CEnumPins. Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="4ab29-104">CEnumPins.Skip method</span></span>

<span data-ttu-id="4ab29-105">La `Skip` méthode ignore un nombre spécifié de codes confidentiels dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="4ab29-105">The `Skip` method skips over a specified number of pins in the enumeration sequence.</span></span> <span data-ttu-id="4ab29-106">Cette méthode implémente la méthode [**IEnumPins :: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) .</span><span class="sxs-lookup"><span data-stu-id="4ab29-106">This method implements the [**IEnumPins::Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ab29-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ab29-107">Syntax</span></span>


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a><span data-ttu-id="4ab29-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ab29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ab29-109">*cPins*</span><span class="sxs-lookup"><span data-stu-id="4ab29-109">*cPins*</span></span> 
</dt> <dd>

<span data-ttu-id="4ab29-110">Nombre de broches à ignorer.</span><span class="sxs-lookup"><span data-stu-id="4ab29-110">Number of pins to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ab29-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4ab29-111">Return value</span></span>

<span data-ttu-id="4ab29-112">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4ab29-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="4ab29-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4ab29-113">Return code</span></span>                                                                                                | <span data-ttu-id="4ab29-114">Description</span><span class="sxs-lookup"><span data-stu-id="4ab29-114">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4ab29-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4ab29-115"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="4ab29-116">Ignorée au-delà de la fin de la séquence.</span><span class="sxs-lookup"><span data-stu-id="4ab29-116">Skipped past the end of the sequence.</span></span><br/>                                       |
| <dl> <span data-ttu-id="4ab29-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4ab29-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="4ab29-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="4ab29-118">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="4ab29-119"><dt>**VFW \_ E \_ enum \_ non \_ \_ synchronisé**</dt></span><span class="sxs-lookup"><span data-stu-id="4ab29-119"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="4ab29-120">L’état du filtre a changé et est désormais incohérent avec l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="4ab29-120">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4ab29-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ab29-121">Requirements</span></span>



| <span data-ttu-id="4ab29-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ab29-122">Requirement</span></span> | <span data-ttu-id="4ab29-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ab29-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ab29-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ab29-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4ab29-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ab29-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4ab29-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4ab29-126">Library</span></span><br/> | <dl> <span data-ttu-id="4ab29-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4ab29-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ab29-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ab29-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ab29-129">**CEnumPins, classe**</span><span class="sxs-lookup"><span data-stu-id="4ab29-129">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




