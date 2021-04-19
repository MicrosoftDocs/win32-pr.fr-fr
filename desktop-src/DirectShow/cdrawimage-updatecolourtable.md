---
description: La méthode UpdateColourTable met à jour la table des couleurs avec une nouvelle palette.
ms.assetid: 61ad98c6-a526-4aac-ad68-d44fadc668de
title: Méthode CDrawImage. UpdateColourTable (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UpdateColourTable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fcffdf9e7deaaac5a01f6559ee557c978fcda88f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537709"
---
# <a name="cdrawimageupdatecolourtable-method"></a><span data-ttu-id="de0fd-103">Méthode CDrawImage. UpdateColourTable</span><span class="sxs-lookup"><span data-stu-id="de0fd-103">CDrawImage.UpdateColourTable method</span></span>

<span data-ttu-id="de0fd-104">La `UpdateColourTable` méthode met à jour la table des couleurs avec une nouvelle palette.</span><span class="sxs-lookup"><span data-stu-id="de0fd-104">The `UpdateColourTable` method updates the color table with a new palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="de0fd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de0fd-105">Syntax</span></span>


```C++
void UpdateColourTable(
   HDC              hdc,
   BITMAPINFOHEADER *pbmi
);
```



## <a name="parameters"></a><span data-ttu-id="de0fd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de0fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de0fd-107">*HDC*</span><span class="sxs-lookup"><span data-stu-id="de0fd-107">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="de0fd-108">Contexte de périphérique contenant l’image.</span><span class="sxs-lookup"><span data-stu-id="de0fd-108">Device context containing the image.</span></span>

</dd> <dt>

<span data-ttu-id="de0fd-109">*pbmi*</span><span class="sxs-lookup"><span data-stu-id="de0fd-109">*pbmi*</span></span> 
</dt> <dd>

<span data-ttu-id="de0fd-110">Pointeur vers une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) contenant la nouvelle palette.</span><span class="sxs-lookup"><span data-stu-id="de0fd-110">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure containing the new palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de0fd-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de0fd-111">Return value</span></span>

<span data-ttu-id="de0fd-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="de0fd-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="de0fd-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de0fd-113">Requirements</span></span>



| <span data-ttu-id="de0fd-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de0fd-114">Requirement</span></span> | <span data-ttu-id="de0fd-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="de0fd-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de0fd-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="de0fd-116">Header</span></span><br/>  | <dl> <span data-ttu-id="de0fd-117"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de0fd-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="de0fd-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="de0fd-118">Library</span></span><br/> | <dl> <span data-ttu-id="de0fd-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="de0fd-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de0fd-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de0fd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de0fd-121">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="de0fd-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




