---
description: La fonction DeleteMediaType supprime une structure de type de média AM allouée \_ \_ , y compris le bloc de format.
ms.assetid: 970f6b2b-2bf5-418d-b4ae-637561cd6765
title: Fonction DeleteMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db0de399ab1be7808370a6d0da57c4c3ca7b8de1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532809"
---
# <a name="deletemediatype-function"></a><span data-ttu-id="f4da4-103">DeleteMediaType fonction)</span><span class="sxs-lookup"><span data-stu-id="f4da4-103">DeleteMediaType function</span></span>

<span data-ttu-id="f4da4-104">La fonction **DeleteMediaType** supprime une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) allouée, y compris le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="f4da4-104">The **DeleteMediaType** function deletes an allocated [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, including the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4da4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4da4-105">Syntax</span></span>


```C++
void WINAPI DeleteMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="f4da4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4da4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4da4-107">*crédit*</span><span class="sxs-lookup"><span data-stu-id="f4da4-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="f4da4-108">Pointeur vers une structure [**de \_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="f4da4-108">A pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4da4-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f4da4-109">Return value</span></span>

<span data-ttu-id="f4da4-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f4da4-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4da4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f4da4-111">Remarks</span></span>

<span data-ttu-id="f4da4-112">Utilisez cette fonction pour libérer toute structure de type de média qui a été allouée à l’aide de [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) ou [**CreateMediaType**](createmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="f4da4-112">Use this function to release any media type structure that was allocated using either [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) or [**CreateMediaType**](createmediatype.md).</span></span>

<span data-ttu-id="f4da4-113">Cette fonction est définie dans la bibliothèque de [classes de base DirectShow](directshow-base-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="f4da4-113">This function is defined in the [DirectShow Base Classes](directshow-base-classes.md) library.</span></span> <span data-ttu-id="f4da4-114">Si vous préférez ne pas établir de liaison avec la bibliothèque de classes de base, vous pouvez utiliser le code suivant :</span><span class="sxs-lookup"><span data-stu-id="f4da4-114">If you prefer not to link to the base class library, you can use the following code:</span></span>


```C++
// Release the format block for a media type.

void _FreeMediaType(AM_MEDIA_TYPE& mt)
{
    if (mt.cbFormat != 0)
    {
        CoTaskMemFree((PVOID)mt.pbFormat);
        mt.cbFormat = 0;
        mt.pbFormat = NULL;
    }
    if (mt.pUnk != NULL)
    {
        // pUnk should not be used.
        mt.pUnk->Release();
        mt.pUnk = NULL;
    }
}


// Delete a media type structure that was allocated on the heap.
void _DeleteMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt != NULL)
    {
        _FreeMediaType(*pmt); 
        CoTaskMemFree(pmt);
    }
}
```





## <a name="requirements"></a><span data-ttu-id="f4da4-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4da4-115">Requirements</span></span>



| <span data-ttu-id="f4da4-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4da4-116">Requirement</span></span> | <span data-ttu-id="f4da4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4da4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4da4-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4da4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f4da4-119"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4da4-119"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="f4da4-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f4da4-120">Library</span></span><br/> | <dl> <span data-ttu-id="f4da4-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f4da4-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4da4-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4da4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4da4-123">**FreeMediaType**</span><span class="sxs-lookup"><span data-stu-id="f4da4-123">**FreeMediaType**</span></span>](freemediatype.md)
</dt> <dt>

[<span data-ttu-id="f4da4-124">**Fonctions de type de média**</span><span class="sxs-lookup"><span data-stu-id="f4da4-124">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

