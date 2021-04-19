---
description: La méthode BreakConnect libère la broche d’entrée d’une connexion.
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: Méthode CBaseRenderer. BreakConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98c1e01c15740616541706ca4d9da3ab5e66538c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539716"
---
# <a name="cbaserendererbreakconnect-method"></a><span data-ttu-id="3e482-103">Méthode CBaseRenderer. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="3e482-103">CBaseRenderer.BreakConnect method</span></span>

<span data-ttu-id="3e482-104">La `BreakConnect` méthode libère la broche d’entrée à partir d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="3e482-104">The `BreakConnect` method releases the input pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e482-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e482-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="3e482-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e482-106">Parameters</span></span>

<span data-ttu-id="3e482-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3e482-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3e482-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e482-108">Return value</span></span>

<span data-ttu-id="3e482-109">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3e482-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="3e482-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3e482-110">Return code</span></span>                                                                                         | <span data-ttu-id="3e482-111">Description</span><span class="sxs-lookup"><span data-stu-id="3e482-111">Description</span></span>                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="3e482-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="3e482-112"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="3e482-113">Le pin n’était pas connecté.</span><span class="sxs-lookup"><span data-stu-id="3e482-113">The pin was not connected.</span></span><br/>  |
| <dl> <span data-ttu-id="3e482-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3e482-114"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="3e482-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="3e482-115">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="3e482-116"><dt>**VFW \_ E \_ non \_ arrêté**</dt></span><span class="sxs-lookup"><span data-stu-id="3e482-116"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="3e482-117">Le filtre est toujours actif.</span><span class="sxs-lookup"><span data-stu-id="3e482-117">The filter is still active.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3e482-118">Notes</span><span class="sxs-lookup"><span data-stu-id="3e482-118">Remarks</span></span>

<span data-ttu-id="3e482-119">La broche d’entrée du filtre appelle cette méthode à l’intérieur de sa propre `BreakConnect` méthode.</span><span class="sxs-lookup"><span data-stu-id="3e482-119">The filter's input pin calls this method from inside its own `BreakConnect` method.</span></span> <span data-ttu-id="3e482-120">(Pour plus d’informations, consultez [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md).) Le filtre effectue une comptabilité interne, telle que la réinitialisation de l’indicateur de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="3e482-120">(For more information, see [**CBasePin::BreakConnect**](cbasepin-breakconnect.md).) The filter performs some internal bookkeeping, such as resetting the end-of-stream flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e482-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e482-121">Requirements</span></span>



| <span data-ttu-id="3e482-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e482-122">Requirement</span></span> | <span data-ttu-id="3e482-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e482-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e482-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e482-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3e482-125"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e482-125"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3e482-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3e482-126">Library</span></span><br/> | <dl> <span data-ttu-id="3e482-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3e482-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e482-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e482-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e482-129">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="3e482-129">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




