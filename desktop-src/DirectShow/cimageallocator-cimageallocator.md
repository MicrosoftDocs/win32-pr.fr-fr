---
description: Méthode constructeur CImageAllocator. CImageAllocator.
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
ms.openlocfilehash: f17ae78b668f6cc35e454c5e4e83d38727077ef7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085757"
---
# <a name="cimageallocatorcimageallocator-constructor"></a><span data-ttu-id="19479-103">Constructeur CImageAllocator. CImageAllocator</span><span class="sxs-lookup"><span data-stu-id="19479-103">CImageAllocator.CImageAllocator constructor</span></span>

<span data-ttu-id="19479-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="19479-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="19479-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19479-105">Syntax</span></span>


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="19479-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19479-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19479-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="19479-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="19479-108">Pointeur désignant le filtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="19479-108">Pointer to the owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="19479-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="19479-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="19479-110">Pointeur vers une chaîne contenant le nom de débogage de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="19479-110">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="19479-111">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="19479-111">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="19479-112">*phr*</span><span class="sxs-lookup"><span data-stu-id="19479-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="19479-113">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="19479-113">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="19479-114">Définissez la valeur sur \_ OK avant de créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="19479-114">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="19479-115">Si le constructeur échoue, la valeur est définie sur un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="19479-115">If the constructor fails, the value is set to an error code.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19479-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19479-116">Requirements</span></span>



| <span data-ttu-id="19479-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19479-117">Requirement</span></span> | <span data-ttu-id="19479-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="19479-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19479-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="19479-119">Header</span></span><br/>  | <dl> <span data-ttu-id="19479-120"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19479-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="19479-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="19479-121">Library</span></span><br/> | <dl> <span data-ttu-id="19479-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="19479-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19479-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19479-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19479-124">**CImageAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="19479-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




