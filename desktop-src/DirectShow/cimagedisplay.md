---
description: La classe CImageDisplay est une classe d’assistance pour les convertisseurs vidéo GDI pour gérer le format d’affichage.
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: CImageDisplay, classe (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a7cbb28c53d8ff357d4e5174d24f92ba2d0cad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521718"
---
# <a name="cimagedisplay-class"></a><span data-ttu-id="d5b97-103">CImageDisplay, classe</span><span class="sxs-lookup"><span data-stu-id="d5b97-103">CImageDisplay class</span></span>

![cimagedisplayclasshierarchy](images/wutil06.png)

<span data-ttu-id="d5b97-105">La `CImageDisplay` classe est une classe d’assistance pour les convertisseurs vidéo GDI pour gérer le format d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d5b97-105">The `CImageDisplay` class is a helper class for GDI video renderers to manage the display format.</span></span> <span data-ttu-id="d5b97-106">L’objet stocke une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) qui décrit le mode d’affichage actuel, qui est initialisé dans la méthode du constructeur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d5b97-106">The object stores a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure that describes the current display mode, which is initialized in the object's constructor method.</span></span> <span data-ttu-id="d5b97-107">La méthode **CheckMediaType** de l’objet vérifie si un type de média proposé peut être rendu efficacement à l’aide de GDI.</span><span class="sxs-lookup"><span data-stu-id="d5b97-107">The object's **CheckMediaType** method checks whether a proposed media type can be rendered efficiently using GDI.</span></span>



| <span data-ttu-id="d5b97-108">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="d5b97-108">Protected Member Variables</span></span>                                       | <span data-ttu-id="d5b97-109">Description</span><span class="sxs-lookup"><span data-stu-id="d5b97-109">Description</span></span>                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5b97-110">**\_affichage m**</span><span class="sxs-lookup"><span data-stu-id="d5b97-110">**m\_Display**</span></span>](cimagedisplay-m-display.md)                    | <span data-ttu-id="d5b97-111">Structure **VIDEOINFO** qui décrit le format d’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="d5b97-111">**VIDEOINFO** structure that describes the current display format.</span></span>                     |
| <span data-ttu-id="d5b97-112">Méthodes protégées</span><span class="sxs-lookup"><span data-stu-id="d5b97-112">Protected Methods</span></span>                                                | <span data-ttu-id="d5b97-113">Description</span><span class="sxs-lookup"><span data-stu-id="d5b97-113">Description</span></span>                                                                            |
| [<span data-ttu-id="d5b97-114">**CheckBitFields**</span><span class="sxs-lookup"><span data-stu-id="d5b97-114">**CheckBitFields**</span></span>](cimagedisplay-checkbitfields.md)           | <span data-ttu-id="d5b97-115">Valide les masques de couleur dans une structure **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="d5b97-115">Validates the color masks in a **VIDEOINFO** structure.</span></span>                                |
| [<span data-ttu-id="d5b97-116">**CountPrefixBits**</span><span class="sxs-lookup"><span data-stu-id="d5b97-116">**CountPrefixBits**</span></span>](cimagedisplay-countprefixbits.md)         | <span data-ttu-id="d5b97-117">Calcule le nombre de bits zéro au début d’un champ de bits spécifié.</span><span class="sxs-lookup"><span data-stu-id="d5b97-117">Calculates the number of zero bits at the start of a specified bit field.</span></span>              |
| [<span data-ttu-id="d5b97-118">**CountSetBits**</span><span class="sxs-lookup"><span data-stu-id="d5b97-118">**CountSetBits**</span></span>](cimagedisplay-countsetbits.md)               | <span data-ttu-id="d5b97-119">Retourne le nombre de bits définis sur 1 dans un champ de bits spécifié.</span><span class="sxs-lookup"><span data-stu-id="d5b97-119">Returns the number of bits set to 1 in a specified bit field.</span></span>                          |
| <span data-ttu-id="d5b97-120">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="d5b97-120">Public Methods</span></span>                                                   | <span data-ttu-id="d5b97-121">Description</span><span class="sxs-lookup"><span data-stu-id="d5b97-121">Description</span></span>                                                                            |
| [<span data-ttu-id="d5b97-122">**CheckHeaderValidity**</span><span class="sxs-lookup"><span data-stu-id="d5b97-122">**CheckHeaderValidity**</span></span>](cimagedisplay-checkheadervalidity.md) | <span data-ttu-id="d5b97-123">Valide une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="d5b97-123">Validates a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>                    |
| [<span data-ttu-id="d5b97-124">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="d5b97-124">**CheckMediaType**</span></span>](cimagedisplay-checkmediatype.md)           | <span data-ttu-id="d5b97-125">Détermine si un type de média proposé est compatible avec le format d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d5b97-125">Determines whether a proposed media type is compatible with the display format.</span></span>        |
| [<span data-ttu-id="d5b97-126">**CheckPaletteHeader**</span><span class="sxs-lookup"><span data-stu-id="d5b97-126">**CheckPaletteHeader**</span></span>](cimagedisplay-checkpaletteheader.md)   | <span data-ttu-id="d5b97-127">Valide les entrées de palette dans une structure **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="d5b97-127">Validates the palette entries in a **VIDEOINFO** structure.</span></span>                            |
| [<span data-ttu-id="d5b97-128">**CheckVideoType**</span><span class="sxs-lookup"><span data-stu-id="d5b97-128">**CheckVideoType**</span></span>](cimagedisplay-checkvideotype.md)           | <span data-ttu-id="d5b97-129">Vérifie si un format **VIDEOINFO** spécifié est compatible avec le format d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d5b97-129">Checks whether a specified **VIDEOINFO** format is compatible with the display format.</span></span> |
| [<span data-ttu-id="d5b97-130">**CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="d5b97-130">**CImageDisplay**</span></span>](cimagedisplay-cimagedisplay.md)             | <span data-ttu-id="d5b97-131">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="d5b97-131">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="d5b97-132">**GetBitMasks**</span><span class="sxs-lookup"><span data-stu-id="d5b97-132">**GetBitMasks**</span></span>](cimagedisplay-getbitmasks.md)                 | <span data-ttu-id="d5b97-133">Récupère les masques de couleur pour un format **VIDEOINFO** spécifié.</span><span class="sxs-lookup"><span data-stu-id="d5b97-133">Retrieves the color masks for a specified **VIDEOINFO** format.</span></span>                        |
| [<span data-ttu-id="d5b97-134">**GetColourMask**</span><span class="sxs-lookup"><span data-stu-id="d5b97-134">**GetColourMask**</span></span>](cimagedisplay-getcolourmask.md)             | <span data-ttu-id="d5b97-135">Récupère les masques de couleur pour le format d’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="d5b97-135">Retrieves the color masks for the current display format.</span></span>                              |
| [<span data-ttu-id="d5b97-136">**GetDisplayDepth**</span><span class="sxs-lookup"><span data-stu-id="d5b97-136">**GetDisplayDepth**</span></span>](cimagedisplay-getdisplaydepth.md)         | <span data-ttu-id="d5b97-137">Récupère la profondeur en bits du mode d’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="d5b97-137">Retrieves the bit depth of the current display mode.</span></span>                                   |
| [<span data-ttu-id="d5b97-138">**GetDisplayFormat**</span><span class="sxs-lookup"><span data-stu-id="d5b97-138">**GetDisplayFormat**</span></span>](cimagedisplay-getdisplayformat.md)       | <span data-ttu-id="d5b97-139">Récupère un format vidéo qui décrit le mode d’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="d5b97-139">Retrieves a video format that describes the current display mode.</span></span>                      |
| [<span data-ttu-id="d5b97-140">**IsPalettised**</span><span class="sxs-lookup"><span data-stu-id="d5b97-140">**IsPalettised**</span></span>](cimagedisplay-ispalettised.md)               | <span data-ttu-id="d5b97-141">Retermines si le format d’affichage actuel est en palette.</span><span class="sxs-lookup"><span data-stu-id="d5b97-141">Retermines whether the current display format is palettized.</span></span>                           |
| [<span data-ttu-id="d5b97-142">**RefreshDisplayType**</span><span class="sxs-lookup"><span data-stu-id="d5b97-142">**RefreshDisplayType**</span></span>](cimagedisplay-refreshdisplaytype.md)   | <span data-ttu-id="d5b97-143">Met à jour le format vidéo de l’objet pour qu’il corresponde à l’affichage spécifié</span><span class="sxs-lookup"><span data-stu-id="d5b97-143">Updates the object's video format to match the specified display</span></span>                       |



 

## <a name="requirements"></a><span data-ttu-id="d5b97-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5b97-144">Requirements</span></span>



| <span data-ttu-id="d5b97-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5b97-145">Requirement</span></span> | <span data-ttu-id="d5b97-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5b97-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5b97-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5b97-147">Header</span></span><br/>  | <dl> <span data-ttu-id="d5b97-148"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5b97-148"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d5b97-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d5b97-149">Library</span></span><br/> | <dl> <span data-ttu-id="d5b97-150"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d5b97-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




