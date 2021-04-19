---
description: La méthode GetFlags récupère les indicateurs de contexte associés à la commande différée.
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: CDeferredCommand. GetFlags, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetFlags
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec9b97e42534d34c5033b3b86edb9c33366d639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521767"
---
# <a name="cdeferredcommandgetflags-method"></a><span data-ttu-id="43c29-103">CDeferredCommand. GetFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="43c29-103">CDeferredCommand.GetFlags method</span></span>

<span data-ttu-id="43c29-104">La `GetFlags` méthode récupère les indicateurs de contexte associés à la commande différée.</span><span class="sxs-lookup"><span data-stu-id="43c29-104">The `GetFlags` method retrieves the context flags associated with the deferred command.</span></span>

## <a name="syntax"></a><span data-ttu-id="43c29-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43c29-105">Syntax</span></span>


```C++
short GetFlags();
```



## <a name="parameters"></a><span data-ttu-id="43c29-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43c29-106">Parameters</span></span>

<span data-ttu-id="43c29-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="43c29-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43c29-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43c29-108">Return value</span></span>

<span data-ttu-id="43c29-109">Retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="43c29-109">Returns one of the following:</span></span>



| <span data-ttu-id="43c29-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="43c29-110">Return code</span></span>                                                                                             | <span data-ttu-id="43c29-111">Description</span><span class="sxs-lookup"><span data-stu-id="43c29-111">Description</span></span>                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43c29-112"><dt>**DISPATCH ( \_ méthode)**</dt></span><span class="sxs-lookup"><span data-stu-id="43c29-112"><dt>**DISPATCH\_METHOD**</dt></span></span> </dl>         | <span data-ttu-id="43c29-113">Exécutez le membre en tant que méthode.</span><span class="sxs-lookup"><span data-stu-id="43c29-113">Run the member as a method.</span></span> <span data-ttu-id="43c29-114">Si une propriété porte le même nom, vous pouvez définir à la fois cet indicateur et l' \_ indicateur PROPERTYGET (Dispatch.</span><span class="sxs-lookup"><span data-stu-id="43c29-114">If a property has the same name, both this and the DISPATCH\_PROPERTYGET flag can be set.</span></span><br/>                                               |
| <dl> <span data-ttu-id="43c29-115"><dt>**DISTRIBUER \_ PropertyGet (**</dt></span><span class="sxs-lookup"><span data-stu-id="43c29-115"><dt>**DISPATCH\_PROPERTYGET**</dt></span></span> </dl>    | <span data-ttu-id="43c29-116">Le membre est récupéré en tant que propriété ou membre de données.</span><span class="sxs-lookup"><span data-stu-id="43c29-116">The member is being retrieved as a property or data member.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="43c29-117"><dt>**DISTRIBUER \_ PROPERTYPUT**</dt></span><span class="sxs-lookup"><span data-stu-id="43c29-117"><dt>**DISPATCH\_PROPERTYPUT**</dt></span></span> </dl>    | <span data-ttu-id="43c29-118">Le membre est modifié en tant que propriété ou membre de données.</span><span class="sxs-lookup"><span data-stu-id="43c29-118">The member is being changed as a property or data member.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="43c29-119"><dt>**DISTRIBUER \_ PROPERTYPUTREF**</dt></span><span class="sxs-lookup"><span data-stu-id="43c29-119"><dt>**DISPATCH\_PROPERTYPUTREF**</dt></span></span> </dl> | <span data-ttu-id="43c29-120">Le membre est modifié via une assignation de référence, plutôt que comme une assignation de valeur.</span><span class="sxs-lookup"><span data-stu-id="43c29-120">The member is being changed via a reference assignment, rather than a value assignment.</span></span> <span data-ttu-id="43c29-121">Cet indicateur est valide uniquement lorsque la propriété accepte une référence à un objet.</span><span class="sxs-lookup"><span data-stu-id="43c29-121">This flag is valid only when the property accepts a reference to an object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="43c29-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43c29-122">Requirements</span></span>



| <span data-ttu-id="43c29-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43c29-123">Requirement</span></span> | <span data-ttu-id="43c29-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="43c29-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43c29-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="43c29-125">Header</span></span><br/>  | <dl> <span data-ttu-id="43c29-126"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43c29-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="43c29-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="43c29-127">Library</span></span><br/> | <dl> <span data-ttu-id="43c29-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="43c29-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43c29-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43c29-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43c29-130">**CDeferredCommand, classe**</span><span class="sxs-lookup"><span data-stu-id="43c29-130">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




