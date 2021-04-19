---
description: La méthode PreparePalette configure une palette, en fonction d’un type de média à partir du filtre propriétaire.
ms.assetid: cb012391-39ab-4ad1-aeb7-ec25010ac64a
title: Méthode CImagePalette. PreparePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.PreparePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9b09804b2ee6ad9fbda394a7fb8f9f188b46453
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525151"
---
# <a name="cimagepalettepreparepalette-method"></a><span data-ttu-id="b0f57-103">Méthode CImagePalette. PreparePalette</span><span class="sxs-lookup"><span data-stu-id="b0f57-103">CImagePalette.PreparePalette method</span></span>

<span data-ttu-id="b0f57-104">La `PreparePalette` méthode Configure une palette, en fonction d’un type de média à partir du filtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="b0f57-104">The `PreparePalette` method sets up a palette, based on a media type from the owning filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f57-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0f57-105">Syntax</span></span>


```C++
HRESULT PreparePalette(
   const CMediaType *pmtNew,
   const CMediaType *pmtOld,
         LPSTR      szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="b0f57-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0f57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0f57-107">*pmtNew*</span><span class="sxs-lookup"><span data-stu-id="b0f57-107">*pmtNew*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f57-108">Pointeur vers le nouveau type de média.</span><span class="sxs-lookup"><span data-stu-id="b0f57-108">Pointer to the new media type.</span></span> <span data-ttu-id="b0f57-109">Le bloc de format doit être une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="b0f57-109">The format block must be a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b0f57-110">*pmtOld*</span><span class="sxs-lookup"><span data-stu-id="b0f57-110">*pmtOld*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f57-111">Pointeur vers l’ancien type de média.</span><span class="sxs-lookup"><span data-stu-id="b0f57-111">Pointer to the old media type.</span></span> <span data-ttu-id="b0f57-112">Si le type de média est défini pour la première fois, ce paramètre peut être un type vide sans bloc de format.</span><span class="sxs-lookup"><span data-stu-id="b0f57-112">If the media type is being set for the first time, this parameter can be an empty type with no format block.</span></span> <span data-ttu-id="b0f57-113">Dans le cas contraire, le bloc de format doit être une structure **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="b0f57-113">Otherwise, the format block must be a **VIDEOINFOHEADER** structure.</span></span>

</dd> <dt>

<span data-ttu-id="b0f57-114">*szDevice*</span><span class="sxs-lookup"><span data-stu-id="b0f57-114">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f57-115">Pointeur vers une chaîne qui contient le nom du périphérique d’affichage, tel que retourné par la fonction GDI **EnumDisplayDevices** .</span><span class="sxs-lookup"><span data-stu-id="b0f57-115">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="b0f57-116">Pour utiliser le périphérique d’affichage principal, attribuez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="b0f57-116">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0f57-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0f57-117">Return value</span></span>

<span data-ttu-id="b0f57-118">Retourne S \_ si la palette a été mise à jour ou \_ false si elle n’a pas changé.</span><span class="sxs-lookup"><span data-stu-id="b0f57-118">Returns S\_OK if the palette was updated, or S\_FALSE if the palette did not change.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0f57-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b0f57-119">Remarks</span></span>

<span data-ttu-id="b0f57-120">Si la palette doit être mise à jour, cette méthode effectue les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b0f57-120">If the palette needs to be updated, this method performs the following actions:</span></span>

-   <span data-ttu-id="b0f57-121">Appelle [**CImagePalette :: MakePalette**](cimagepalette-makepalette.md) pour créer une nouvelle palette logique.</span><span class="sxs-lookup"><span data-stu-id="b0f57-121">Calls [**CImagePalette::MakePalette**](cimagepalette-makepalette.md) to create a new logical palette.</span></span>
-   <span data-ttu-id="b0f57-122">Envoie un événement de [**\_ \_ modification de palette EC**](ec-palette-changed.md) au gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="b0f57-122">Sends an [**EC\_PALETTE\_CHANGED**](ec-palette-changed.md) event to the Filter Graph Manager.</span></span>
-   <span data-ttu-id="b0f57-123">Appelle [**CBaseWindow :: SetPalette**](cbasewindow-setpalette.md) sur l’objet **CBaseWindow** .</span><span class="sxs-lookup"><span data-stu-id="b0f57-123">Calls [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) on the **CBaseWindow** object.</span></span>
-   <span data-ttu-id="b0f57-124">Appelle [**CDrawImage :: IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) sur l’objet **CDrawImage** .</span><span class="sxs-lookup"><span data-stu-id="b0f57-124">Calls [**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) on the **CDrawImage** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0f57-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0f57-125">Requirements</span></span>



| <span data-ttu-id="b0f57-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0f57-126">Requirement</span></span> | <span data-ttu-id="b0f57-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0f57-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f57-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0f57-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b0f57-129"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0f57-129"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b0f57-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b0f57-130">Library</span></span><br/> | <dl> <span data-ttu-id="b0f57-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b0f57-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0f57-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0f57-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0f57-133">**CImagePalette, classe**</span><span class="sxs-lookup"><span data-stu-id="b0f57-133">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




