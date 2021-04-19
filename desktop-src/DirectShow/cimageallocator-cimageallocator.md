---
description: Méthode de constructeur.
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: Constructeur CImageAllocator. CImageAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5f6873e8cc073e0b716f94c980ecceba8f4512f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543824"
---
# <a name="cimageallocatorcimageallocator-constructor"></a><span data-ttu-id="ad0d0-103">Constructeur CImageAllocator. CImageAllocator</span><span class="sxs-lookup"><span data-stu-id="ad0d0-103">CImageAllocator.CImageAllocator constructor</span></span>

<span data-ttu-id="ad0d0-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="ad0d0-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad0d0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad0d0-105">Syntax</span></span>


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="ad0d0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad0d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad0d0-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="ad0d0-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="ad0d0-108">Pointeur désignant le filtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="ad0d0-108">Pointer to the owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="ad0d0-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="ad0d0-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ad0d0-110">Pointeur vers une chaîne contenant le nom de débogage de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="ad0d0-110">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="ad0d0-111">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="ad0d0-111">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad0d0-112">*phr*</span><span class="sxs-lookup"><span data-stu-id="ad0d0-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ad0d0-113">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ad0d0-113">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="ad0d0-114">Définissez la valeur sur \_ OK avant de créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="ad0d0-114">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="ad0d0-115">Si le constructeur échoue, la valeur est définie sur un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ad0d0-115">If the constructor fails, the value is set to an error code.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad0d0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad0d0-116">Requirements</span></span>



| <span data-ttu-id="ad0d0-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad0d0-117">Requirement</span></span> | <span data-ttu-id="ad0d0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad0d0-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad0d0-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad0d0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ad0d0-120"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad0d0-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ad0d0-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ad0d0-121">Library</span></span><br/> | <dl> <span data-ttu-id="ad0d0-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ad0d0-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad0d0-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad0d0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad0d0-124">**CImageAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="ad0d0-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




