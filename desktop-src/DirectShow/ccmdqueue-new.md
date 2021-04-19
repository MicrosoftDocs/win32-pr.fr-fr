---
description: La nouvelle méthode initialise une commande à exécuter et retourne un nouvel objet CDeferredCommand.
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: CCmdQueue. New, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.New
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 58c3aee63005010b9ed7366cfb63a69fcc7348b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539190"
---
# <a name="ccmdqueuenew-method"></a><span data-ttu-id="0b3b4-103">CCmdQueue. New, méthode</span><span class="sxs-lookup"><span data-stu-id="0b3b4-103">CCmdQueue.New method</span></span>

<span data-ttu-id="0b3b4-104">La `New` méthode initialise une commande à exécuter et retourne un nouvel objet [**CDeferredCommand**](cdeferredcommand.md) .</span><span class="sxs-lookup"><span data-stu-id="0b3b4-104">The `New` method initializes a command to be run and returns a new [**CDeferredCommand**](cdeferredcommand.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b3b4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b3b4-105">Syntax</span></span>


```C++
virtual HRESULT New(
   CDeferredCommand **ppCmd,
   LPUNKNOWN        pUnk,
   REFTIME          time,
   GUID             *iid,
   long             dispidMethod,
   short            wFlags,
   long             cArgs,
   VARIANT          *pDispParams,
   VARIANT          *pvarResult,
   short            *puArgErr,
   BOOL             bStream
);
```



## <a name="parameters"></a><span data-ttu-id="0b3b4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b3b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b3b4-107">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="0b3b4-107">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3b4-108">Adresse d’un pointeur vers un objet [**CDeferredCommand**](cdeferredcommand.md) par lequel une application peut annuler la commande, définir une nouvelle heure de présentation pour celle-ci ou récupérer des informations d’estimation.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-108">Address of a pointer to a [**CDeferredCommand**](cdeferredcommand.md) object by which an application can cancel the command, set a new presentation time for it, or retrieve estimate information.</span></span>

</dd> <dt>

<span data-ttu-id="0b3b4-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="0b3b4-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3b4-110">Pointeur vers l’objet qui exécutera la commande.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-110">Pointer to the object that will run the command.</span></span>

</dd> <dt>

<span data-ttu-id="0b3b4-111">*time*</span><span class="sxs-lookup"><span data-stu-id="0b3b4-111">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3b4-112">Heure à laquelle exécuter la ou les commandes mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-112">Time at which to run the queued command or commands.</span></span>

</dd> <dt>

<span data-ttu-id="0b3b4-113">*vaut*</span><span class="sxs-lookup"><span data-stu-id="0b3b4-113">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3b4-114">Pointeur vers l’identificateur global unique (**GUID**) de l’interface à appeler.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-114">Pointer to the globally unique identifier (**GUID**) of the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="0b3b4-115">*dispidMethod*</span><span class="sxs-lookup"><span data-stu-id="0b3b4-115">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3b4-116">Méthode sur l’interface à appeler.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-116">Method on the interface to be called.</span></span>

</dd> <dt>

<span data-ttu-id="0b3b4-117">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="0b3b4-117">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3b4-118">Indicateurs décrivant le contexte de l'appel.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-118">Flags describing the context of the call.</span></span> <span data-ttu-id="0b3b4-119">Ce paramètre prend en charge les mêmes indicateurs que la méthode **IDispatch :: Invoke** .</span><span class="sxs-lookup"><span data-stu-id="0b3b4-119">This parameter supports the same flags as the **IDispatch::Invoke** method.</span></span>

</dd> <dt>

<span data-ttu-id="0b3b4-120">*cArgs*</span><span class="sxs-lookup"><span data-stu-id="0b3b4-120">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3b4-121">Nombre d’arguments passés.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-121">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="0b3b4-122">*pDispParams*</span><span class="sxs-lookup"><span data-stu-id="0b3b4-122">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3b4-123">Pointeur vers la liste des types variant associés aux paramètres de dispatch.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-123">Pointer to the list of variant types associated with the dispatch parameters.</span></span>

</dd> <dt>

<span data-ttu-id="0b3b4-124">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="0b3b4-124">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3b4-125">Pointeur vers la liste où les résultats, le cas échéant, doivent être retournés.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-125">Pointer to the list where results, if any, are to be returned.</span></span>

</dd> <dt>

<span data-ttu-id="0b3b4-126">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="0b3b4-126">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3b4-127">Pointeur vers l’index dans la liste de paramètres *pDispParams* où la dernière erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-127">Pointer to the index within the *pDispParams* parameter list where the last error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0b3b4-128">*bStream*</span><span class="sxs-lookup"><span data-stu-id="0b3b4-128">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3b4-129">Valeur indiquant si le paramètre de *temps* est une valeur de flux de temps (**true**) ou une valeur d’heure de présentation (**false**).</span><span class="sxs-lookup"><span data-stu-id="0b3b4-129">Value indicating whether the *time* parameter is a stream-time value (**TRUE**) or a presentation-time value (**FALSE**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b3b4-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b3b4-130">Return value</span></span>

<span data-ttu-id="0b3b4-131">Retourne S \_ OK en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-131">Returns S\_OK if successful.</span></span> <span data-ttu-id="0b3b4-132">Retourne E \_ OUTOFMEMORY si *ppCmd* renvoie de la création du nouvel objet [**CDeferredCommand**](cdeferredcommand.md) avec la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-132">Returns E\_OUTOFMEMORY if *ppCmd* returns from creating the new [**CDeferredCommand**](cdeferredcommand.md) object with a value of **NULL**.</span></span> <span data-ttu-id="0b3b4-133">Sinon, retourne un **HRESULT** qui indique une erreur lors de la tentative de création d’un nouvel objet **CDeferredCommand** .</span><span class="sxs-lookup"><span data-stu-id="0b3b4-133">Otherwise, returns an **HRESULT** that indicates an error from attempting to create a new **CDeferredCommand** object.</span></span> <span data-ttu-id="0b3b4-134">En cas d’erreur, aucun objet n’a été mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-134">If there is an error, no object has been queued.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b3b4-135">Notes</span><span class="sxs-lookup"><span data-stu-id="0b3b4-135">Remarks</span></span>

<span data-ttu-id="0b3b4-136">Le nouvel objet [**CDeferredCommand**](cdeferredcommand.md) sera initialisé avec les paramètres et sera ajouté à la file d’attente pendant la construction.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-136">The new [**CDeferredCommand**](cdeferredcommand.md) object will be initialized with the parameters and will be added to the queue during construction.</span></span> <span data-ttu-id="0b3b4-137">Cette méthode est similaire à la méthode **IDispatch :: Invoke** .</span><span class="sxs-lookup"><span data-stu-id="0b3b4-137">This method is similar to the **IDispatch::Invoke** method.</span></span>

<span data-ttu-id="0b3b4-138">Les valeurs du paramètre *wFlags* sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b3b4-138">Values for the *wFlags* parameter include the following:</span></span>



| <span data-ttu-id="0b3b4-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b3b4-139">Value</span></span>                    | <span data-ttu-id="0b3b4-140">Description</span><span class="sxs-lookup"><span data-stu-id="0b3b4-140">Description</span></span>                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b3b4-141">DISPATCH ( \_ méthode)</span><span class="sxs-lookup"><span data-stu-id="0b3b4-141">DISPATCH\_METHOD</span></span>         | <span data-ttu-id="0b3b4-142">Le membre est exécuté en tant que méthode.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-142">The member is being run as a method.</span></span> <span data-ttu-id="0b3b4-143">Si une propriété porte le même nom, vous pouvez définir à la fois cet indicateur et l' \_ indicateur PROPERTYGET (Dispatch.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-143">If a property has the same name, both this and the DISPATCH\_PROPERTYGET flag can be set.</span></span>                                       |
| <span data-ttu-id="0b3b4-144">DISTRIBUER \_ PropertyGet (</span><span class="sxs-lookup"><span data-stu-id="0b3b4-144">DISPATCH\_PROPERTYGET</span></span>    | <span data-ttu-id="0b3b4-145">Le membre est récupéré en tant que propriété ou membre de données.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-145">The member is being retrieved as a property or data member.</span></span>                                                                                                          |
| <span data-ttu-id="0b3b4-146">DISTRIBUER \_ PROPERTYPUT</span><span class="sxs-lookup"><span data-stu-id="0b3b4-146">DISPATCH\_PROPERTYPUT</span></span>    | <span data-ttu-id="0b3b4-147">Le membre est modifié en tant que propriété ou membre de données.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-147">The member is being changed as a property or data member.</span></span>                                                                                                            |
| <span data-ttu-id="0b3b4-148">DISTRIBUER \_ PROPERTYPUTREF</span><span class="sxs-lookup"><span data-stu-id="0b3b4-148">DISPATCH\_PROPERTYPUTREF</span></span> | <span data-ttu-id="0b3b4-149">Le membre est modifié via une assignation de référence, plutôt que comme une assignation de valeur.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-149">The member is being changed via a reference assignment, rather than a value assignment.</span></span> <span data-ttu-id="0b3b4-150">Cette valeur est valide uniquement lorsque la propriété accepte une référence à un objet.</span><span class="sxs-lookup"><span data-stu-id="0b3b4-150">This value is valid only when the property accepts a reference to an object.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0b3b4-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b3b4-151">Requirements</span></span>



| <span data-ttu-id="0b3b4-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b3b4-152">Requirement</span></span> | <span data-ttu-id="0b3b4-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b3b4-153">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b3b4-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b3b4-154">Header</span></span><br/>  | <dl> <span data-ttu-id="0b3b4-155"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b3b4-155"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0b3b4-156">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0b3b4-156">Library</span></span><br/> | <dl> <span data-ttu-id="0b3b4-157"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0b3b4-157"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b3b4-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b3b4-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b3b4-159">**CCmdQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="0b3b4-159">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




