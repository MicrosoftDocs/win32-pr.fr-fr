---
description: La méthode ShouldUpdate détermine s’il est nécessaire de créer une nouvelle palette.
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: Méthode CImagePalette. ShouldUpdate (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.ShouldUpdate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8cf27548487ad0338f0c4773c66df8f7d03c2f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543784"
---
# <a name="cimagepaletteshouldupdate-method"></a><span data-ttu-id="4bdc3-103">Méthode CImagePalette. ShouldUpdate</span><span class="sxs-lookup"><span data-stu-id="4bdc3-103">CImagePalette.ShouldUpdate method</span></span>

<span data-ttu-id="4bdc3-104">La `ShouldUpdate` méthode détermine s’il est nécessaire de créer une nouvelle palette.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-104">The `ShouldUpdate` method determines whether it is necessary to create a new palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bdc3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bdc3-105">Syntax</span></span>


```C++
BOOL ShouldUpdate(
   const VIDEOINFOHEADER *pNewInfo,
   const VIDEOINFOHEADER *pOldInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4bdc3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4bdc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bdc3-107">*pNewInfo*</span><span class="sxs-lookup"><span data-stu-id="4bdc3-107">*pNewInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="4bdc3-108">Pointeur vers une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) contenant la nouvelle table de couleurs.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure containing the new color table.</span></span>

</dd> <dt>

<span data-ttu-id="4bdc3-109">*pOldInfo*</span><span class="sxs-lookup"><span data-stu-id="4bdc3-109">*pOldInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="4bdc3-110">Pointeur vers une structure **VIDEOINFOHEADER** contenant l’ancienne table de couleurs.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-110">Pointer to a **VIDEOINFOHEADER** structure containing the old color table.</span></span> <span data-ttu-id="4bdc3-111">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-111">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bdc3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4bdc3-112">Return value</span></span>

<span data-ttu-id="4bdc3-113">Retourne la **valeur true** si la palette doit être mise à jour, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-113">Returns **TRUE** if the palette needs to be updated, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bdc3-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4bdc3-114">Remarks</span></span>

-   <span data-ttu-id="4bdc3-115">Si aucune structure **VIDEOINFOHEADER** ne contient de table de couleurs, la méthode retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-115">If neither **VIDEOINFOHEADER** structure contains a color table, the method returns **FALSE**.</span></span>
-   <span data-ttu-id="4bdc3-116">Si une seule structure contient une table de couleurs ou si *pOldInfo* a la **valeur null**, la méthode retourne **true**.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-116">If only one structure contains a color table, or if *pOldInfo* is **NULL**, the method returns **TRUE**.</span></span>
-   <span data-ttu-id="4bdc3-117">Si les deux structures contiennent des tables de couleurs et que les entrées de couleur correspondent, la méthode retourne la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-117">If both structures contain color tables, and the color entries match, the method returns **FALSE**.</span></span>
-   <span data-ttu-id="4bdc3-118">Si les deux structures contiennent des tables de couleurs, mais que les entrées de couleur ne correspondent pas, la méthode retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="4bdc3-118">If both structures contain color tables, but the color entries do not match, the method returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bdc3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bdc3-119">Requirements</span></span>



| <span data-ttu-id="4bdc3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bdc3-120">Requirement</span></span> | <span data-ttu-id="4bdc3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bdc3-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bdc3-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="4bdc3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4bdc3-123"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4bdc3-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4bdc3-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4bdc3-124">Library</span></span><br/> | <dl> <span data-ttu-id="4bdc3-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4bdc3-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bdc3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bdc3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bdc3-127">**CImagePalette, classe**</span><span class="sxs-lookup"><span data-stu-id="4bdc3-127">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




