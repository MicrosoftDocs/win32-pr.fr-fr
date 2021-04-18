---
description: La classe LockIt est une classe interne qui verrouille et déverrouille la classe DMO.
ms.assetid: f516ce22-17ad-488e-a768-3f3849c56087
title: 'IMediaObjectImpl :: LockIt, classe (Dmoimpl. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24fe896ea293ec5e60b038f908cab794274d26e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526021"
---
# <a name="imediaobjectimpllockit-class"></a><span data-ttu-id="aff18-103">IMediaObjectImpl :: LockIt, classe</span><span class="sxs-lookup"><span data-stu-id="aff18-103">IMediaObjectImpl::LockIt Class</span></span>

<span data-ttu-id="aff18-104">La `LockIt` classe est une classe interne qui verrouille et déverrouille la classe DMO.</span><span class="sxs-lookup"><span data-stu-id="aff18-104">The `LockIt` class is an internal class that locks and unlocks the DMO.</span></span>

``` syntax
LockIt(
    _DERIVED_ *p
);
```

## <a name="parameters"></a><span data-ttu-id="aff18-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aff18-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aff18-106"><span id="p"></span><span id="P"></span>*p*</span><span class="sxs-lookup"><span data-stu-id="aff18-106"><span id="p"></span><span id="P"></span>*p*</span></span>
</dt> <dd>

<span data-ttu-id="aff18-107">Pointeur vers l’objet dérivé.</span><span class="sxs-lookup"><span data-stu-id="aff18-107">Pointer to the derived object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aff18-108">Notes</span><span class="sxs-lookup"><span data-stu-id="aff18-108">Remarks</span></span>

<span data-ttu-id="aff18-109">Le `LockIt` constructeur verrouille la DMO, et le destructeur déverrouille la DMO.</span><span class="sxs-lookup"><span data-stu-id="aff18-109">The `LockIt` constructor locks the DMO, and the destructor unlocks the DMO.</span></span> <span data-ttu-id="aff18-110">Pour verrouiller l’objet à l’intérieur de votre classe dérivée, déclarez une variable locale de type `LockIt` .</span><span class="sxs-lookup"><span data-stu-id="aff18-110">To lock the object from inside your derived class, declare a local variable of type `LockIt`.</span></span> <span data-ttu-id="aff18-111">Le DMO est verrouillé alors que l' `LockIt` objet reste dans la portée :</span><span class="sxs-lookup"><span data-stu-id="aff18-111">The DMO is locked while the `LockIt` object remains in scope:</span></span>


```C++
void SomeMethod()
{
    // The DMO is not locked.
    {
        LockIt dmoLock(this); // Locks the DMO.
        /* ... */
    } 
    // dmoLock goes out of scope, DMO is unlocked.
}
```



<span data-ttu-id="aff18-112">Les méthodes dans **IMediaObjectImpl** verrouillent automatiquement la méthode DMO.</span><span class="sxs-lookup"><span data-stu-id="aff18-112">The methods in **IMediaObjectImpl** automatically lock the DMO.</span></span>

## <a name="requirements"></a><span data-ttu-id="aff18-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aff18-113">Requirements</span></span>



| <span data-ttu-id="aff18-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aff18-114">Requirement</span></span> | <span data-ttu-id="aff18-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="aff18-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aff18-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="aff18-116">Header</span></span><br/>  | <dl> <span data-ttu-id="aff18-117"><dt>Dmoimpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aff18-117"><dt>Dmoimpl.h</dt></span></span> </dl>                                                                     |
| <span data-ttu-id="aff18-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aff18-118">Library</span></span><br/> | <dl> <span data-ttu-id="aff18-119"><dt>Dmoguids. lib ; </dt> <dt>Msdmo. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aff18-119"><dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff18-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aff18-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff18-121">**Modèle de classe IMediaObjectImpl**</span><span class="sxs-lookup"><span data-stu-id="aff18-121">**IMediaObjectImpl Class Template**</span></span>](imediaobjectimpl-class-template.md)
</dt> </dl>

 

 




