---
description: La méthode ReallocFormatBuffer réaffecte le bloc de format à une nouvelle taille.
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: Méthode CMediaType. ReallocFormatBuffer (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.ReallocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22e861c61f01a7594d720833e2b3a4b923a1e183
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532203"
---
# <a name="cmediatypereallocformatbuffer-method"></a><span data-ttu-id="ab318-103">Méthode CMediaType. ReallocFormatBuffer</span><span class="sxs-lookup"><span data-stu-id="ab318-103">CMediaType.ReallocFormatBuffer method</span></span>

<span data-ttu-id="ab318-104">La `ReallocFormatBuffer` méthode réaffecte le bloc de format à une nouvelle taille.</span><span class="sxs-lookup"><span data-stu-id="ab318-104">The `ReallocFormatBuffer` method reallocates the format block to a new size.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab318-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab318-105">Syntax</span></span>


```C++
BYTE* ReallocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="ab318-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab318-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab318-107">*length*</span><span class="sxs-lookup"><span data-stu-id="ab318-107">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="ab318-108">Nouvelle taille requise pour le bloc de format, en octets.</span><span class="sxs-lookup"><span data-stu-id="ab318-108">New size required for the format block, in bytes.</span></span> <span data-ttu-id="ab318-109">Doit être supérieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="ab318-109">Must be greater than zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab318-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab318-110">Return value</span></span>

<span data-ttu-id="ab318-111">Retourne un pointeur vers le nouveau bloc en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="ab318-111">Returns a pointer to the new block if successful.</span></span> <span data-ttu-id="ab318-112">Sinon, retourne un pointeur vers l’ancien bloc de format ou la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ab318-112">Otherwise, returns either a pointer to the old format block, or **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab318-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ab318-113">Remarks</span></span>

<span data-ttu-id="ab318-114">Cette méthode alloue un nouveau bloc de format.</span><span class="sxs-lookup"><span data-stu-id="ab318-114">This method allocates a new format block.</span></span> <span data-ttu-id="ab318-115">Il copie la plus grande partie du bloc de format existant dans le nouveau bloc de format.</span><span class="sxs-lookup"><span data-stu-id="ab318-115">It copies as much of the existing format block as possible into the new format block.</span></span> <span data-ttu-id="ab318-116">Si le nouveau bloc est plus petit que le bloc existant, le bloc de format existant est tronqué.</span><span class="sxs-lookup"><span data-stu-id="ab318-116">If the new block is smaller than the existing block, the existing format block is truncated.</span></span> <span data-ttu-id="ab318-117">Si le nouveau bloc est plus grand, le contenu de l’espace supplémentaire n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="ab318-117">If the new block is larger, the contents of the additional space are undefined.</span></span> <span data-ttu-id="ab318-118">Ils ne sont pas explicitement définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="ab318-118">They are not explicitly set to zero.</span></span>

<span data-ttu-id="ab318-119">La méthode met à jour les membres **cbFormat** et **pbFormat** de la structure du **\_ \_ type de média am** .</span><span class="sxs-lookup"><span data-stu-id="ab318-119">The method updates the **cbFormat** and **pbFormat** members of the **AM\_MEDIA\_TYPE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab318-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab318-120">Requirements</span></span>



| <span data-ttu-id="ab318-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab318-121">Requirement</span></span> | <span data-ttu-id="ab318-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab318-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab318-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab318-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ab318-124"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab318-124"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="ab318-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ab318-125">Library</span></span><br/> | <dl> <span data-ttu-id="ab318-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ab318-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab318-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab318-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab318-128">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="ab318-128">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




