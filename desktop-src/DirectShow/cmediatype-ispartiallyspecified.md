---
description: La méthode IsPartiallySpecified détermine si le type de média est partiellement défini. Un type de média est partiel si le type principal, le sous-type ou le type de format est le GUID \_ null.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: Méthode CMediaType. IsPartiallySpecified (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsPartiallySpecified
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32c39942ab3f97d45ecf71ba841d56b7afd4be62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539983"
---
# <a name="cmediatypeispartiallyspecified-method"></a><span data-ttu-id="20691-104">Méthode CMediaType. IsPartiallySpecified</span><span class="sxs-lookup"><span data-stu-id="20691-104">CMediaType.IsPartiallySpecified method</span></span>

<span data-ttu-id="20691-105">La `IsPartiallySpecified` méthode détermine si le type de média est partiellement défini.</span><span class="sxs-lookup"><span data-stu-id="20691-105">The `IsPartiallySpecified` method determines if the media type is partially defined.</span></span> <span data-ttu-id="20691-106">Un type de média est *partiel* si le type principal, le sous-type ou le type de format est le GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="20691-106">A media type is *partial* if the major type, subtype, or format type is GUID\_NULL.</span></span>

## <a name="syntax"></a><span data-ttu-id="20691-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20691-107">Syntax</span></span>


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a><span data-ttu-id="20691-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20691-108">Parameters</span></span>

<span data-ttu-id="20691-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="20691-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20691-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20691-110">Return value</span></span>

<span data-ttu-id="20691-111">Retourne la **valeur true** si le type de média est partiellement spécifié.</span><span class="sxs-lookup"><span data-stu-id="20691-111">Returns **TRUE** if the media type is partially specified.</span></span> <span data-ttu-id="20691-112">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="20691-112">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="20691-113">Notes</span><span class="sxs-lookup"><span data-stu-id="20691-113">Remarks</span></span>

<span data-ttu-id="20691-114">La méthode [**IPIN :: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) peut accepter des types de média partiels.</span><span class="sxs-lookup"><span data-stu-id="20691-114">The [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method can accept partial media types.</span></span>

<span data-ttu-id="20691-115">L’implémentation de ne teste pas réellement le sous-type.</span><span class="sxs-lookup"><span data-stu-id="20691-115">The implementation does not actually test the subtype.</span></span> <span data-ttu-id="20691-116">S’il existe un type de format spécifié, le type de média n’est pas considéré comme partiel, même si le sous-type est un GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="20691-116">If there is a specified format type, the media type is not considered partial, even if the subtype is GUID\_NULL.</span></span>

## <a name="requirements"></a><span data-ttu-id="20691-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20691-117">Requirements</span></span>



| <span data-ttu-id="20691-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20691-118">Requirement</span></span> | <span data-ttu-id="20691-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="20691-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20691-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="20691-120">Header</span></span><br/>  | <dl> <span data-ttu-id="20691-121"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20691-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="20691-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="20691-122">Library</span></span><br/> | <dl> <span data-ttu-id="20691-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="20691-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20691-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20691-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20691-125">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="20691-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




