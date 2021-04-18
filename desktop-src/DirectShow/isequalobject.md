---
description: La fonction IsEqualObject vérifie si deux interfaces se trouvent sur le même objet.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: IsEqualObject, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e959d687d7d6b11dc6055daeda789e728d875d70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540382"
---
# <a name="isequalobject-function"></a><span data-ttu-id="8b1e9-103">IsEqualObject fonction)</span><span class="sxs-lookup"><span data-stu-id="8b1e9-103">IsEqualObject function</span></span>

<span data-ttu-id="8b1e9-104">La `IsEqualObject` fonction vérifie si deux interfaces se trouvent sur le même objet.</span><span class="sxs-lookup"><span data-stu-id="8b1e9-104">The `IsEqualObject` function checks if two interfaces are on the same object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b1e9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b1e9-105">Syntax</span></span>


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a><span data-ttu-id="8b1e9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b1e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b1e9-107">*pFirst*</span><span class="sxs-lookup"><span data-stu-id="8b1e9-107">*pFirst*</span></span> 
</dt> <dd>

<span data-ttu-id="8b1e9-108">Pointeur vers une interface.</span><span class="sxs-lookup"><span data-stu-id="8b1e9-108">Pointer to one interface.</span></span>

</dd> <dt>

<span data-ttu-id="8b1e9-109">*pSecond*</span><span class="sxs-lookup"><span data-stu-id="8b1e9-109">*pSecond*</span></span> 
</dt> <dd>

<span data-ttu-id="8b1e9-110">Pointeur vers l’autre interface.</span><span class="sxs-lookup"><span data-stu-id="8b1e9-110">Pointer to the other interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b1e9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b1e9-111">Return value</span></span>

<span data-ttu-id="8b1e9-112">Retourne la **valeur true** si les interfaces sont à la fois sur le même objet, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8b1e9-112">Returns **TRUE** if the interfaces are both on the same object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b1e9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b1e9-113">Requirements</span></span>



| <span data-ttu-id="8b1e9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b1e9-114">Requirement</span></span> | <span data-ttu-id="8b1e9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b1e9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b1e9-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b1e9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8b1e9-117"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b1e9-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8b1e9-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8b1e9-118">Library</span></span><br/> | <dl> <span data-ttu-id="8b1e9-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8b1e9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b1e9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b1e9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b1e9-121">Fonctions d’assistance diverses</span><span class="sxs-lookup"><span data-stu-id="8b1e9-121">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




