---
description: 'Méthode CBaseRenderer. BeginFlush : la méthode BeginFlush commence une opération de vidage.'
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: Méthode CBaseRenderer. BeginFlush (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76dfd77a5170a83813871143781868cae55c45ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095937"
---
# <a name="cbaserendererbeginflush-method"></a><span data-ttu-id="4db82-103">Méthode CBaseRenderer. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="4db82-103">CBaseRenderer.BeginFlush method</span></span>

<span data-ttu-id="4db82-104">La `BeginFlush` méthode commence une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="4db82-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4db82-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4db82-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="4db82-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4db82-106">Parameters</span></span>

<span data-ttu-id="4db82-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4db82-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4db82-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4db82-108">Return value</span></span>

<span data-ttu-id="4db82-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4db82-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4db82-110">Notes </span><span class="sxs-lookup"><span data-stu-id="4db82-110">Remarks</span></span>

<span data-ttu-id="4db82-111">La broche d’entrée du filtre appelle cette méthode lorsqu’elle reçoit un appel à la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="4db82-111">The filter's input pin calls this method when it receives a call to the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span> <span data-ttu-id="4db82-112">Le filtre libère le thread de diffusion en continu et libère les exemples qu’il détient pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="4db82-112">The filter releases the streaming thread, and releases any sample that it was holding for rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="4db82-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4db82-113">Requirements</span></span>



| <span data-ttu-id="4db82-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4db82-114">Requirement</span></span> | <span data-ttu-id="4db82-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4db82-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4db82-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="4db82-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4db82-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4db82-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4db82-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4db82-118">Library</span></span><br/> | <dl> <span data-ttu-id="4db82-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4db82-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4db82-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4db82-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db82-121">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="4db82-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




