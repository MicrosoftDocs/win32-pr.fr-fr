---
description: Méthode constructeur CImagePalette. CImagePalette.
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Constructeur CImagePalette. CImagePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CImagePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5021b165a8fa47bedc7961657d7cdbfa07af301d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085677"
---
# <a name="cimagepalettecimagepalette-constructor"></a><span data-ttu-id="aee24-103">Constructeur CImagePalette. CImagePalette</span><span class="sxs-lookup"><span data-stu-id="aee24-103">CImagePalette.CImagePalette constructor</span></span>

<span data-ttu-id="aee24-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="aee24-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aee24-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aee24-105">Syntax</span></span>


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a><span data-ttu-id="aee24-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aee24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aee24-107">*pBaseFilter*</span><span class="sxs-lookup"><span data-stu-id="aee24-107">*pBaseFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="aee24-108">Pointeur vers le filtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="aee24-108">Pointer to owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="aee24-109">*pBaseWindow*</span><span class="sxs-lookup"><span data-stu-id="aee24-109">*pBaseWindow*</span></span> 
</dt> <dd>

<span data-ttu-id="aee24-110">Pointeur vers un objet **CBaseWindow** , qui gère la fenêtre dans laquelle la palette est réalisée.</span><span class="sxs-lookup"><span data-stu-id="aee24-110">Pointer to a **CBaseWindow** object, which manages the window where the palette is realized.</span></span> <span data-ttu-id="aee24-111">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="aee24-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aee24-112">*pDrawImage*</span><span class="sxs-lookup"><span data-stu-id="aee24-112">*pDrawImage*</span></span> 
</dt> <dd>

<span data-ttu-id="aee24-113">Pointeur vers un objet **CDrawImage** , qui dessine l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="aee24-113">Pointer to a **CDrawImage** object, which draws the video image.</span></span> <span data-ttu-id="aee24-114">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="aee24-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aee24-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aee24-115">Requirements</span></span>



| <span data-ttu-id="aee24-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aee24-116">Requirement</span></span> | <span data-ttu-id="aee24-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="aee24-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aee24-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="aee24-118">Header</span></span><br/>  | <dl> <span data-ttu-id="aee24-119"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aee24-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aee24-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aee24-120">Library</span></span><br/> | <dl> <span data-ttu-id="aee24-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="aee24-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aee24-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aee24-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee24-123">**CImagePalette, classe**</span><span class="sxs-lookup"><span data-stu-id="aee24-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




