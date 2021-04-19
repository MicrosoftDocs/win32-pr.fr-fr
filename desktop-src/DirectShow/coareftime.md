---
description: La classe COARefTime convertit les temps de référence entre les secondes et les unités de 100 nanosecondes.
ms.assetid: 724420fc-9252-468f-9516-174be0a82999
title: COARefTime, classe (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851495d69a1e34bd1723c20f88dc4bb86b7a8025
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539547"
---
# <a name="coareftime-class"></a><span data-ttu-id="eda0e-103">COARefTime, classe</span><span class="sxs-lookup"><span data-stu-id="eda0e-103">COARefTime class</span></span>

![hiérarchie de la classe coareftime](images/cutil05.png)

<span data-ttu-id="eda0e-105">La `COARefTime` classe convertit les temps de référence entre les secondes et les unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="eda0e-105">The `COARefTime` class converts reference times between seconds and 100-nanosecond units.</span></span>

<span data-ttu-id="eda0e-106">Cette classe effectue une conversion entre les temps de référence qui sont compatibles avec l’automatisation et les temps de référence compatibles avec C/C++.</span><span class="sxs-lookup"><span data-stu-id="eda0e-106">This class converts between reference times that are compatible with Automation and reference times that are compatible with C/C++.</span></span> <span data-ttu-id="eda0e-107">Les interfaces compatibles Automation utilisent des valeurs **double** pour représenter le temps en secondes.</span><span class="sxs-lookup"><span data-stu-id="eda0e-107">Automation-compatible interfaces use **double** values to represent time in seconds.</span></span> <span data-ttu-id="eda0e-108">Les autres interfaces utilisent des valeurs **LongLong** bits 64 pour représenter le temps en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="eda0e-108">Other interfaces use 64-bit **LONGLONG** values to represent time in 100-nanosecond units.</span></span> <span data-ttu-id="eda0e-109">Les types suivants sont définis pour ces valeurs :</span><span class="sxs-lookup"><span data-stu-id="eda0e-109">The following types are defined for these values:</span></span>

``` syntax
typedef LONGLONG  REFERENCE_TIME;
typedef double    REFTIME;
```

<span data-ttu-id="eda0e-110">Les filtres peuvent utiliser la `COARefTime` classe pour effectuer une conversion entre les deux formats.</span><span class="sxs-lookup"><span data-stu-id="eda0e-110">Filters can use the `COARefTime` class to convert between the two formats.</span></span> <span data-ttu-id="eda0e-111">Cette classe est dérivée de la classe [**CRefTime**](creftime.md) .</span><span class="sxs-lookup"><span data-stu-id="eda0e-111">This class is derived from the [**CRefTime**](creftime.md) class.</span></span>



| <span data-ttu-id="eda0e-112">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="eda0e-112">Public Methods</span></span>                                          | <span data-ttu-id="eda0e-113">Description</span><span class="sxs-lookup"><span data-stu-id="eda0e-113">Description</span></span>                                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="eda0e-114">**COARefTime**</span><span class="sxs-lookup"><span data-stu-id="eda0e-114">**COARefTime**</span></span>](coareftime-coareftime.md)             | <span data-ttu-id="eda0e-115">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="eda0e-115">Constructor method.</span></span>                                                   |
| <span data-ttu-id="eda0e-116">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="eda0e-116">Operators</span></span>                                               | <span data-ttu-id="eda0e-117">Description</span><span class="sxs-lookup"><span data-stu-id="eda0e-117">Description</span></span>                                                           |
| [<span data-ttu-id="eda0e-118">**double**</span><span class="sxs-lookup"><span data-stu-id="eda0e-118">**double**</span></span>](coareftime-double.md)                     | <span data-ttu-id="eda0e-119">Convertit le temps de référence en valeur **double** .</span><span class="sxs-lookup"><span data-stu-id="eda0e-119">Converts the reference time to a **double** value.</span></span>                    |
| [<span data-ttu-id="eda0e-120">**temps de référence \_**</span><span class="sxs-lookup"><span data-stu-id="eda0e-120">**REFERENCE\_TIME**</span></span>](coareftime-reference-time.md)    | <span data-ttu-id="eda0e-121">Convertit l’objet en valeur de **\_ temps de référence** .</span><span class="sxs-lookup"><span data-stu-id="eda0e-121">Casts the object to a **REFERENCE\_TIME** value.</span></span>                      |
| [<span data-ttu-id="eda0e-122">**opérateur =**</span><span class="sxs-lookup"><span data-stu-id="eda0e-122">**operator =**</span></span>](coareftime-operator-assign.md)        | <span data-ttu-id="eda0e-123">Affecte une nouvelle heure de référence.</span><span class="sxs-lookup"><span data-stu-id="eda0e-123">Assigns a new reference time.</span></span>                                         |
| [<span data-ttu-id="eda0e-124">**opérateur = =**</span><span class="sxs-lookup"><span data-stu-id="eda0e-124">**operator ==**</span></span>](coareftime-operator-eq.md)           | <span data-ttu-id="eda0e-125">Teste l’égalité entre deux heures de référence.</span><span class="sxs-lookup"><span data-stu-id="eda0e-125">Tests for equality between two reference times.</span></span>                       |
| [<span data-ttu-id="eda0e-126">**opérateur ! =**</span><span class="sxs-lookup"><span data-stu-id="eda0e-126">**operator !=**</span></span>](cmediatype-operator-neq.md)          | <span data-ttu-id="eda0e-127">Teste l’inégalité entre deux heures de référence.</span><span class="sxs-lookup"><span data-stu-id="eda0e-127">Tests for inequality between two reference times.</span></span>                     |
| [<span data-ttu-id="eda0e-128">**<d’opérateur**</span><span class="sxs-lookup"><span data-stu-id="eda0e-128">**operator <**</span></span>](coareftime-operator-lt.md)         | <span data-ttu-id="eda0e-129">Teste si une heure de référence est inférieure à une autre.</span><span class="sxs-lookup"><span data-stu-id="eda0e-129">Tests if one reference time is less than another.</span></span>                     |
| [<span data-ttu-id="eda0e-130">**>d’opérateur**</span><span class="sxs-lookup"><span data-stu-id="eda0e-130">**operator >**</span></span>](coareftime-operator-gt.md)         | <span data-ttu-id="eda0e-131">Teste si une heure de référence est supérieure à une autre.</span><span class="sxs-lookup"><span data-stu-id="eda0e-131">Tests if one reference time is greater than another.</span></span>                  |
| [<span data-ttu-id="eda0e-132">**<opérateur =**</span><span class="sxs-lookup"><span data-stu-id="eda0e-132">**operator <=**</span></span>](coareftime-operator-lteq.md)      | <span data-ttu-id="eda0e-133">Teste si une heure de référence est inférieure ou égale à une autre.</span><span class="sxs-lookup"><span data-stu-id="eda0e-133">Tests if one reference time is less than or equal to another.</span></span>         |
| [<span data-ttu-id="eda0e-134">**>opérateur =**</span><span class="sxs-lookup"><span data-stu-id="eda0e-134">**operator >=**</span></span>](coareftime-operator-gteq.md)      | <span data-ttu-id="eda0e-135">Teste si une heure de référence est supérieure ou égale à une autre.</span><span class="sxs-lookup"><span data-stu-id="eda0e-135">Tests if one reference time is greater than or equal to another.</span></span>      |
| [<span data-ttu-id="eda0e-136">**opérateur +**</span><span class="sxs-lookup"><span data-stu-id="eda0e-136">**operator +**</span></span>](coareftime-operator-plus.md)          | <span data-ttu-id="eda0e-137">Ajoute deux heures de référence.</span><span class="sxs-lookup"><span data-stu-id="eda0e-137">Adds two reference times.</span></span>                                             |
| [<span data-ttu-id="eda0e-138">\* \* opérateur \* \*</span><span class="sxs-lookup"><span data-stu-id="eda0e-138">\*\*operator  \*\*</span></span>](coareftime-operator-minus.md)         | <span data-ttu-id="eda0e-139">Soustrait une heure de référence d’une autre.</span><span class="sxs-lookup"><span data-stu-id="eda0e-139">Subtracts one reference time from another.</span></span>                            |
| [<span data-ttu-id="eda0e-140">**opérateur + =**</span><span class="sxs-lookup"><span data-stu-id="eda0e-140">**operator +=**</span></span>](coareftime-operator-plus-assign.md)  | <span data-ttu-id="eda0e-141">Ajoute deux heures de référence et assigne le résultat à cet objet.</span><span class="sxs-lookup"><span data-stu-id="eda0e-141">Adds two reference times, and assigns the result to this object.</span></span>      |
| [<span data-ttu-id="eda0e-142">**opérateur =**</span><span class="sxs-lookup"><span data-stu-id="eda0e-142">**operator  =**</span></span>](coareftime-operator-minus-assign.md) | <span data-ttu-id="eda0e-143">Soustrait deux heures de référence et assigne le résultat à cet objet.</span><span class="sxs-lookup"><span data-stu-id="eda0e-143">Subtracts two reference times, and assigns the result to this object.</span></span> |
| [<span data-ttu-id="eda0e-144">**and \***</span><span class="sxs-lookup"><span data-stu-id="eda0e-144">**operator \***</span></span>](coareftime-operator-mult.md)         | <span data-ttu-id="eda0e-145">Multiplie une heure de référence par une valeur.</span><span class="sxs-lookup"><span data-stu-id="eda0e-145">Multiplies a reference time by a value.</span></span>                               |
| [<span data-ttu-id="eda0e-146">**and**</span><span class="sxs-lookup"><span data-stu-id="eda0e-146">**operator /**</span></span>](coareftime-operator-div.md)           | <span data-ttu-id="eda0e-147">Divise une heure de référence par une valeur.</span><span class="sxs-lookup"><span data-stu-id="eda0e-147">Divides a reference time by a value.</span></span>                                  |



 

## <a name="requirements"></a><span data-ttu-id="eda0e-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eda0e-148">Requirements</span></span>



| <span data-ttu-id="eda0e-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eda0e-149">Requirement</span></span> | <span data-ttu-id="eda0e-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="eda0e-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eda0e-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="eda0e-151">Header</span></span><br/>  | <dl> <span data-ttu-id="eda0e-152"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eda0e-152"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eda0e-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eda0e-153">Library</span></span><br/> | <dl> <span data-ttu-id="eda0e-154"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="eda0e-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




