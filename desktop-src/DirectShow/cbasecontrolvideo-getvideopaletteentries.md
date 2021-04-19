---
description: La méthode GetVideoPaletteEntries récupère une plage d’entrées de palette pour la vidéo.
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: Méthode CBaseControlVideo. GetVideoPaletteEntries (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoPaletteEntries
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa354922e57436c0d9e3e18924dcf31afe1629e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529982"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a><span data-ttu-id="e6164-103">Méthode CBaseControlVideo. GetVideoPaletteEntries</span><span class="sxs-lookup"><span data-stu-id="e6164-103">CBaseControlVideo.GetVideoPaletteEntries method</span></span>

<span data-ttu-id="e6164-104">La `GetVideoPaletteEntries` méthode récupère une plage d’entrées de palette pour la vidéo.</span><span class="sxs-lookup"><span data-stu-id="e6164-104">The `GetVideoPaletteEntries` method retrieves a range of palette entries for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6164-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6164-105">Syntax</span></span>


```C++
HRESULT GetVideoPaletteEntries(
   long StartIndex,
   long Entries,
   long *pRetrieved,
   long *pPalette
);
```



## <a name="parameters"></a><span data-ttu-id="e6164-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6164-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6164-107">*StartIndex*</span><span class="sxs-lookup"><span data-stu-id="e6164-107">*StartIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="e6164-108">Entrée de la palette de démarrage de base zéro.</span><span class="sxs-lookup"><span data-stu-id="e6164-108">Zero-based start palette entry.</span></span>

</dd> <dt>

<span data-ttu-id="e6164-109">*Écritures*</span><span class="sxs-lookup"><span data-stu-id="e6164-109">*Entries*</span></span> 
</dt> <dd>

<span data-ttu-id="e6164-110">Nombre d’entrées requises.</span><span class="sxs-lookup"><span data-stu-id="e6164-110">Number of entries required.</span></span>

</dd> <dt>

<span data-ttu-id="e6164-111">*pRetrieved*</span><span class="sxs-lookup"><span data-stu-id="e6164-111">*pRetrieved*</span></span> 
</dt> <dd>

<span data-ttu-id="e6164-112">Pointeur vers le nombre de couleurs obtenues.</span><span class="sxs-lookup"><span data-stu-id="e6164-112">Pointer to the number of colors obtained.</span></span>

</dd> <dt>

<span data-ttu-id="e6164-113">*pPalette*</span><span class="sxs-lookup"><span data-stu-id="e6164-113">*pPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="e6164-114">Pointeur vers la mémoire tampon de sortie pour les couleurs.</span><span class="sxs-lookup"><span data-stu-id="e6164-114">Pointer to output buffer for colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6164-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6164-115">Return value</span></span>

<span data-ttu-id="e6164-116">Retourne une erreur noerreur en cas de réussite, VFW \_ e \_ no \_ palette \_ disponible si les exemples vidéo n’ont pas de palette de couleurs, e \_ OUTOFMEMORY si la mémoire disponible est insuffisante, e \_ INVALIDARG si *startIndex* n’est pas valide ou \_ a la valeur false s’il n’y a aucune couleur dans la palette.</span><span class="sxs-lookup"><span data-stu-id="e6164-116">Returns NOERROR if successful, VFW\_E\_NO\_PALETTE\_AVAILABLE if the video samples has no color palette, E\_OUTOFMEMORY if there is not enough memory available, E\_INVALIDARG if *StartIndex* is invalid, or S\_FALSE if there are no colors in the palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6164-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e6164-117">Remarks</span></span>

<span data-ttu-id="e6164-118">Cette fonction membre retourne la palette actuelle de la vidéo sous la forme d’un tableau alloué par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6164-118">This member function returns the current palette of the video as an array allocated by the user.</span></span> <span data-ttu-id="e6164-119">Pour rester cohérent, utilisez les membres de la structure Win32 **PaletteEntry** pour retourner les couleurs, plutôt que les membres de la structure **RGBQUAD** (même si le paramètre est **long**).</span><span class="sxs-lookup"><span data-stu-id="e6164-119">To remain consistent, use the members in the Win32 **PALETTEENTRY** structure to return the colors, rather than the members in the **RGBQUAD** structure (although the parameter is a **LONG**).</span></span> <span data-ttu-id="e6164-120">La mémoire est allouée par l’appelant. par conséquent, il suffit de copier chacun à son tour.</span><span class="sxs-lookup"><span data-stu-id="e6164-120">The memory is allocated by the caller, so simply copy each in turn.</span></span> <span data-ttu-id="e6164-121">Déterminez que le nombre d’entrées demandées et le décalage de position de début sont valides.</span><span class="sxs-lookup"><span data-stu-id="e6164-121">Determine that the number of entries requested and the start position offset are both valid.</span></span> <span data-ttu-id="e6164-122">Si le nombre d’entrées est égal à zéro, retourne un \_ faux code.</span><span class="sxs-lookup"><span data-stu-id="e6164-122">If the number of entries evaluates to zero, return an S\_FALSE code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6164-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6164-123">Requirements</span></span>



| <span data-ttu-id="e6164-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6164-124">Requirement</span></span> | <span data-ttu-id="e6164-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6164-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6164-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6164-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e6164-127"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6164-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6164-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e6164-128">Library</span></span><br/> | <dl> <span data-ttu-id="e6164-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e6164-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6164-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6164-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6164-131">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="e6164-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




