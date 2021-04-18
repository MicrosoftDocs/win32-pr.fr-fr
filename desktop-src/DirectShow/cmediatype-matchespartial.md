---
description: La méthode MatchesPartial détermine si ce type de média correspond à un type de média partiellement spécifié.
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: Méthode CMediaType. MatchesPartial (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.MatchesPartial
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4d2d4232b64857ca209e6b43cd7081a42495fee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526791"
---
# <a name="cmediatypematchespartial-method"></a><span data-ttu-id="07853-103">Méthode CMediaType. MatchesPartial</span><span class="sxs-lookup"><span data-stu-id="07853-103">CMediaType.MatchesPartial method</span></span>

<span data-ttu-id="07853-104">La `MatchesPartial` méthode détermine si ce type de média correspond à un type de média partiellement spécifié.</span><span class="sxs-lookup"><span data-stu-id="07853-104">The `MatchesPartial` method determines if this media type matches a partially specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="07853-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07853-105">Syntax</span></span>


```C++
BOOL MatchesPartial(
   const CMediaType *ppartial
) const;
```



## <a name="parameters"></a><span data-ttu-id="07853-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07853-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07853-107">*ppartial*</span><span class="sxs-lookup"><span data-stu-id="07853-107">*ppartial*</span></span> 
</dt> <dd>

<span data-ttu-id="07853-108">Pointeur vers le type de média à faire correspondre.</span><span class="sxs-lookup"><span data-stu-id="07853-108">Pointer to the media type to match.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07853-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="07853-109">Return value</span></span>

<span data-ttu-id="07853-110">Retourne la **valeur true** si les types de média correspondent.</span><span class="sxs-lookup"><span data-stu-id="07853-110">Returns **TRUE** if the media types match.</span></span> <span data-ttu-id="07853-111">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="07853-111">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="07853-112">Notes</span><span class="sxs-lookup"><span data-stu-id="07853-112">Remarks</span></span>

<span data-ttu-id="07853-113">Le type de média spécifié par *ppartial* peut avoir la valeur Guid \_ null pour le type principal, le sous-type ou le type de format.</span><span class="sxs-lookup"><span data-stu-id="07853-113">The media type specified by *ppartial* can have a value of GUID\_NULL for the major type, subtype, or format type.</span></span> <span data-ttu-id="07853-114">Les membres avec des \_ valeurs GUID NULL ne sont pas testés.</span><span class="sxs-lookup"><span data-stu-id="07853-114">Any members with GUID\_NULL values are not tested.</span></span> <span data-ttu-id="07853-115">(En fait, GUID \_ NULL agit comme un caractère générique.) Les membres avec des valeurs autres que le GUID \_ null doivent correspondre pour que le type de média corresponde.</span><span class="sxs-lookup"><span data-stu-id="07853-115">(In effect, GUID\_NULL acts as a wildcard.) Members with values other than GUID\_NULL must match for the media type to match.</span></span>

## <a name="requirements"></a><span data-ttu-id="07853-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07853-116">Requirements</span></span>



| <span data-ttu-id="07853-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07853-117">Requirement</span></span> | <span data-ttu-id="07853-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="07853-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07853-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="07853-119">Header</span></span><br/>  | <dl> <span data-ttu-id="07853-120"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07853-120"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="07853-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="07853-121">Library</span></span><br/> | <dl> <span data-ttu-id="07853-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="07853-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07853-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07853-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07853-124">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="07853-124">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




