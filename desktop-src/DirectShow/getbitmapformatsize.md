---
description: La fonction GetBitmapFormatSize calcule la taille nécessaire pour une structure VIDEOINFO qui peut contenir une structure BITMAPINFOHEADER spécifiée.
ms.assetid: a559415a-070f-4674-be12-a65a46025809
title: GetBitmapFormatSize, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapFormatSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39a64f6d975e403de6c177906b23ef7e09f29ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533091"
---
# <a name="getbitmapformatsize-function"></a><span data-ttu-id="09045-103">GetBitmapFormatSize fonction)</span><span class="sxs-lookup"><span data-stu-id="09045-103">GetBitmapFormatSize function</span></span>

<span data-ttu-id="09045-104">La `GetBitmapFormatSize` fonction calcule la taille nécessaire pour une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) qui peut contenir une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) spécifiée.</span><span class="sxs-lookup"><span data-stu-id="09045-104">The `GetBitmapFormatSize` function calculates the size needed for a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure that can hold a specified [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="09045-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09045-105">Syntax</span></span>


```C++
LONG GetBitmapFormatSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="09045-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09045-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09045-107">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="09045-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="09045-108">Pointeur vers une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="09045-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09045-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09045-109">Return value</span></span>

<span data-ttu-id="09045-110">Retourne la taille, en octets.</span><span class="sxs-lookup"><span data-stu-id="09045-110">Returns the size, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="09045-111">Notes</span><span class="sxs-lookup"><span data-stu-id="09045-111">Remarks</span></span>

<span data-ttu-id="09045-112">Une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) peut être suivie de masques de couleur ou d’entrées de palette. il peut donc être difficile de déterminer le nombre d’octets requis pour construire une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) à partir d’une structure **BITMAPINFOHEADER** existante.</span><span class="sxs-lookup"><span data-stu-id="09045-112">A [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure might be followed by color masks or palette entries, so it can be difficult to determine the number of bytes required to construct a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure from an existing **BITMAPINFOHEADER** structure.</span></span>

<span data-ttu-id="09045-113">Pour copier une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) dans une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) , utilisez la macro d' [**en-tête**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) , qui calcule le décalage correct.</span><span class="sxs-lookup"><span data-stu-id="09045-113">To copy a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure into a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure, use the [**HEADER**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) macro, which calculates the correct offset.</span></span>

## <a name="examples"></a><span data-ttu-id="09045-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="09045-114">Examples</span></span>


```
LONG size = GetBitmapFormatSize(&bmi);

VIDEOINFO *pVi = static_cast<VIDEOINFO*>(CoTaskMemAlloc(size));

if (pVi != NULL)
{
    CopyMemory(HEADER(pVi), &bmi, sizeof(BITMAPINFOHEADER));
}
```



## <a name="requirements"></a><span data-ttu-id="09045-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09045-115">Requirements</span></span>



| <span data-ttu-id="09045-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09045-116">Requirement</span></span> | <span data-ttu-id="09045-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="09045-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09045-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="09045-118">Header</span></span><br/>  | <dl> <span data-ttu-id="09045-119"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09045-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="09045-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="09045-120">Library</span></span><br/> | <dl> <span data-ttu-id="09045-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="09045-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09045-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09045-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09045-123">Fonctions vidéo et image</span><span class="sxs-lookup"><span data-stu-id="09045-123">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




