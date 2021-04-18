---
description: La fonction GetBitmapSubtype retourne le GUID du sous-type de média pour la bitmap spécifiée.
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: GetBitmapSubtype, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSubtype
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ba12ffcd1b50b920f28e1969444a2d31a9d073d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540475"
---
# <a name="getbitmapsubtype-function"></a><span data-ttu-id="08c44-103">GetBitmapSubtype fonction)</span><span class="sxs-lookup"><span data-stu-id="08c44-103">GetBitmapSubtype function</span></span>

<span data-ttu-id="08c44-104">La `GetBitmapSubtype` fonction retourne le **GUID** du sous-type de média pour la bitmap spécifiée.</span><span class="sxs-lookup"><span data-stu-id="08c44-104">The `GetBitmapSubtype` function returns the media subtype **GUID** for the specified bitmap.</span></span>

## <a name="syntax"></a><span data-ttu-id="08c44-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08c44-105">Syntax</span></span>


```C++
const GUID GetBitmapSubtype(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="08c44-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08c44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08c44-107">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="08c44-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="08c44-108">Pointeur vers une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="08c44-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08c44-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08c44-109">Return value</span></span>

<span data-ttu-id="08c44-110">Retourne le **GUID** du sous-type de média.</span><span class="sxs-lookup"><span data-stu-id="08c44-110">Returns the media subtype **GUID**.</span></span>

## <a name="remarks"></a><span data-ttu-id="08c44-111">Notes</span><span class="sxs-lookup"><span data-stu-id="08c44-111">Remarks</span></span>

<span data-ttu-id="08c44-112">Pour les types RVB non compressés, cette fonction mappe le champ **biBitCount** au sous-type.</span><span class="sxs-lookup"><span data-stu-id="08c44-112">For uncompressed RGB types, this function maps the **biBitCount** field to the subtype.</span></span> <span data-ttu-id="08c44-113">Pour les types de vidéo compressés, cette fonction utilise la classe [**FOURCCMap**](fourccmap.md) pour mapper le champ de **bicompression** au sous-type.</span><span class="sxs-lookup"><span data-stu-id="08c44-113">For compressed video types, this function uses the [**FOURCCMap**](fourccmap.md) class to map the **biCompression** field to the subtype.</span></span>

<span data-ttu-id="08c44-114">Si la fonction ne peut pas correspondre au format d’un sous-type, la valeur de retour est le GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="08c44-114">If the function cannot match the format to a subtype, the return value is GUID\_NULL.</span></span>

## <a name="requirements"></a><span data-ttu-id="08c44-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08c44-115">Requirements</span></span>



| <span data-ttu-id="08c44-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08c44-116">Requirement</span></span> | <span data-ttu-id="08c44-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="08c44-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08c44-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="08c44-118">Header</span></span><br/>  | <dl> <span data-ttu-id="08c44-119"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08c44-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="08c44-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="08c44-120">Library</span></span><br/> | <dl> <span data-ttu-id="08c44-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="08c44-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08c44-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08c44-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c44-123">Fonctions vidéo et image</span><span class="sxs-lookup"><span data-stu-id="08c44-123">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




