---
description: La méthode suivante récupère la position suivante dans la liste.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: Méthode CBaseList. Next (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8a09ec91191437fbfb851ce92824b118a5440ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528749"
---
# <a name="cbaselistnext-method"></a><span data-ttu-id="0906d-103">CBaseList. Next, méthode</span><span class="sxs-lookup"><span data-stu-id="0906d-103">CBaseList.Next method</span></span>

<span data-ttu-id="0906d-104">La `Next` méthode récupère la position suivante dans la liste.</span><span class="sxs-lookup"><span data-stu-id="0906d-104">The `Next` method retrieves the next position in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="0906d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0906d-105">Syntax</span></span>


```C++
POSITION Next(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="0906d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0906d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0906d-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="0906d-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="0906d-108">Valeur de POSITION.</span><span class="sxs-lookup"><span data-stu-id="0906d-108">POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0906d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0906d-109">Return value</span></span>

<span data-ttu-id="0906d-110">Retourne l’indicateur de position qui suit la position spécifiée par *pos*.</span><span class="sxs-lookup"><span data-stu-id="0906d-110">Returns the position indicator that follows the position specified by *pos*.</span></span>

## <a name="remarks"></a><span data-ttu-id="0906d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0906d-111">Remarks</span></span>

<span data-ttu-id="0906d-112">Si *pos* est la dernière position de la liste, la méthode retourne **null**.</span><span class="sxs-lookup"><span data-stu-id="0906d-112">If *pos* is the last position in the list, the method returns **NULL**.</span></span> <span data-ttu-id="0906d-113">Si *pos* a la **valeur null**, la méthode retourne la première position dans la liste.</span><span class="sxs-lookup"><span data-stu-id="0906d-113">If *pos* is **NULL**, the method returns the first position in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="0906d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0906d-114">Requirements</span></span>



| <span data-ttu-id="0906d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0906d-115">Requirement</span></span> | <span data-ttu-id="0906d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0906d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0906d-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="0906d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0906d-118"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0906d-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0906d-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0906d-119">Library</span></span><br/> | <dl> <span data-ttu-id="0906d-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0906d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0906d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0906d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0906d-122">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="0906d-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




