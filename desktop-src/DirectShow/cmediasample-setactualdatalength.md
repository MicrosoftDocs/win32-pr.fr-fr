---
description: 'La méthode SetActualDataLength définit la longueur des données valides dans la mémoire tampon. Cette méthode implémente la méthode IMediaSample :: SetActualDataLength.'
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: Méthode CMediaSample. SetActualDataLength (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825b02f43195424f9ceb5ecd23c4dcf26727ef8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540348"
---
# <a name="cmediasamplesetactualdatalength-method"></a><span data-ttu-id="95447-104">Méthode CMediaSample. SetActualDataLength</span><span class="sxs-lookup"><span data-stu-id="95447-104">CMediaSample.SetActualDataLength method</span></span>

<span data-ttu-id="95447-105">La `SetActualDataLength` méthode définit la longueur des données valides dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="95447-105">The `SetActualDataLength` method sets the length of the valid data in the buffer.</span></span> <span data-ttu-id="95447-106">Cette méthode implémente la méthode [**IMediaSample :: SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) .</span><span class="sxs-lookup"><span data-stu-id="95447-106">This method implements the [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="95447-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95447-107">Syntax</span></span>


```C++
HRESULT SetActualDataLength(
   long lLen
);
```



## <a name="parameters"></a><span data-ttu-id="95447-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95447-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95447-109">*lLen*</span><span class="sxs-lookup"><span data-stu-id="95447-109">*lLen*</span></span> 
</dt> <dd>

<span data-ttu-id="95447-110">Longueur des données valides, en octets.</span><span class="sxs-lookup"><span data-stu-id="95447-110">Length of the valid data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95447-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95447-111">Return value</span></span>

<span data-ttu-id="95447-112">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="95447-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="95447-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="95447-113">Return code</span></span>                                                                                             | <span data-ttu-id="95447-114">Description</span><span class="sxs-lookup"><span data-stu-id="95447-114">Description</span></span>                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="95447-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="95447-115"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="95447-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="95447-116">Success.</span></span><br/>                                         |
| <dl> <span data-ttu-id="95447-117"><dt>**\_dépassement de \_ mémoire tampon VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95447-117"><dt>**VFW\_E\_BUFFER\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="95447-118">*lLen* est plus grand que la taille de la mémoire tampon allouée.</span><span class="sxs-lookup"><span data-stu-id="95447-118">*lLen* is larger than the allocated buffer size.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="95447-119">Notes</span><span class="sxs-lookup"><span data-stu-id="95447-119">Remarks</span></span>

<span data-ttu-id="95447-120">Cette méthode définit la variable de membre [**CMediaSample :: m \_ lActual**](cmediasample-m-lactual.md) .</span><span class="sxs-lookup"><span data-stu-id="95447-120">This method sets the [**CMediaSample::m\_lActual**](cmediasample-m-lactual.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="95447-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95447-121">Requirements</span></span>



| <span data-ttu-id="95447-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95447-122">Requirement</span></span> | <span data-ttu-id="95447-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="95447-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95447-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="95447-124">Header</span></span><br/>  | <dl> <span data-ttu-id="95447-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95447-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="95447-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="95447-126">Library</span></span><br/> | <dl> <span data-ttu-id="95447-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="95447-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95447-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95447-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95447-129">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="95447-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




