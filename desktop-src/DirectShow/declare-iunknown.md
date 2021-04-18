---
description: La \_ macro DECLARE IUnknown déclare les trois méthodes de l’interface de base pour une nouvelle interface.
ms.assetid: 3bf8e830-c923-4c31-8855-88fa08f80422
title: DECLARE_IUNKNOWN (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DECLARE_IUNKNOWN
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4823c1b4bd4832b1047a732bc503f04b4da65483
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528923"
---
# <a name="declare_iunknown"></a><span data-ttu-id="a8421-103">DÉCLARER \_ IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8421-103">DECLARE\_IUNKNOWN</span></span>

<span data-ttu-id="a8421-104">La macro **Declare \_ IUnknown** déclare les trois méthodes de l’interface de base pour une nouvelle interface.</span><span class="sxs-lookup"><span data-stu-id="a8421-104">The **DECLARE\_IUNKNOWN** macro declares the three methods of the base interface for a new interface.</span></span>

<span data-ttu-id="a8421-105">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="a8421-105">**Syntax**</span></span>

``` syntax
#define DECLARE_IUNKNOWN                                        \
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      \
        return GetOwner()->QueryInterface(riid,ppv);            \
    };                                                          \
    STDMETHODIMP_(ULONG) AddRef() {                             \
        return GetOwner()->AddRef();                            \
    };                                                          \
    STDMETHODIMP_(ULONG) Release() {                            \
        return GetOwner()->Release();                           \
    };
```

## <a name="remarks"></a><span data-ttu-id="a8421-106">Notes</span><span class="sxs-lookup"><span data-stu-id="a8421-106">Remarks</span></span>

<span data-ttu-id="a8421-107">Quand vous créez une interface, elle doit dériver de **IUnknown**, qui a trois méthodes : **QueryInterface**, **AddRef** et **Release**.</span><span class="sxs-lookup"><span data-stu-id="a8421-107">When you create a new interface, it must derive from **IUnknown**, which has three methods: **QueryInterface**, **AddRef**, and **Release**.</span></span> <span data-ttu-id="a8421-108">Cette macro simplifie le processus de déclaration en déclarant chacune de ces méthodes pour la nouvelle interface.</span><span class="sxs-lookup"><span data-stu-id="a8421-108">This macro simplifies the declaration process by declaring each of these methods for the new interface.</span></span>

<span data-ttu-id="a8421-109">Cette macro fonctionne uniquement avec les classes qui dérivent, directement ou indirectement, de la classe [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="a8421-109">This macro works only with classes that derive, directly or indirectly, from the [**CUnknown**](cunknown.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8421-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8421-110">Requirements</span></span>



| <span data-ttu-id="a8421-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8421-111">Requirement</span></span> | <span data-ttu-id="a8421-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8421-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8421-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8421-113">Header</span></span><br/>  | <dl> <span data-ttu-id="a8421-114"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8421-114"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a8421-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a8421-115">Library</span></span><br/> | <dl> <span data-ttu-id="a8421-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a8421-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8421-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8421-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8421-118">**Fonctions d’assistance COM**</span><span class="sxs-lookup"><span data-stu-id="a8421-118">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="a8421-119">**CUnknown :: GetOwner**</span><span class="sxs-lookup"><span data-stu-id="a8421-119">**CUnknown::GetOwner**</span></span>](cunknown-getowner.md)
</dt> <dt>

[<span data-ttu-id="a8421-120">Comment implémenter IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8421-120">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 




