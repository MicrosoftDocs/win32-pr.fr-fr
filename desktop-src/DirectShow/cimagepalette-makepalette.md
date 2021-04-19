---
description: La méthode MakePalette crée une palette logique à partir de la table de couleurs dans un format vidéo.
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: Méthode CImagePalette. MakePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20c4484b2666b25b5d713ede450a9a5a99f93348
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527290"
---
# <a name="cimagepalettemakepalette-method"></a><span data-ttu-id="2f1d7-103">Méthode CImagePalette. MakePalette</span><span class="sxs-lookup"><span data-stu-id="2f1d7-103">CImagePalette.MakePalette method</span></span>

<span data-ttu-id="2f1d7-104">La `MakePalette` méthode crée une palette logique à partir de la table de couleurs dans un format vidéo.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-104">The `MakePalette` method creates a logical palette from the color table in a video format.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f1d7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f1d7-105">Syntax</span></span>


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="2f1d7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f1d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f1d7-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="2f1d7-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="2f1d7-108">Pointeur vers une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) qui contient la table des couleurs.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure that contains the color table.</span></span>

</dd> <dt>

<span data-ttu-id="2f1d7-109">*szDevice*</span><span class="sxs-lookup"><span data-stu-id="2f1d7-109">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="2f1d7-110">Pointeur vers une chaîne qui contient le nom du périphérique d’affichage, tel que retourné par la fonction GDI **EnumDisplayDevices** .</span><span class="sxs-lookup"><span data-stu-id="2f1d7-110">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="2f1d7-111">Pour utiliser le périphérique d’affichage principal, attribuez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-111">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f1d7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f1d7-112">Return value</span></span>

<span data-ttu-id="2f1d7-113">En cas de réussite, retourne un handle vers la palette.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-113">If successful, returns a handle to the palette.</span></span> <span data-ttu-id="2f1d7-114">Sinon, retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-114">Otherwise, returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f1d7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f1d7-115">Requirements</span></span>



| <span data-ttu-id="2f1d7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f1d7-116">Requirement</span></span> | <span data-ttu-id="2f1d7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f1d7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f1d7-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f1d7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2f1d7-119"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f1d7-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2f1d7-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2f1d7-120">Library</span></span><br/> | <dl> <span data-ttu-id="2f1d7-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2f1d7-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f1d7-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f1d7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f1d7-123">**CImagePalette, classe**</span><span class="sxs-lookup"><span data-stu-id="2f1d7-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




