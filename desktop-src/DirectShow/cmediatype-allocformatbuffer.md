---
description: La méthode AllocFormatBuffer alloue de la mémoire pour le bloc de format.
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: Méthode CMediaType. AllocFormatBuffer (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.AllocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6a9314fd06734adcc367b7be34dc8d6d1b9d996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532702"
---
# <a name="cmediatypeallocformatbuffer-method"></a><span data-ttu-id="dece7-103">Méthode CMediaType. AllocFormatBuffer</span><span class="sxs-lookup"><span data-stu-id="dece7-103">CMediaType.AllocFormatBuffer method</span></span>

<span data-ttu-id="dece7-104">La `AllocFormatBuffer` méthode alloue de la mémoire pour le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="dece7-104">The `AllocFormatBuffer` method allocates memory for the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="dece7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dece7-105">Syntax</span></span>


```C++
BYTE* AllocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="dece7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dece7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dece7-107">*length*</span><span class="sxs-lookup"><span data-stu-id="dece7-107">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="dece7-108">Taille requise pour le bloc de format, en octets.</span><span class="sxs-lookup"><span data-stu-id="dece7-108">Size required for the format block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dece7-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dece7-109">Return value</span></span>

<span data-ttu-id="dece7-110">Retourne un pointeur vers le nouveau bloc en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="dece7-110">Returns a pointer to the new block if successful.</span></span> <span data-ttu-id="dece7-111">Sinon, retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="dece7-111">Otherwise, returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dece7-112">Notes</span><span class="sxs-lookup"><span data-stu-id="dece7-112">Remarks</span></span>

<span data-ttu-id="dece7-113">Si la méthode alloue correctement un nouveau bloc de format, il libère le bloc de format existant.</span><span class="sxs-lookup"><span data-stu-id="dece7-113">If the method successfully allocates a new format block, it frees the existing format block.</span></span> <span data-ttu-id="dece7-114">Si l’allocation échoue, la méthode laisse le bloc de format existant.</span><span class="sxs-lookup"><span data-stu-id="dece7-114">If the allocation fails, the method leaves the existing format block.</span></span>

<span data-ttu-id="dece7-115">La méthode met à jour les membres **cbFormat** et **pbFormat** de la structure du **\_ \_ type de média am** .</span><span class="sxs-lookup"><span data-stu-id="dece7-115">The method updates the **cbFormat** and **pbFormat** members of the **AM\_MEDIA\_TYPE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="dece7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dece7-116">Requirements</span></span>



| <span data-ttu-id="dece7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dece7-117">Requirement</span></span> | <span data-ttu-id="dece7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="dece7-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dece7-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="dece7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="dece7-120"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dece7-120"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="dece7-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dece7-121">Library</span></span><br/> | <dl> <span data-ttu-id="dece7-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dece7-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dece7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dece7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dece7-124">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="dece7-124">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




