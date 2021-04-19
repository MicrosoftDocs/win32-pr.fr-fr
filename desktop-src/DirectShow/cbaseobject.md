---
description: La classe CBaseObject est une classe abstraite pour l’implémentation d’objets DirectShow. Pour implémenter des objets COM (Component Object Model), utilisez la classe CUnknown, qui dérive de CBaseObject.
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: CBaseObject, classe (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbc3e072c31618dab6a7bc07048728f60dbcf0d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532812"
---
# <a name="cbaseobject-class"></a><span data-ttu-id="c492d-104">CBaseObject, classe</span><span class="sxs-lookup"><span data-stu-id="c492d-104">CBaseObject class</span></span>

<span data-ttu-id="c492d-105">La classe **CBaseObject** est une classe abstraite pour l’implémentation d’objets DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c492d-105">The **CBaseObject** class is an abstract class for implementing DirectShow objects.</span></span> <span data-ttu-id="c492d-106">Pour implémenter des objets COM (Component Object Model), utilisez la classe [**CUnknown**](cunknown.md) , qui dérive de **CBaseObject**.</span><span class="sxs-lookup"><span data-stu-id="c492d-106">To implement Component Object Model (COM) objects, use the [**CUnknown**](cunknown.md) class, which derives from **CBaseObject**.</span></span>



| <span data-ttu-id="c492d-107">Méthodes de classe</span><span class="sxs-lookup"><span data-stu-id="c492d-107">Class Methods</span></span>                                      | <span data-ttu-id="c492d-108">Description</span><span class="sxs-lookup"><span data-stu-id="c492d-108">Description</span></span>                            |
|----------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="c492d-109">**CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="c492d-109">**CBaseObject**</span></span>](cbaseobject-cbaseobject.md)     | <span data-ttu-id="c492d-110">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="c492d-110">Constructor method.</span></span>                    |
| [<span data-ttu-id="c492d-111">**~ CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="c492d-111">**~CBaseObject**</span></span>](cbaseobject--cbaseobject.md)   | <span data-ttu-id="c492d-112">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="c492d-112">Destructor method.</span></span>                     |
| [<span data-ttu-id="c492d-113">**ObjectsActive**</span><span class="sxs-lookup"><span data-stu-id="c492d-113">**ObjectsActive**</span></span>](cbaseobject-objectsactive.md) | <span data-ttu-id="c492d-114">Récupère le nombre d’objets actifs.</span><span class="sxs-lookup"><span data-stu-id="c492d-114">Retrieves the count of active objects.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c492d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c492d-115">Remarks</span></span>

<span data-ttu-id="c492d-116">La plupart des classes de base DirectShow dérivent de **CBaseObject**.</span><span class="sxs-lookup"><span data-stu-id="c492d-116">Most of the DirectShow base classes derive from **CBaseObject**.</span></span> <span data-ttu-id="c492d-117">Cette classe fournit une assistance en matière de débogage en conservant le décompte de tous les objets DirectShow actifs au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="c492d-117">This class provides debugging assistance by keeping a count of all the DirectShow objects active during run time.</span></span> <span data-ttu-id="c492d-118">Le nombre d’objets est stocké dans une variable membre statique de classe :</span><span class="sxs-lookup"><span data-stu-id="c492d-118">The object count is stored in a class-static member variable:</span></span>


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



<span data-ttu-id="c492d-119">Dans les versions Debug, la DLL déclarera si elle est déchargée alors que le nombre d’objets est supérieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="c492d-119">In debug builds, the DLL will assert if it is unloaded while the object count is greater than zero.</span></span> <span data-ttu-id="c492d-120">Cela facilite le suivi des fuites provoquées par des problèmes de comptage des références.</span><span class="sxs-lookup"><span data-stu-id="c492d-120">This makes it easier to track down leaks caused by reference-counting problems.</span></span>

<span data-ttu-id="c492d-121">Le constructeur **CBaseObject** prend un argument, un nom de débogage pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="c492d-121">The **CBaseObject** constructor takes one argument, a debugging name for the object.</span></span> <span data-ttu-id="c492d-122">Ce nom est stocké dans une table globale de la DLL.</span><span class="sxs-lookup"><span data-stu-id="c492d-122">This name is stored in a global table in the DLL.</span></span> <span data-ttu-id="c492d-123">La fonction [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) met en forme une liste des objets actifs dans la dll et l’envoie à la sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="c492d-123">The [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) function formats a list of the objects active in the DLL, and sends it to the debug output.</span></span>

## <a name="requirements"></a><span data-ttu-id="c492d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c492d-124">Requirements</span></span>



| <span data-ttu-id="c492d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c492d-125">Requirement</span></span> | <span data-ttu-id="c492d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c492d-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c492d-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="c492d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c492d-128"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c492d-128"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c492d-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c492d-129">Library</span></span><br/> | <dl> <span data-ttu-id="c492d-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c492d-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c492d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c492d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c492d-132">Classes de base DirectShow</span><span class="sxs-lookup"><span data-stu-id="c492d-132">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




