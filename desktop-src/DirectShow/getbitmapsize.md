---
description: La fonction GetBitmapSize calcule le nombre d’octets requis par une image bitmap indépendante du périphérique (DIB, Device-Independent Bitmap). Cette fonction appelle simplement la macro DIBSIZE.
ms.assetid: ce23cdf2-9804-4d2e-b9ef-16e54b2d571e
title: GetBitmapSize, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 004201cf3ff839aa1301dcfff0240a73a9128e50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537522"
---
# <a name="getbitmapsize-function"></a><span data-ttu-id="d66c9-104">GetBitmapSize fonction)</span><span class="sxs-lookup"><span data-stu-id="d66c9-104">GetBitmapSize function</span></span>

<span data-ttu-id="d66c9-105">La `GetBitmapSize` fonction calcule le nombre d’octets requis par une image bitmap indépendante du périphérique (DIB, Device-Independent Bitmap).</span><span class="sxs-lookup"><span data-stu-id="d66c9-105">The `GetBitmapSize` function calculates the number of bytes required by a device-independent bitmap (DIB).</span></span> <span data-ttu-id="d66c9-106">Cette fonction appelle simplement la macro [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) .</span><span class="sxs-lookup"><span data-stu-id="d66c9-106">This function simply calls the [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) macro.</span></span>

## <a name="syntax"></a><span data-ttu-id="d66c9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d66c9-107">Syntax</span></span>


```C++
DWORD GetBitmapSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="d66c9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d66c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d66c9-109">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="d66c9-109">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="d66c9-110">Pointeur vers une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="d66c9-110">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d66c9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d66c9-111">Return value</span></span>

<span data-ttu-id="d66c9-112">Retourne la taille en octets.</span><span class="sxs-lookup"><span data-stu-id="d66c9-112">Returns the size in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="d66c9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d66c9-113">Requirements</span></span>



| <span data-ttu-id="d66c9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d66c9-114">Requirement</span></span> | <span data-ttu-id="d66c9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d66c9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d66c9-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="d66c9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d66c9-117"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d66c9-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d66c9-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d66c9-118">Library</span></span><br/> | <dl> <span data-ttu-id="d66c9-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d66c9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d66c9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d66c9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d66c9-121">Fonctions vidéo et image</span><span class="sxs-lookup"><span data-stu-id="d66c9-121">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




