---
description: Méthode constructeur CSource. CSource.
ms.assetid: 94a92c1e-9768-4293-8290-a2b1938cd196
title: Constructeur CSource. CSource (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fab398f3f4e3fdd8c23ce1e1c08f5c130478dfb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085357"
---
# <a name="csourcecsource-constructor"></a><span data-ttu-id="0cc71-103">Constructeur CSource. CSource</span><span class="sxs-lookup"><span data-stu-id="0cc71-103">CSource.CSource constructor</span></span>

<span data-ttu-id="0cc71-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="0cc71-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cc71-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cc71-105">Syntax</span></span>


```C++
CSource(
   TCHAR     *pName,
   LPUNKNOWN lpunk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="0cc71-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0cc71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cc71-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="0cc71-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0cc71-108">Pointeur vers une chaîne contenant le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0cc71-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="0cc71-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="0cc71-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cc71-110">*lpunk*</span><span class="sxs-lookup"><span data-stu-id="0cc71-110">*lpunk*</span></span> 
</dt> <dd>

<span data-ttu-id="0cc71-111">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="0cc71-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="0cc71-112">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="0cc71-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="0cc71-113">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="0cc71-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0cc71-114">*identificateur*</span><span class="sxs-lookup"><span data-stu-id="0cc71-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="0cc71-115">Identificateur de classe du filtre.</span><span class="sxs-lookup"><span data-stu-id="0cc71-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0cc71-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cc71-116">Requirements</span></span>



| <span data-ttu-id="0cc71-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cc71-117">Requirement</span></span> | <span data-ttu-id="0cc71-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cc71-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc71-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="0cc71-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0cc71-120"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0cc71-120"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0cc71-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0cc71-121">Library</span></span><br/> | <dl> <span data-ttu-id="0cc71-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0cc71-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cc71-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cc71-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cc71-124">**CSource, classe**</span><span class="sxs-lookup"><span data-stu-id="0cc71-124">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




