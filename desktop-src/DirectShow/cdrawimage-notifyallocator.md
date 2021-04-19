---
description: La méthode NotifyAllocator informe l’objet CDrawImage si l’allocateur de la connexion est un objet CImageAllocator.
ms.assetid: cc1604e7-f755-4a7a-9294-6fd06bb434d4
title: Méthode CDrawImage. NotifyAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7bab7d1d00b70317a7cbb0b79f8a430a603a757
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525610"
---
# <a name="cdrawimagenotifyallocator-method"></a><span data-ttu-id="adef1-103">Méthode CDrawImage. NotifyAllocator</span><span class="sxs-lookup"><span data-stu-id="adef1-103">CDrawImage.NotifyAllocator method</span></span>

<span data-ttu-id="adef1-104">La `NotifyAllocator` méthode informe l’objet **CDrawImage** si l’allocateur de la connexion est un objet [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="adef1-104">The `NotifyAllocator` method informs the **CDrawImage** object whether the allocator for the connection is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="adef1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adef1-105">Syntax</span></span>


```C++
void NotifyAllocator(
   BOOL bUsingImageAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="adef1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="adef1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adef1-107">*bUsingImageAllocator*</span><span class="sxs-lookup"><span data-stu-id="adef1-107">*bUsingImageAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="adef1-108">Valeur booléenne qui indique le type d’allocateur utilisé.</span><span class="sxs-lookup"><span data-stu-id="adef1-108">Boolean value that indicates what kind of allocator is being used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adef1-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="adef1-109">Return value</span></span>

<span data-ttu-id="adef1-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="adef1-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="adef1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="adef1-111">Remarks</span></span>

<span data-ttu-id="adef1-112">Le filtre propriétaire doit appeler cette méthode une fois que les codes confidentiels ont accepté un allocateur.</span><span class="sxs-lookup"><span data-stu-id="adef1-112">The owning filter should call this method after the pins agree to an allocator.</span></span> <span data-ttu-id="adef1-113">Si le filtre sait que l’allocateur est un objet **CImageAllocator** , il doit appeler cette méthode avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="adef1-113">If the filter knows the allocator is a **CImageAllocator** object, it should call this method with the value **TRUE**.</span></span> <span data-ttu-id="adef1-114">(En général, le filtre ne le connaîtra que s’il est propriétaire de l’allocateur en question.) Sinon, elle doit appeler cette méthode avec la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="adef1-114">(Typically, the filter will know this only if it owns the allocator in question.) Otherwise, it should call this method with the value **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="adef1-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adef1-115">Requirements</span></span>



| <span data-ttu-id="adef1-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adef1-116">Requirement</span></span> | <span data-ttu-id="adef1-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="adef1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adef1-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="adef1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="adef1-119"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="adef1-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="adef1-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="adef1-120">Library</span></span><br/> | <dl> <span data-ttu-id="adef1-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="adef1-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adef1-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adef1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adef1-123">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="adef1-123">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="adef1-124">**CDrawImage ::D rawImage**</span><span class="sxs-lookup"><span data-stu-id="adef1-124">**CDrawImage::DrawImage**</span></span>](cdrawimage-drawimage.md)
</dt> </dl>

 

 




