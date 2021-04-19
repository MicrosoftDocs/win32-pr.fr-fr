---
description: La fonction CreateMediaType alloue une nouvelle structure de \_ type de média am \_ , y compris le bloc de format.
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: Fonction CreateMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03ea3eaee03ebf98ac22d702bde9a165fda21e51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531047"
---
# <a name="createmediatype-function"></a><span data-ttu-id="83d6b-103">CreateMediaType fonction)</span><span class="sxs-lookup"><span data-stu-id="83d6b-103">CreateMediaType function</span></span>

<span data-ttu-id="83d6b-104">La fonction **CreateMediaType** alloue une nouvelle structure [**de \_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , y compris le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="83d6b-104">The **CreateMediaType** function allocates a new [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, including the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="83d6b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83d6b-105">Syntax</span></span>


```C++
AM_MEDIA_TYPE* WINAPI CreateMediaType(
   AM_MEDIA_TYPE const *pSrc
);
```



## <a name="parameters"></a><span data-ttu-id="83d6b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83d6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83d6b-107">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="83d6b-107">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="83d6b-108">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="83d6b-108">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="83d6b-109">La méthode copie cette structure dans la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="83d6b-109">The method copies this structure into the new structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83d6b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83d6b-110">Return value</span></span>

<span data-ttu-id="83d6b-111">Retourne une nouvelle structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , ou **null** en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="83d6b-111">Returns a new [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, or **NULL** if there is an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="83d6b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="83d6b-112">Remarks</span></span>

<span data-ttu-id="83d6b-113">Pour libérer la mémoire allouée par cette fonction, appelez [**DeleteMediaType**](deletemediatype.md).</span><span class="sxs-lookup"><span data-stu-id="83d6b-113">To free the memory allocated by this function, call [**DeleteMediaType**](deletemediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83d6b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83d6b-114">Requirements</span></span>



| <span data-ttu-id="83d6b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83d6b-115">Requirement</span></span> | <span data-ttu-id="83d6b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="83d6b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83d6b-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="83d6b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="83d6b-118"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83d6b-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="83d6b-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="83d6b-119">Library</span></span><br/> | <dl> <span data-ttu-id="83d6b-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="83d6b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83d6b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83d6b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83d6b-122">**Fonctions de type de média**</span><span class="sxs-lookup"><span data-stu-id="83d6b-122">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




