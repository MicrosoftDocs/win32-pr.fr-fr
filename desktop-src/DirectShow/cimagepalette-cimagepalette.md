---
description: Méthode de constructeur.
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
ms.openlocfilehash: 38b5766617e1d17fa3917048c2fb845b5194cc42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540046"
---
# <a name="cimagepalettecimagepalette-constructor"></a><span data-ttu-id="b3a37-103">Constructeur CImagePalette. CImagePalette</span><span class="sxs-lookup"><span data-stu-id="b3a37-103">CImagePalette.CImagePalette constructor</span></span>

<span data-ttu-id="b3a37-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="b3a37-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3a37-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3a37-105">Syntax</span></span>


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a><span data-ttu-id="b3a37-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3a37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3a37-107">*pBaseFilter*</span><span class="sxs-lookup"><span data-stu-id="b3a37-107">*pBaseFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="b3a37-108">Pointeur vers le filtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="b3a37-108">Pointer to owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="b3a37-109">*pBaseWindow*</span><span class="sxs-lookup"><span data-stu-id="b3a37-109">*pBaseWindow*</span></span> 
</dt> <dd>

<span data-ttu-id="b3a37-110">Pointeur vers un objet **CBaseWindow** , qui gère la fenêtre dans laquelle la palette est réalisée.</span><span class="sxs-lookup"><span data-stu-id="b3a37-110">Pointer to a **CBaseWindow** object, which manages the window where the palette is realized.</span></span> <span data-ttu-id="b3a37-111">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b3a37-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b3a37-112">*pDrawImage*</span><span class="sxs-lookup"><span data-stu-id="b3a37-112">*pDrawImage*</span></span> 
</dt> <dd>

<span data-ttu-id="b3a37-113">Pointeur vers un objet **CDrawImage** , qui dessine l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="b3a37-113">Pointer to a **CDrawImage** object, which draws the video image.</span></span> <span data-ttu-id="b3a37-114">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b3a37-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3a37-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3a37-115">Requirements</span></span>



| <span data-ttu-id="b3a37-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3a37-116">Requirement</span></span> | <span data-ttu-id="b3a37-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3a37-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3a37-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3a37-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b3a37-119"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3a37-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b3a37-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b3a37-120">Library</span></span><br/> | <dl> <span data-ttu-id="b3a37-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b3a37-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3a37-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3a37-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3a37-123">**CImagePalette, classe**</span><span class="sxs-lookup"><span data-stu-id="b3a37-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




