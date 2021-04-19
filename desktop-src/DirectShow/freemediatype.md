---
description: La fonction FreeMediaType supprime le bloc de format dans une \_ structure de type de média am \_ .
ms.assetid: b7ec335e-518d-4aa6-8cde-8cb92184d0b0
title: Fonction FreeMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f332ccc9a60473a9d814481b759221dc6468d5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541687"
---
# <a name="freemediatype-function"></a><span data-ttu-id="0d3f5-103">FreeMediaType fonction)</span><span class="sxs-lookup"><span data-stu-id="0d3f5-103">FreeMediaType function</span></span>

<span data-ttu-id="0d3f5-104">La fonction **FreeMediaType** supprime le bloc de format dans une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="0d3f5-104">The **FreeMediaType** function deletes the format block in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d3f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d3f5-105">Syntax</span></span>


```C++
void FreeMediaType(
   AM_MEDIA_TYPE &mt
);
```



## <a name="parameters"></a><span data-ttu-id="0d3f5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d3f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d3f5-107">*MT* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="0d3f5-107">*mt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="0d3f5-108">Référence à une structure [**de \_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="0d3f5-108">A reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d3f5-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0d3f5-109">Return value</span></span>

<span data-ttu-id="0d3f5-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0d3f5-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d3f5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0d3f5-111">Remarks</span></span>

<span data-ttu-id="0d3f5-112">Le bloc de format est alloué sur le tas.</span><span class="sxs-lookup"><span data-stu-id="0d3f5-112">The format block is allocated on the heap.</span></span> <span data-ttu-id="0d3f5-113">Le membre **pbFormat** du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) pointe vers le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="0d3f5-113">The **pbFormat** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) points to the format block.</span></span> <span data-ttu-id="0d3f5-114">Utilisez cette fonction pour libérer uniquement le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="0d3f5-114">Use this function to free just the format block.</span></span> <span data-ttu-id="0d3f5-115">Pour supprimer une structure **de \_ \_ type de média am** allouée, appelez [**DeleteMediaType**](deletemediatype.md).</span><span class="sxs-lookup"><span data-stu-id="0d3f5-115">To delete an allocated **AM\_MEDIA\_TYPE** structure, call [**DeleteMediaType**](deletemediatype.md).</span></span>

<span data-ttu-id="0d3f5-116">Cette fonction est définie dans la bibliothèque de [classes de base DirectShow](directshow-base-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="0d3f5-116">This function is defined in the [DirectShow Base Classes](directshow-base-classes.md) library.</span></span> <span data-ttu-id="0d3f5-117">Si vous préférez ne pas établir de liaison avec la bibliothèque de classes de base, vous pouvez utiliser le code suivant :</span><span class="sxs-lookup"><span data-stu-id="0d3f5-117">If you prefer not to link to the base class library, you can use the following code:</span></span>


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
```



## <a name="requirements"></a><span data-ttu-id="0d3f5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d3f5-118">Requirements</span></span>



| <span data-ttu-id="0d3f5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d3f5-119">Requirement</span></span> | <span data-ttu-id="0d3f5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d3f5-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d3f5-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d3f5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0d3f5-122"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d3f5-122"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="0d3f5-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0d3f5-123">Library</span></span><br/> | <dl> <span data-ttu-id="0d3f5-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0d3f5-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d3f5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d3f5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d3f5-126">**DeleteMediaType**</span><span class="sxs-lookup"><span data-stu-id="0d3f5-126">**DeleteMediaType**</span></span>](deletemediatype.md)
</dt> <dt>

[<span data-ttu-id="0d3f5-127">**Fonctions de type de média**</span><span class="sxs-lookup"><span data-stu-id="0d3f5-127">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




