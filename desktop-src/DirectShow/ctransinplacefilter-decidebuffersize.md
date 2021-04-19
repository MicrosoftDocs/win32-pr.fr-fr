---
description: La méthode DecideBufferSize définit les exigences de mémoire tampon de la broche de sortie.
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: Méthode CTransInPlaceFilter. DecideBufferSize (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55227510eee3c1afdcd14ed390edf21eccfcf1de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535923"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a><span data-ttu-id="0fefa-103">Méthode CTransInPlaceFilter. DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="0fefa-103">CTransInPlaceFilter.DecideBufferSize method</span></span>

<span data-ttu-id="0fefa-104">La `DecideBufferSize` méthode définit les exigences de mémoire tampon de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="0fefa-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fefa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fefa-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a><span data-ttu-id="0fefa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0fefa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fefa-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="0fefa-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="0fefa-108">Pointeur vers l’objet [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) utilisé par la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="0fefa-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) object used by the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="0fefa-109">*pProperties*</span><span class="sxs-lookup"><span data-stu-id="0fefa-109">*pProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="0fefa-110">Pointeur vers les propriétés d’allocateur demandées pour le nombre, la taille et l’alignement, comme spécifié par la structure des [**\_ Propriétés de l’allocateur**](/windows/win32/api/strmif/ns-strmif-allocator_properties) .</span><span class="sxs-lookup"><span data-stu-id="0fefa-110">Pointer to the requested allocator properties for count, size, and alignment, as specified by the [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fefa-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0fefa-111">Return value</span></span>

<span data-ttu-id="0fefa-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0fefa-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0fefa-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0fefa-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0fefa-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0fefa-114">Return code</span></span>                                                                            | <span data-ttu-id="0fefa-115">Description</span><span class="sxs-lookup"><span data-stu-id="0fefa-115">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="0fefa-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0fefa-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0fefa-117">Succès</span><span class="sxs-lookup"><span data-stu-id="0fefa-117">Success</span></span><br/> |
| <dl> <span data-ttu-id="0fefa-118"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="0fefa-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0fefa-119">Échec</span><span class="sxs-lookup"><span data-stu-id="0fefa-119">Failure</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0fefa-120">Notes</span><span class="sxs-lookup"><span data-stu-id="0fefa-120">Remarks</span></span>

<span data-ttu-id="0fefa-121">Cette méthode est appelée lorsque la classe **CTransInPlaceFilter** doit fournir une taille de mémoire tampon au filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="0fefa-121">This method is called when the **CTransInPlaceFilter** class needs to provide a buffer size to the downstream filter.</span></span> <span data-ttu-id="0fefa-122">Si le filtre **CTransInPlaceFilter** est déjà connecté en amont, il utilise les propriétés Allocator sur la connexion de code confidentiel amont.</span><span class="sxs-lookup"><span data-stu-id="0fefa-122">If the **CTransInPlaceFilter** filter is already connected upstream, it uses the allocator properties on the upstream pin connection.</span></span> <span data-ttu-id="0fefa-123">Dans le cas contraire, elle définit la taille de la mémoire tampon sur 1 octet comme valeur de détenteur temporaire.</span><span class="sxs-lookup"><span data-stu-id="0fefa-123">Otherwise, it sets the buffer size to 1 byte as a temporary place-holder value.</span></span> <span data-ttu-id="0fefa-124">Lorsque le filtre amont se connecte, la classe **CTransInPlaceFilter** renégocie l’allocateur en aval.</span><span class="sxs-lookup"><span data-stu-id="0fefa-124">When the upstream filter connects, the **CTransInPlaceFilter** class renegotiates the downstream allocator.</span></span> <span data-ttu-id="0fefa-125">Pour plus d’informations sur le processus de connexion de code confidentiel dans cette classe, consultez [**CTransInPlaceFilter, classe**](ctransinplacefilter.md).</span><span class="sxs-lookup"><span data-stu-id="0fefa-125">For more information about the pin connection process in this class, see [**CTransInPlaceFilter Class**](ctransinplacefilter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fefa-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0fefa-126">Requirements</span></span>



| <span data-ttu-id="0fefa-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0fefa-127">Requirement</span></span> | <span data-ttu-id="0fefa-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="0fefa-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fefa-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="0fefa-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0fefa-130"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fefa-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0fefa-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0fefa-131">Library</span></span><br/> | <dl> <span data-ttu-id="0fefa-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0fefa-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fefa-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fefa-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fefa-134">**CTransInPlaceFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="0fefa-134">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




