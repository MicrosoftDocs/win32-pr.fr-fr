---
description: La méthode ajourner spécifie une nouvelle heure de présentation pour une commande précédemment mise en file d’attente.
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: CDeferredCommand. ajourner, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Postpone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9ce19c5391541336f52dd872b44bb9f3a447c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541373"
---
# <a name="cdeferredcommandpostpone-method"></a><span data-ttu-id="ee83e-103">CDeferredCommand. ajourne, méthode</span><span class="sxs-lookup"><span data-stu-id="ee83e-103">CDeferredCommand.Postpone method</span></span>

<span data-ttu-id="ee83e-104">La `Postpone` méthode spécifie une nouvelle heure de présentation pour une commande précédemment mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="ee83e-104">The `Postpone` method specifies a new presentation time for a previously queued command.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee83e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee83e-105">Syntax</span></span>


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a><span data-ttu-id="ee83e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee83e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee83e-107">*newtime*</span><span class="sxs-lookup"><span data-stu-id="ee83e-107">*newtime*</span></span> 
</dt> <dd>

<span data-ttu-id="ee83e-108">Heure de la nouvelle présentation.</span><span class="sxs-lookup"><span data-stu-id="ee83e-108">New presentation time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee83e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ee83e-109">Return value</span></span>

<span data-ttu-id="ee83e-110">Retourne l' \_ heure de VFW E \_ \_ déjà \_ passée si *Newtime* est déjà passé.</span><span class="sxs-lookup"><span data-stu-id="ee83e-110">Returns VFW\_E\_TIME\_ALREADY\_PASSED if *newtime* is already passed.</span></span> <span data-ttu-id="ee83e-111">Sinon, retourne un **HRESULT** résultant d’un appel à [**CCmdQueue :: Remove**](ccmdqueue-remove.md) (lors de l’extraction de la liste) ou [**CCmdQueue :: Insert**](ccmdqueue-insert.md) (lors de la réinsertion avec l’heure modifiée).</span><span class="sxs-lookup"><span data-stu-id="ee83e-111">Otherwise, returns an **HRESULT** resulting from a call to [**CCmdQueue::Remove**](ccmdqueue-remove.md) (when extracting from the list) or [**CCmdQueue::Insert**](ccmdqueue-insert.md) (when reinserting with the changed time).</span></span>

## <a name="remarks"></a><span data-ttu-id="ee83e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ee83e-112">Remarks</span></span>

<span data-ttu-id="ee83e-113">Cette fonction membre implémente la méthode [**IDeferredCommand ::P ostpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) .</span><span class="sxs-lookup"><span data-stu-id="ee83e-113">This member function implements the [**IDeferredCommand::Postpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee83e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee83e-114">Requirements</span></span>



| <span data-ttu-id="ee83e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee83e-115">Requirement</span></span> | <span data-ttu-id="ee83e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee83e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee83e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee83e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ee83e-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee83e-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ee83e-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ee83e-119">Library</span></span><br/> | <dl> <span data-ttu-id="ee83e-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ee83e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee83e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee83e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee83e-122">**CDeferredCommand, classe**</span><span class="sxs-lookup"><span data-stu-id="ee83e-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




