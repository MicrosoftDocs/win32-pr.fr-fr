---
description: La classe CRefTime est une classe d’assistance pour la gestion des temps de référence.
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: CRefTime, classe (reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01e83520943abafd814425b6ff3fb53f48775627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532223"
---
# <a name="creftime-class"></a><span data-ttu-id="b16e9-103">CRefTime, classe</span><span class="sxs-lookup"><span data-stu-id="b16e9-103">CRefTime class</span></span>

![hiérarchie de la classe creftime](images/cutil05.png)

<span data-ttu-id="b16e9-105">La `CRefTime` classe est une classe d’assistance pour la gestion des temps de référence.</span><span class="sxs-lookup"><span data-stu-id="b16e9-105">The `CRefTime` class is a helper class for managing reference times.</span></span>

<span data-ttu-id="b16e9-106">Une *heure de référence* est une unité de temps représentée en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="b16e9-106">A *reference time* is a unit of time represented in 100-nanosecond units.</span></span> <span data-ttu-id="b16e9-107">Cette classe partage la même disposition des données que le type de données de [**\_ temps de référence**](reference-time.md) , mais ajoute des méthodes et des opérateurs qui fournissent des fonctions de comparaison, de conversion et arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="b16e9-107">This class shares the same data layout as the [**REFERENCE\_TIME**](reference-time.md) data type, but adds some methods and operators that provide comparison, conversion, and arithmetic functions.</span></span> <span data-ttu-id="b16e9-108">Pour plus d’informations sur les temps de référence, consultez [temps et horloges dans DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="b16e9-108">For more information about reference times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>



| <span data-ttu-id="b16e9-109">Variables membres publiques</span><span class="sxs-lookup"><span data-stu-id="b16e9-109">Public Member Variables</span></span>                                                 | <span data-ttu-id="b16e9-110">Description</span><span class="sxs-lookup"><span data-stu-id="b16e9-110">Description</span></span>                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="b16e9-111">**m \_ heure**</span><span class="sxs-lookup"><span data-stu-id="b16e9-111">**m\_time**</span></span>](creftime-m-time.md)                                      | <span data-ttu-id="b16e9-112">Spécifie la valeur de **\_ temps de référence** .</span><span class="sxs-lookup"><span data-stu-id="b16e9-112">Specifies the **REFERENCE\_TIME** value.</span></span>              |
| <span data-ttu-id="b16e9-113">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="b16e9-113">Public Methods</span></span>                                                          | <span data-ttu-id="b16e9-114">Description</span><span class="sxs-lookup"><span data-stu-id="b16e9-114">Description</span></span>                                           |
| [<span data-ttu-id="b16e9-115">**CRefTime**</span><span class="sxs-lookup"><span data-stu-id="b16e9-115">**CRefTime**</span></span>](creftime-creftime.md)                                   | <span data-ttu-id="b16e9-116">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="b16e9-116">Constructor method.</span></span>                                   |
| [<span data-ttu-id="b16e9-117">**GetUnits**</span><span class="sxs-lookup"><span data-stu-id="b16e9-117">**GetUnits**</span></span>](creftime-getunits.md)                                   | <span data-ttu-id="b16e9-118">Récupère le temps de référence en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="b16e9-118">Retrieves the reference time in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="b16e9-119">**Millisecondes**</span><span class="sxs-lookup"><span data-stu-id="b16e9-119">**Millisecs**</span></span>](creftime-millisecs.md)                                 | <span data-ttu-id="b16e9-120">Convertit la durée de référence en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="b16e9-120">Converts the reference time to milliseconds.</span></span>          |
| <span data-ttu-id="b16e9-121">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="b16e9-121">Operators</span></span>                                                               | <span data-ttu-id="b16e9-122">Description</span><span class="sxs-lookup"><span data-stu-id="b16e9-122">Description</span></span>                                           |
| [<span data-ttu-id="b16e9-123">**\_temps de référence de l’opérateur ()**</span><span class="sxs-lookup"><span data-stu-id="b16e9-123">**operator REFERENCE\_TIME()**</span></span>](creftime-operator-reference-time-.md) | <span data-ttu-id="b16e9-124">Convertit l’objet en un type de données de **\_ temps de référence** .</span><span class="sxs-lookup"><span data-stu-id="b16e9-124">Casts the object to a **REFERENCE\_TIME** data type.</span></span>  |
| [<span data-ttu-id="b16e9-125">**opérateur =**</span><span class="sxs-lookup"><span data-stu-id="b16e9-125">**operator=**</span></span>](creftime-operator-assign.md)                           | <span data-ttu-id="b16e9-126">Affecte une nouvelle heure de référence.</span><span class="sxs-lookup"><span data-stu-id="b16e9-126">Assigns a new reference time.</span></span>                         |
| [<span data-ttu-id="b16e9-127">**opérateur + =**</span><span class="sxs-lookup"><span data-stu-id="b16e9-127">**operator+=**</span></span>](creftime-operator-plus-assign.md)                     | <span data-ttu-id="b16e9-128">Ajoute deux heures de référence.</span><span class="sxs-lookup"><span data-stu-id="b16e9-128">Adds two reference times.</span></span>                             |
| [<span data-ttu-id="b16e9-129">**opérateur =**</span><span class="sxs-lookup"><span data-stu-id="b16e9-129">**operator =**</span></span>](creftime-operator-minus-assign.md)                    | <span data-ttu-id="b16e9-130">Soustrait une heure de référence d’une autre.</span><span class="sxs-lookup"><span data-stu-id="b16e9-130">Subtracts one reference time from another.</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="b16e9-131">Notes</span><span class="sxs-lookup"><span data-stu-id="b16e9-131">Remarks</span></span>

<span data-ttu-id="b16e9-132">L’utilisation de cette classe présente un inconvénient potentiel.</span><span class="sxs-lookup"><span data-stu-id="b16e9-132">There is a potential pitfall with using this class.</span></span> <span data-ttu-id="b16e9-133">Si vous appliquez l’opérateur + = avec un objet **CRefTime** comme opérande de gauche et une variable de type **long** comme opérande de droite, le compilateur convertit implicitement l’opérande de droite en objet **CRefTime** .</span><span class="sxs-lookup"><span data-stu-id="b16e9-133">If you apply the += operator with a **CRefTime** object as the left operand and a variable of type **LONG** as the right operand, the compiler will implicitly coerce the right operand into a **CRefTime** object.</span></span> <span data-ttu-id="b16e9-134">Cette contrainte utilise le constructeur **CRefTime** qui convertit les millisecondes en unités de temps de référence \_ ; par conséquent, l’opérande droit est multiplié par 10 000 :</span><span class="sxs-lookup"><span data-stu-id="b16e9-134">This coercion uses the **CRefTime** constructor that converts milliseconds into REFERENCE\_TIME units; as a result, the right operand is multiplied by 10,000:</span></span>


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



<span data-ttu-id="b16e9-135">Toutefois, le même élément ne se produit pas à l’aide de l’opérateur + :</span><span class="sxs-lookup"><span data-stu-id="b16e9-135">However, the same thing does not happen using the + operator:</span></span>


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a><span data-ttu-id="b16e9-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b16e9-136">Requirements</span></span>



| <span data-ttu-id="b16e9-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b16e9-137">Requirement</span></span> | <span data-ttu-id="b16e9-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="b16e9-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b16e9-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="b16e9-139">Header</span></span><br/>  | <dl> <span data-ttu-id="b16e9-140"><dt>Reftime. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b16e9-140"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b16e9-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b16e9-141">Library</span></span><br/> | <dl> <span data-ttu-id="b16e9-142"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b16e9-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




