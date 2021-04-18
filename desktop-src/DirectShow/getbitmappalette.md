---
description: La fonction GetBitmapPalette retourne la première entrée de palette dans une structure VIDEOINFOHEADER.
ms.assetid: 7c620f81-31d9-408f-954d-aeff39f93956
title: GetBitmapPalette, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa4139c7aaece3e92a26fbf69fc02b8759f1613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540283"
---
# <a name="getbitmappalette-function"></a><span data-ttu-id="bb1b0-103">GetBitmapPalette fonction)</span><span class="sxs-lookup"><span data-stu-id="bb1b0-103">GetBitmapPalette function</span></span>

<span data-ttu-id="bb1b0-104">La `GetBitmapPalette` fonction retourne la première entrée de la palette dans une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="bb1b0-104">The `GetBitmapPalette` function returns the first palette entry in a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb1b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb1b0-105">Syntax</span></span>


```C++
const RGBQUAD* GetBitmapPalette(
   const VIDEOINFOHEADER *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="bb1b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb1b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb1b0-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="bb1b0-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="bb1b0-108">Pointeur vers une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="bb1b0-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb1b0-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb1b0-109">Return value</span></span>

<span data-ttu-id="bb1b0-110">Retourne un pointeur vers la première entrée de la palette.</span><span class="sxs-lookup"><span data-stu-id="bb1b0-110">Returns a pointer to the first palette entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb1b0-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb1b0-111">Requirements</span></span>



| <span data-ttu-id="bb1b0-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb1b0-112">Requirement</span></span> | <span data-ttu-id="bb1b0-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb1b0-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb1b0-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb1b0-114">Header</span></span><br/>  | <dl> <span data-ttu-id="bb1b0-115"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb1b0-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="bb1b0-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bb1b0-116">Library</span></span><br/> | <dl> <span data-ttu-id="bb1b0-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bb1b0-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




