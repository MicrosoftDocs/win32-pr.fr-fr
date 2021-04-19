---
description: La méthode GetBitMasks récupère les masques de couleur pour un format VIDEOINFO spécifié.
ms.assetid: 72a9ba44-96de-4fff-a3fb-675d3dd080d8
title: Méthode CImageDisplay. GetBitMasks (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetBitMasks
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2defe5e80a0d7311adcd19dca67119019623993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541517"
---
# <a name="cimagedisplaygetbitmasks-method"></a><span data-ttu-id="3cb17-103">Méthode CImageDisplay. GetBitMasks</span><span class="sxs-lookup"><span data-stu-id="3cb17-103">CImageDisplay.GetBitMasks method</span></span>

<span data-ttu-id="3cb17-104">La `GetBitMasks` méthode récupère les masques de couleur pour un format [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) spécifié.</span><span class="sxs-lookup"><span data-stu-id="3cb17-104">The `GetBitMasks` method retrieves the color masks for a specified [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) format.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cb17-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cb17-105">Syntax</span></span>


```C++
const DWORD* GetBitMasks(
   const VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3cb17-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cb17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cb17-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="3cb17-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="3cb17-108">Pointeur vers la structure **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="3cb17-108">Pointer to the **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cb17-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3cb17-109">Return value</span></span>

<span data-ttu-id="3cb17-110">Retourne un tableau de trois valeurs **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="3cb17-110">Returns an array of three **DWORD** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cb17-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3cb17-111">Remarks</span></span>

<span data-ttu-id="3cb17-112">Si le membre de **décompression** est bi-champs \_ , la méthode retourne un pointeur vers les masques de couleur qui sont fournis dans le membre **dwBitMasks** .</span><span class="sxs-lookup"><span data-stu-id="3cb17-112">If the **biCompression** member is BI\_BITFIELDS, the method returns a pointer to the color masks that are supplied in the **dwBitMasks** member.</span></span> <span data-ttu-id="3cb17-113">Si le membre de **bicompression** est bi \_ RGB, la méthode retourne les masques de couleur qui correspondent à la profondeur de bit.</span><span class="sxs-lookup"><span data-stu-id="3cb17-113">If the **biCompression** member is BI\_RGB, the method returns the color masks that correspond to the bit depth.</span></span> <span data-ttu-id="3cb17-114">Si la méthode échoue (par exemple, la profondeur du bit est inférieure à 16), la méthode retourne le tableau {0,0,0} .</span><span class="sxs-lookup"><span data-stu-id="3cb17-114">If the method fails (for example, the bit depth is less than 16), the method returns the array {0,0,0}.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb17-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cb17-115">Requirements</span></span>



| <span data-ttu-id="3cb17-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cb17-116">Requirement</span></span> | <span data-ttu-id="3cb17-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cb17-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb17-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="3cb17-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3cb17-119"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3cb17-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3cb17-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3cb17-120">Library</span></span><br/> | <dl> <span data-ttu-id="3cb17-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3cb17-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cb17-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cb17-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cb17-123">**CImageDisplay, classe**</span><span class="sxs-lookup"><span data-stu-id="3cb17-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




