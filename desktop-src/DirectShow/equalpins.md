---
description: La fonction EqualPins vérifie si deux broches se trouvent sur le même objet.
ms.assetid: b6a92cb6-f4a9-4a14-831c-3b123e4692c0
title: EqualPins, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EqualPins
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fdf499b494f41a0acc5cc446bc92deade61c045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525372"
---
# <a name="equalpins-function"></a><span data-ttu-id="ffa3a-103">EqualPins fonction)</span><span class="sxs-lookup"><span data-stu-id="ffa3a-103">EqualPins function</span></span>

<span data-ttu-id="ffa3a-104">La fonction EqualPins vérifie si deux broches se trouvent sur le même objet.</span><span class="sxs-lookup"><span data-stu-id="ffa3a-104">The EqualPins function checks if two pins are on the same object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffa3a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffa3a-105">Syntax</span></span>


```C++
BOOL EqualPins(
   IUnknown *pPin1,
   IUnknown *pPin2
);
```



## <a name="parameters"></a><span data-ttu-id="ffa3a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffa3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffa3a-107">*pPin1*</span><span class="sxs-lookup"><span data-stu-id="ffa3a-107">*pPin1*</span></span> 
</dt> <dd>

<span data-ttu-id="ffa3a-108">Pointeur vers une broche.</span><span class="sxs-lookup"><span data-stu-id="ffa3a-108">Pointer to one pin.</span></span>

</dd> <dt>

<span data-ttu-id="ffa3a-109">*pPin2*</span><span class="sxs-lookup"><span data-stu-id="ffa3a-109">*pPin2*</span></span> 
</dt> <dd>

<span data-ttu-id="ffa3a-110">Pointeur vers l’autre code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="ffa3a-110">Pointer to the other pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffa3a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ffa3a-111">Return value</span></span>

<span data-ttu-id="ffa3a-112">Retourne la **valeur true** si les deux codes confidentiels se trouvent sur le même objet, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ffa3a-112">Returns **TRUE** if both pins are on the same object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffa3a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffa3a-113">Requirements</span></span>



| <span data-ttu-id="ffa3a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffa3a-114">Requirement</span></span> | <span data-ttu-id="ffa3a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffa3a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa3a-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffa3a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ffa3a-117"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffa3a-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ffa3a-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ffa3a-118">Library</span></span><br/> | <dl> <span data-ttu-id="ffa3a-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ffa3a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffa3a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffa3a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa3a-121">Fonctions d’assistance diverses</span><span class="sxs-lookup"><span data-stu-id="ffa3a-121">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




