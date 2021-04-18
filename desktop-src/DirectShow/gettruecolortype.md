---
description: La fonction GetTrueColorType récupère le nom explicite d’un sous-type de vidéo.
ms.assetid: 479a020c-b55c-44ec-9096-5528113a4b74
title: GetTrueColorType, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTrueColorType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c262031045eed3755fe2d19d3bd703a347e6117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540473"
---
# <a name="gettruecolortype-function"></a><span data-ttu-id="0cb8d-103">GetTrueColorType fonction)</span><span class="sxs-lookup"><span data-stu-id="0cb8d-103">GetTrueColorType function</span></span>

<span data-ttu-id="0cb8d-104">La fonction **GetTrueColorType** récupère le nom explicite d’un sous-type de vidéo.</span><span class="sxs-lookup"><span data-stu-id="0cb8d-104">The **GetTrueColorType** function retrieves the human-readable name of a video subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb8d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cb8d-105">Syntax</span></span>


```C++
const GUID GetTrueColorType(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="0cb8d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0cb8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cb8d-107">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="0cb8d-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="0cb8d-108">Pointeur vers une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) qui définit l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="0cb8d-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure that defines the bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cb8d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0cb8d-109">Return value</span></span>

<span data-ttu-id="0cb8d-110">Retourne MEDIASUBTYPE \_ RGB555 ou MEDIASUBTYPE \_ RGB565.</span><span class="sxs-lookup"><span data-stu-id="0cb8d-110">Returns MEDIASUBTYPE\_RGB555 or MEDIASUBTYPE\_RGB565.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb8d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cb8d-111">Requirements</span></span>



| <span data-ttu-id="0cb8d-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cb8d-112">Requirement</span></span> | <span data-ttu-id="0cb8d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cb8d-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb8d-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="0cb8d-114">Header</span></span><br/>  | <dl> <span data-ttu-id="0cb8d-115"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0cb8d-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0cb8d-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0cb8d-116">Library</span></span><br/> | <dl> <span data-ttu-id="0cb8d-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0cb8d-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cb8d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cb8d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb8d-119">Fonctions vidéo et image</span><span class="sxs-lookup"><span data-stu-id="0cb8d-119">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




