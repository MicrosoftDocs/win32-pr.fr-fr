---
description: La fonction GetSubtypeName récupère le nom explicite d’un sous-type de vidéo.
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: GetSubtypeName, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSubtypeName
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5cae835a3a7f1b5510d85ecf3f2ae9d15251a45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532004"
---
# <a name="getsubtypename-function"></a><span data-ttu-id="4b3cc-103">GetSubtypeName fonction)</span><span class="sxs-lookup"><span data-stu-id="4b3cc-103">GetSubtypeName function</span></span>

<span data-ttu-id="4b3cc-104">La `GetSubtypeName` fonction récupère le nom explicite d’un sous-type de vidéo.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-104">The `GetSubtypeName` function retrieves the human-readable name of a video subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b3cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b3cc-105">Syntax</span></span>


```C++
TCHAR* GetSubtypeName(
   const GUID *pSubtype
);
```



## <a name="parameters"></a><span data-ttu-id="4b3cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b3cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b3cc-107">*pSubtype*</span><span class="sxs-lookup"><span data-stu-id="4b3cc-107">*pSubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="4b3cc-108">Pointeur vers un **GUID** de sous-type de vidéo.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-108">Pointer to a video subtype **GUID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b3cc-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b3cc-109">Return value</span></span>

<span data-ttu-id="4b3cc-110">Retourne une chaîne contenant le nom.</span><span class="sxs-lookup"><span data-stu-id="4b3cc-110">Returns a string containing the name.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b3cc-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b3cc-111">Requirements</span></span>



| <span data-ttu-id="4b3cc-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b3cc-112">Requirement</span></span> | <span data-ttu-id="4b3cc-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b3cc-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b3cc-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="4b3cc-114">Header</span></span><br/>  | <dl> <span data-ttu-id="4b3cc-115"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b3cc-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4b3cc-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4b3cc-116">Library</span></span><br/> | <dl> <span data-ttu-id="4b3cc-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4b3cc-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b3cc-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b3cc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b3cc-119">Fonctions vidéo et image</span><span class="sxs-lookup"><span data-stu-id="4b3cc-119">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




