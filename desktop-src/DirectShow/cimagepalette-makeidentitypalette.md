---
description: La méthode MakeIdentityPalette tente de créer une &\# 0034 ; palette d’identité, &\# 0034 ; définie comme une correspondance directe avec la palette sélectionnée dans le périphérique d’affichage.
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: Méthode CImagePalette. MakeIdentityPalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakeIdentityPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e105652108e74907375408f0bd8946c69194202
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539566"
---
# <a name="cimagepalettemakeidentitypalette-method"></a><span data-ttu-id="03359-103">Méthode CImagePalette. MakeIdentityPalette</span><span class="sxs-lookup"><span data-stu-id="03359-103">CImagePalette.MakeIdentityPalette method</span></span>

<span data-ttu-id="03359-104">La `MakeIdentityPalette` méthode tente de faire une « palette d’identité » définie comme un mappage direct à la palette sélectionnée dans le périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="03359-104">The `MakeIdentityPalette` method attempts to make an "identity palette," defined as one that maps directly to the palette selected in the display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="03359-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03359-105">Syntax</span></span>


```C++
HRESULT MakeIdentityPalette(
   PALETTEENTRY *pEntry,
   INT          iColours,
   LPSTR        szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="03359-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03359-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03359-107">*pEntry*</span><span class="sxs-lookup"><span data-stu-id="03359-107">*pEntry*</span></span> 
</dt> <dd>

<span data-ttu-id="03359-108">Pointeur vers un tableau d’entrées de palette.</span><span class="sxs-lookup"><span data-stu-id="03359-108">Pointer to an array of palette entries.</span></span>

</dd> <dt>

<span data-ttu-id="03359-109">*iColours*</span><span class="sxs-lookup"><span data-stu-id="03359-109">*iColours*</span></span> 
</dt> <dd>

<span data-ttu-id="03359-110">Nombre d’entrées de palette dans *pEntry*.</span><span class="sxs-lookup"><span data-stu-id="03359-110">Number of palette entries in *pEntry*.</span></span>

</dd> <dt>

<span data-ttu-id="03359-111">*szDevice*</span><span class="sxs-lookup"><span data-stu-id="03359-111">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="03359-112">Pointeur vers une chaîne qui contient le nom du périphérique d’affichage, tel que retourné par la fonction GDI **EnumDisplayDevices** .</span><span class="sxs-lookup"><span data-stu-id="03359-112">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="03359-113">Pour utiliser le périphérique d’affichage principal, attribuez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="03359-113">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03359-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03359-114">Return value</span></span>

<span data-ttu-id="03359-115">Retourne S \_ OK en cas de réussite ou S \_ false en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="03359-115">Returns S\_OK if successful or S\_FALSE if unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="03359-116">Notes</span><span class="sxs-lookup"><span data-stu-id="03359-116">Remarks</span></span>

<span data-ttu-id="03359-117">Cette méthode compare les entrées réservées de la palette système aux entrées correspondantes dans le tableau *pEntry* .</span><span class="sxs-lookup"><span data-stu-id="03359-117">This method compares the reserved entries in the system palette against the corresponding entries in the *pEntry* array.</span></span> <span data-ttu-id="03359-118">Si elles correspondent exactement, la méthode définit l' \_ indicateur NOcollapse du PC dans les entrées de palette restantes (non réservées) dans *pEntry*.</span><span class="sxs-lookup"><span data-stu-id="03359-118">If they match exactly, the method sets the PC\_NOCOLLAPSE flag in the remaining (non-reserved) palette entries in *pEntry*.</span></span> <span data-ttu-id="03359-119">Cet indicateur empêche GDI de tenter de mapper les entrées de palette logique aux entrées de la palette système.</span><span class="sxs-lookup"><span data-stu-id="03359-119">This flag prevents GDI from trying map logical palette entries to system palette entries.</span></span>

<span data-ttu-id="03359-120">La méthode [**CImagePalette :: MakePalette**](cimagepalette-makepalette.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="03359-120">The [**CImagePalette::MakePalette**](cimagepalette-makepalette.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="03359-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03359-121">Requirements</span></span>



| <span data-ttu-id="03359-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03359-122">Requirement</span></span> | <span data-ttu-id="03359-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="03359-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03359-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="03359-124">Header</span></span><br/>  | <dl> <span data-ttu-id="03359-125"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03359-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="03359-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="03359-126">Library</span></span><br/> | <dl> <span data-ttu-id="03359-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="03359-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03359-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03359-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03359-129">**CImagePalette, classe**</span><span class="sxs-lookup"><span data-stu-id="03359-129">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




