---
description: La méthode SetTemporalCompression spécifie si les échantillons sont compressés à l’aide de la compression temporelle (intertrame).
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: Méthode CMediaType. SetTemporalCompression (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetTemporalCompression
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0aba07375c5b5c760c432de704562efb2bea148
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540484"
---
# <a name="cmediatypesettemporalcompression-method"></a><span data-ttu-id="b34cc-103">Méthode CMediaType. SetTemporalCompression</span><span class="sxs-lookup"><span data-stu-id="b34cc-103">CMediaType.SetTemporalCompression method</span></span>

<span data-ttu-id="b34cc-104">La `SetTemporalCompression` méthode spécifie si les échantillons sont compressés à l’aide de la compression temporelle (intertrame).</span><span class="sxs-lookup"><span data-stu-id="b34cc-104">The `SetTemporalCompression` method specifies whether samples are compressed using temporal (interframe) compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="b34cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b34cc-105">Syntax</span></span>


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a><span data-ttu-id="b34cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b34cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b34cc-107">*bCompressed*</span><span class="sxs-lookup"><span data-stu-id="b34cc-107">*bCompressed*</span></span> 
</dt> <dd>

<span data-ttu-id="b34cc-108">Valeur booléenne qui spécifie si le flux utilise la compression temporelle.</span><span class="sxs-lookup"><span data-stu-id="b34cc-108">Boolean value that specifies whether the stream uses temporal compression.</span></span> <span data-ttu-id="b34cc-109">Si le flux utilise la compression temporelle, définissez la valeur sur **true**.</span><span class="sxs-lookup"><span data-stu-id="b34cc-109">If the stream uses temporal compression, set the value to **TRUE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b34cc-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b34cc-110">Return value</span></span>

<span data-ttu-id="b34cc-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b34cc-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b34cc-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b34cc-112">Remarks</span></span>

<span data-ttu-id="b34cc-113">Cette méthode définit le membre **bTemporalCompression** .</span><span class="sxs-lookup"><span data-stu-id="b34cc-113">This method sets the **bTemporalCompression** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="b34cc-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b34cc-114">Requirements</span></span>



| <span data-ttu-id="b34cc-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b34cc-115">Requirement</span></span> | <span data-ttu-id="b34cc-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b34cc-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b34cc-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="b34cc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b34cc-118"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b34cc-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="b34cc-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b34cc-119">Library</span></span><br/> | <dl> <span data-ttu-id="b34cc-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b34cc-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b34cc-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b34cc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b34cc-122">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="b34cc-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




