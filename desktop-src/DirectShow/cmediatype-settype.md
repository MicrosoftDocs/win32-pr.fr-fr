---
description: La méthode SetType spécifie le type principal.
ms.assetid: 3fd93d5e-73ea-453e-8f08-652d5a81239f
title: Méthode CMediaType. SetType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfcf6ca634bce92701eb89f26dcfb6bdfb51f698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533206"
---
# <a name="cmediatypesettype-method"></a><span data-ttu-id="35f32-103">Méthode CMediaType. SetType</span><span class="sxs-lookup"><span data-stu-id="35f32-103">CMediaType.SetType method</span></span>

<span data-ttu-id="35f32-104">La `SetType` méthode spécifie le type principal.</span><span class="sxs-lookup"><span data-stu-id="35f32-104">The `SetType` method specifies the major type.</span></span>

## <a name="syntax"></a><span data-ttu-id="35f32-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35f32-105">Syntax</span></span>


```C++
void SetType(
   const GUID *ptype
);
```



## <a name="parameters"></a><span data-ttu-id="35f32-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35f32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35f32-107">*ptype*</span><span class="sxs-lookup"><span data-stu-id="35f32-107">*ptype*</span></span> 
</dt> <dd>

<span data-ttu-id="35f32-108">Pointeur vers un **GUID** qui spécifie le type principal.</span><span class="sxs-lookup"><span data-stu-id="35f32-108">Pointer to a **GUID** that specifies the major type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35f32-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35f32-109">Return value</span></span>

<span data-ttu-id="35f32-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="35f32-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="35f32-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35f32-111">Requirements</span></span>



| <span data-ttu-id="35f32-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35f32-112">Requirement</span></span> | <span data-ttu-id="35f32-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="35f32-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35f32-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="35f32-114">Header</span></span><br/>  | <dl> <span data-ttu-id="35f32-115"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35f32-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="35f32-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="35f32-116">Library</span></span><br/> | <dl> <span data-ttu-id="35f32-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="35f32-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35f32-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35f32-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35f32-119">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="35f32-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




