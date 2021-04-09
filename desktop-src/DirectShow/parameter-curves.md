---
description: Courbes de paramètres
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: Courbes de paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c482112c8bd76217f5cbdabdf3cda13b09c3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109511"
---
# <a name="parameter-curves"></a><span data-ttu-id="a0426-103">Courbes de paramètres</span><span class="sxs-lookup"><span data-stu-id="a0426-103">Parameter Curves</span></span>

<span data-ttu-id="a0426-104">Les paramètres de média peuvent suivre une courbe dans le temps.</span><span class="sxs-lookup"><span data-stu-id="a0426-104">Media parameters are able to follow a curve over time.</span></span> <span data-ttu-id="a0426-105">Chaque courbe est décrite par une formule mathématique et deux points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a0426-105">Each curve is described by a mathematical formula and two end-points.</span></span> <span data-ttu-id="a0426-106">Chaque point de terminaison est défini par une heure de référence et la valeur de la courbe à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="a0426-106">Each end-point is defined by a reference time and the value of the curve at that time.</span></span> <span data-ttu-id="a0426-107">La formule est utilisée pour calculer les valeurs intermédiaires entre les points et détermine la forme de la courbe.</span><span class="sxs-lookup"><span data-stu-id="a0426-107">The formula is used to calculate intermediate values between the points, and determines the shape of the curve.</span></span> <span data-ttu-id="a0426-108">Les courbes possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a0426-108">The possible curves are:</span></span>

-   <span data-ttu-id="a0426-109">Y</span><span class="sxs-lookup"><span data-stu-id="a0426-109">Jump</span></span>
-   <span data-ttu-id="a0426-110">Linéaire</span><span class="sxs-lookup"><span data-stu-id="a0426-110">Linear</span></span>
-   <span data-ttu-id="a0426-111">Carré</span><span class="sxs-lookup"><span data-stu-id="a0426-111">Square</span></span>
-   <span data-ttu-id="a0426-112">Carré inverse</span><span class="sxs-lookup"><span data-stu-id="a0426-112">Inverse square</span></span>
-   <span data-ttu-id="a0426-113">Sinus</span><span class="sxs-lookup"><span data-stu-id="a0426-113">Sine</span></span>

<span data-ttu-id="a0426-114">« Jump » signifie passer directement à la valeur de fin.</span><span class="sxs-lookup"><span data-stu-id="a0426-114">"Jump" means jump directly to the end value.</span></span> <span data-ttu-id="a0426-115">Les autres courbes sont présentées dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="a0426-115">The other curves are shown in the following diagram.</span></span>

![courbes de paramètres](images/param-curves01.png)

<span data-ttu-id="a0426-117">Mathématiquement, les courbes fonctionnent comme suit.</span><span class="sxs-lookup"><span data-stu-id="a0426-117">Mathematically, the curves work as follows.</span></span> <span data-ttu-id="a0426-118">Supposons qu’une courbe commence à l’heure *t*₀ avec la valeur *v*₀ et se termine à l’heure *t*₁ par une valeur *v*₁.</span><span class="sxs-lookup"><span data-stu-id="a0426-118">Suppose that a curve begins at time *t*₀ with a value of *v*₀, and ends at time *t*₁ with a value of *v*₁.</span></span> <span data-ttu-id="a0426-119">Les deux points qui définissent la courbe sont (*t*₀, *v*₀) et (*t*₁, *v*₁).</span><span class="sxs-lookup"><span data-stu-id="a0426-119">The two points that define the curve are (*t*₀, *v*₀) and (*t*₁, *v*₁).</span></span>

-   <span data-ttu-id="a0426-120">Laissez Δ *t* la durée totale de la courbe, *t*₁ –*t*₀.</span><span class="sxs-lookup"><span data-stu-id="a0426-120">Let Δ *t* be the total duration of the curve, *t*₁–*t*₀.</span></span>
-   <span data-ttu-id="a0426-121">Laissez Δ *v* correspondre à l’intervalle entre les valeurs de début et de fin, *v*₁ –*v*₀.</span><span class="sxs-lookup"><span data-stu-id="a0426-121">Let Δ *v* be the interval between the starting and ending values, *v*₁–*v*₀.</span></span>
-   <span data-ttu-id="a0426-122">À tout moment *t* comme t *₀ <*= *t*  <=  *t*₁, laissez Δ *t*' = *t*-*t*₀.</span><span class="sxs-lookup"><span data-stu-id="a0426-122">At any time *t* such that *t*₀ <= *t* <= *t*₁, let Δ *t*' = *t*–*t*₀.</span></span>

![calcul des paramètres](images/param-curves02.png)

<span data-ttu-id="a0426-124">La valeur du paramètre à l’heure *t* est la suivante :</span><span class="sxs-lookup"><span data-stu-id="a0426-124">The value of the parameter at time *t* is:</span></span>

<span data-ttu-id="a0426-125">*v* = f (Δ *t*'/Δ *t* ) \* Δ *v*  +  *v*₀</span><span class="sxs-lookup"><span data-stu-id="a0426-125">*v* = f( Δ *t*' / Δ *t* ) \* Δ *v* + *v*₀</span></span>

<span data-ttu-id="a0426-126">où f (x) est une fonction déterminée par le type de courbe :</span><span class="sxs-lookup"><span data-stu-id="a0426-126">where f(x) is a function determined by the curve type:</span></span>

-   <span data-ttu-id="a0426-127">Linéaire : y = x</span><span class="sxs-lookup"><span data-stu-id="a0426-127">Linear: y = x</span></span>
-   <span data-ttu-id="a0426-128">Square : y = x ^ 2</span><span class="sxs-lookup"><span data-stu-id="a0426-128">Square: y = x^2</span></span>
-   <span data-ttu-id="a0426-129">Carré inverse : y = sqrt (x)</span><span class="sxs-lookup"><span data-stu-id="a0426-129">Inverse square: y = sqrt(x)</span></span>
-   <span data-ttu-id="a0426-130">Sinus : y = \[ Sin (πx – π/2) + 1 \] /2</span><span class="sxs-lookup"><span data-stu-id="a0426-130">Sine: y = \[ sin(πx – π/2) + 1 \] / 2</span></span>

<span data-ttu-id="a0426-131">Notez que Δ *t*' < Δ *t*, donc le terme Δ *t*'/Δ *t* est compris entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="a0426-131">Observe that Δ *t*' < Δ *t*, so the term Δ *t*'/Δ *t* ranges from 0 to 1.</span></span> <span data-ttu-id="a0426-132">Par conséquent, f (x) est également compris entre 0 et 1, et *v* se situe toujours entre *v*₀ et *v*₁.</span><span class="sxs-lookup"><span data-stu-id="a0426-132">Therefore, f(x) also ranges from 0 to 1, and *v* always falls between *v*₀ and *v*₁.</span></span> <span data-ttu-id="a0426-133">C’est vrai que *v*₀ < *v*₁ ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="a0426-133">This is true whether *v*₀ < *v*₁ or vice versa.</span></span> <span data-ttu-id="a0426-134">En d’autres termes, la courbe est délimitée par le rectangle (*t*₀, *v*₀, *t*₁, *v*₁).</span><span class="sxs-lookup"><span data-stu-id="a0426-134">In other words, the curve is bounded by the rectangle (*t*₀, *v*₀, *t*₁, *v*₁).</span></span>

<span data-ttu-id="a0426-135">Pour la courbe sinusoïdale, la valeur de (πx – π/2) est comprise entre – π/2 et π/2, ce qui signifie que sin (πx – π/2) est compris entre-1 et 1.</span><span class="sxs-lookup"><span data-stu-id="a0426-135">For the sine curve, the value of (πx – π/2) ranges from –π/2 to π/2, which means that sin(πx – π/2) ranges from –1 to 1.</span></span> <span data-ttu-id="a0426-136">Le résultat est ensuite normalisé afin que f (x) se trouve dans la plage (0 – 1).</span><span class="sxs-lookup"><span data-stu-id="a0426-136">The result is then normalized so that f(x) falls into the range (0–1).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0426-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0426-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0426-138">Paramètres de média</span><span class="sxs-lookup"><span data-stu-id="a0426-138">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



