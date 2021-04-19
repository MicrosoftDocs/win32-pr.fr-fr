---
description: 'La méthode Skip ignore un nombre spécifié de types de médias. Cette méthode implémente la méthode IEnumMediaTypes :: Skip.'
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: CEnumMediaTypes. Skip, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e09217bc45b866cfb08aa2ab0cae5a7a28815fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535289"
---
# <a name="cenummediatypesskip-method"></a><span data-ttu-id="e8e87-104">CEnumMediaTypes. Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="e8e87-104">CEnumMediaTypes.Skip method</span></span>

<span data-ttu-id="e8e87-105">La `Skip` méthode ignore un nombre spécifié de types de médias.</span><span class="sxs-lookup"><span data-stu-id="e8e87-105">The `Skip` method skips over a specified number of media types.</span></span> <span data-ttu-id="e8e87-106">Cette méthode implémente la méthode [**IEnumMediaTypes :: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) .</span><span class="sxs-lookup"><span data-stu-id="e8e87-106">This method implements the [**IEnumMediaTypes::Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e87-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8e87-107">Syntax</span></span>


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="e8e87-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8e87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8e87-109">*cMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="e8e87-109">*cMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e87-110">Nombre de types de médias à ignorer.</span><span class="sxs-lookup"><span data-stu-id="e8e87-110">Number of media types to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8e87-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e8e87-111">Return value</span></span>

<span data-ttu-id="e8e87-112">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e8e87-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="e8e87-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e8e87-113">Return code</span></span>                                                                                                | <span data-ttu-id="e8e87-114">Description</span><span class="sxs-lookup"><span data-stu-id="e8e87-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e8e87-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e8e87-115"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="e8e87-116">Ignorée au-delà de la fin de la séquence.</span><span class="sxs-lookup"><span data-stu-id="e8e87-116">Skipped past the end of the sequence.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e8e87-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e8e87-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="e8e87-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e8e87-118">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="e8e87-119"><dt>**VFW \_ E \_ enum \_ non \_ \_ synchronisé**</dt></span><span class="sxs-lookup"><span data-stu-id="e8e87-119"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="e8e87-120">L’état du pin a changé et est désormais incohérent avec l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="e8e87-120">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e8e87-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8e87-121">Requirements</span></span>



| <span data-ttu-id="e8e87-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8e87-122">Requirement</span></span> | <span data-ttu-id="e8e87-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8e87-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e87-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8e87-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e8e87-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8e87-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e8e87-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e8e87-126">Library</span></span><br/> | <dl> <span data-ttu-id="e8e87-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e8e87-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8e87-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8e87-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e87-129">**CEnumMediaTypes, classe**</span><span class="sxs-lookup"><span data-stu-id="e8e87-129">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




