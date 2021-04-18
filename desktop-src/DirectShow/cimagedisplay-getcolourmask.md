---
description: La méthode GetColourMask récupère les masques de couleur pour le format d’affichage actuel.
ms.assetid: 386d0439-8502-411d-935c-3c2153a8b5b4
title: Méthode CImageDisplay. GetColourMask (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetColourMask
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 499b3677cd68444b58514d692d87cd4f631350b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533237"
---
# <a name="cimagedisplaygetcolourmask-method"></a><span data-ttu-id="06e7f-103">Méthode CImageDisplay. GetColourMask</span><span class="sxs-lookup"><span data-stu-id="06e7f-103">CImageDisplay.GetColourMask method</span></span>

<span data-ttu-id="06e7f-104">La `GetColourMask` méthode récupère les masques de couleur pour le format d’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="06e7f-104">The `GetColourMask` method retrieves the color masks for the current display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="06e7f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06e7f-105">Syntax</span></span>


```C++
BOOL GetColourMask(
   DWORD *pMaskRed,
   DWORD *pMaskGreen,
   DWORD *pMaskBlue
);
```



## <a name="parameters"></a><span data-ttu-id="06e7f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06e7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06e7f-107">*pMaskRed*</span><span class="sxs-lookup"><span data-stu-id="06e7f-107">*pMaskRed*</span></span> 
</dt> <dd>

<span data-ttu-id="06e7f-108">Pointeur vers une variable qui reçoit le masque de composant rouge.</span><span class="sxs-lookup"><span data-stu-id="06e7f-108">Pointer to a variable that receives the red-component mask.</span></span>

</dd> <dt>

<span data-ttu-id="06e7f-109">*pMaskGreen*</span><span class="sxs-lookup"><span data-stu-id="06e7f-109">*pMaskGreen*</span></span> 
</dt> <dd>

<span data-ttu-id="06e7f-110">Pointeur vers une variable qui reçoit le masque de composant vert.</span><span class="sxs-lookup"><span data-stu-id="06e7f-110">Pointer to a variable that receives the green-component mask.</span></span>

</dd> <dt>

<span data-ttu-id="06e7f-111">*pMaskBlue*</span><span class="sxs-lookup"><span data-stu-id="06e7f-111">*pMaskBlue*</span></span> 
</dt> <dd>

<span data-ttu-id="06e7f-112">Pointeur vers une variable qui reçoit le masque de composant bleu.</span><span class="sxs-lookup"><span data-stu-id="06e7f-112">Pointer to a variable that receives the blue-component mask.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06e7f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06e7f-113">Return value</span></span>

<span data-ttu-id="06e7f-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="06e7f-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="06e7f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06e7f-115">Requirements</span></span>



| <span data-ttu-id="06e7f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06e7f-116">Requirement</span></span> | <span data-ttu-id="06e7f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="06e7f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06e7f-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="06e7f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="06e7f-119"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06e7f-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="06e7f-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="06e7f-120">Library</span></span><br/> | <dl> <span data-ttu-id="06e7f-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="06e7f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06e7f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06e7f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06e7f-123">**CImageDisplay, classe**</span><span class="sxs-lookup"><span data-stu-id="06e7f-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




