---
description: La classe CUnknown implémente l’interface IUnknown. La plupart des objets COM (Component Object Model) dans DirectShow dérivent de CUnknown.
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: CUnknown, classe (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4818a088119f7cba25ce8a470f63cab722998c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541444"
---
# <a name="cunknown-class"></a><span data-ttu-id="9bc91-104">CUnknown, classe</span><span class="sxs-lookup"><span data-stu-id="9bc91-104">CUnknown class</span></span>

![hiérarchie de la classe CUnknown](images/cbase01.png)

<span data-ttu-id="9bc91-106">La classe **CUnknown** implémente l’interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="9bc91-106">The **CUnknown** class implements the **IUnknown** interface.</span></span> <span data-ttu-id="9bc91-107">La plupart des objets COM (Component Object Model) dans DirectShow dérivent de **CUnknown**.</span><span class="sxs-lookup"><span data-stu-id="9bc91-107">Most Component Object Model (COM) objects in DirectShow derive from **CUnknown**.</span></span>

<span data-ttu-id="9bc91-108">Si vous implémentez un objet COM, vous souhaiterez peut-être le dériver de **CUnknown**.</span><span class="sxs-lookup"><span data-stu-id="9bc91-108">If you implement a COM object, you might want to derive it from **CUnknown**.</span></span> <span data-ttu-id="9bc91-109">La dérivation à partir de **CUnknown** fournit une implémentation thread-safe, ce qui vous évite de rencontrer les problèmes d’implémentation de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="9bc91-109">Deriving from **CUnknown** provides a thread-safe implementation, and saves you the trouble of implementing **IUnknown**.</span></span>

<span data-ttu-id="9bc91-110">Pour obtenir une présentation détaillée de l’utilisation de cette classe de base, consultez [How to implement IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="9bc91-110">For a detailed discussion of how to use this base class, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span> <span data-ttu-id="9bc91-111">Voici un bref résumé :</span><span class="sxs-lookup"><span data-stu-id="9bc91-111">What follows is a brief summary:</span></span>

-   <span data-ttu-id="9bc91-112">Incluez la macro [**Declare \_ IUnknown**](declare-iunknown.md) dans la section public de votre définition de classe.</span><span class="sxs-lookup"><span data-stu-id="9bc91-112">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public section of your class definition.</span></span> <span data-ttu-id="9bc91-113">Cette macro déclare les trois méthodes de l’interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="9bc91-113">This macro declares the three methods of the **IUnknown** interface.</span></span>
-   <span data-ttu-id="9bc91-114">Substituez la méthode [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) pour prendre en charge les interfaces autres que **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="9bc91-114">Override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method to support interfaces other than **IUnknown**.</span></span> <span data-ttu-id="9bc91-115">Dans cette méthode, appelez la fonction [**GetInterface**](getinterface.md) pour récupérer les pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="9bc91-115">Within this method, call the [**GetInterface**](getinterface.md) function to retrieve interface pointers.</span></span>
-   <span data-ttu-id="9bc91-116">Dans votre constructeur de classe, appelez la méthode de constructeur **CUnknown** .</span><span class="sxs-lookup"><span data-stu-id="9bc91-116">In your class constructor, invoke the **CUnknown** constructor method.</span></span>



| <span data-ttu-id="9bc91-117">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="9bc91-117">Protected Member Variables</span></span>                                                  | <span data-ttu-id="9bc91-118">Description</span><span class="sxs-lookup"><span data-stu-id="9bc91-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="9bc91-119">**m \_ cref**</span><span class="sxs-lookup"><span data-stu-id="9bc91-119">**m\_cRef**</span></span>](cunknown-m-cref.md)                                          | <span data-ttu-id="9bc91-120">Nombre de références.</span><span class="sxs-lookup"><span data-stu-id="9bc91-120">Reference count.</span></span>                                                   |
| <span data-ttu-id="9bc91-121">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="9bc91-121">Public Methods</span></span>                                                              | <span data-ttu-id="9bc91-122">Description</span><span class="sxs-lookup"><span data-stu-id="9bc91-122">Description</span></span>                                                        |
| [<span data-ttu-id="9bc91-123">**CUnknown**</span><span class="sxs-lookup"><span data-stu-id="9bc91-123">**CUnknown**</span></span>](cunknown-cunknown.md)                                       | <span data-ttu-id="9bc91-124">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="9bc91-124">Constructor method.</span></span>                                                |
| [<span data-ttu-id="9bc91-125">**~ CUnknown**</span><span class="sxs-lookup"><span data-stu-id="9bc91-125">**~ CUnknown**</span></span>](cunknown--cunknown.md)                                    | <span data-ttu-id="9bc91-126">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="9bc91-126">Destructor method.</span></span> <span data-ttu-id="9bc91-127">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="9bc91-127">Virtual.</span></span>                                        |
| [<span data-ttu-id="9bc91-128">**GetOwner**</span><span class="sxs-lookup"><span data-stu-id="9bc91-128">**GetOwner**</span></span>](cunknown-getowner.md)                                       | <span data-ttu-id="9bc91-129">Obtient un pointeur vers le contrôle **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="9bc91-129">Gets a pointer to the controlling **IUnknown**.</span></span>                    |
| <span data-ttu-id="9bc91-130">Méthodes INonDelegatingUnknown</span><span class="sxs-lookup"><span data-stu-id="9bc91-130">INonDelegatingUnknown Methods</span></span>                                               | <span data-ttu-id="9bc91-131">Description</span><span class="sxs-lookup"><span data-stu-id="9bc91-131">Description</span></span>                                                        |
| [<span data-ttu-id="9bc91-132">**NonDelegatingAddRef**</span><span class="sxs-lookup"><span data-stu-id="9bc91-132">**NonDelegatingAddRef**</span></span>](cunknown-nondelegatingaddref.md)                 | <span data-ttu-id="9bc91-133">Incrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="9bc91-133">Increments the reference count.</span></span>                                    |
| [<span data-ttu-id="9bc91-134">**NonDelegatingQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="9bc91-134">**NonDelegatingQueryInterface**</span></span>](cunknown-nondelegatingqueryinterface.md) | <span data-ttu-id="9bc91-135">Récupère un pointeur d’interface et incrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="9bc91-135">Retrieves an interface pointer and increments the reference count.</span></span> |
| [<span data-ttu-id="9bc91-136">**NonDelegatingRelease**</span><span class="sxs-lookup"><span data-stu-id="9bc91-136">**NonDelegatingRelease**</span></span>](cunknown-nondelegatingrelease.md)               | <span data-ttu-id="9bc91-137">Décrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="9bc91-137">Decrements the reference count.</span></span>                                    |



 

## <a name="requirements"></a><span data-ttu-id="9bc91-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9bc91-138">Requirements</span></span>



| <span data-ttu-id="9bc91-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9bc91-139">Requirement</span></span> | <span data-ttu-id="9bc91-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bc91-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc91-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="9bc91-141">Header</span></span><br/>  | <dl> <span data-ttu-id="9bc91-142"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bc91-142"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9bc91-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9bc91-143">Library</span></span><br/> | <dl> <span data-ttu-id="9bc91-144"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9bc91-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bc91-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bc91-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bc91-146">Classes de base DirectShow</span><span class="sxs-lookup"><span data-stu-id="9bc91-146">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




