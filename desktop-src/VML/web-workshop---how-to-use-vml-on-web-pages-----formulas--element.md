---
title: Utilisation de l’élément Formulas
description: Utilisation de l’élément Formulas
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Web Workshop, élément Formulas
- conception de pages Web, élément Formulas
- Langage VML (VML), élément Formulas
- VML (langage VML), élément Formulas
- élément Graphics, Formulas
- élément Formulas
- Éléments VML, formules
- Formes VML, élément Formulas
- Langage VML (VML), définition des tracés pour les formes
- VML (langage VML), définition des tracés pour les formes
- graphiques vectoriels, définition des tracés pour les formes
- Formes VML, définition de chemins d’accès
- définition des tracés pour les formes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85ce4ebb6eea05895edf974e3ca86b1fa2ad923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031299"
---
# <a name="using-the-formulas-element"></a><span data-ttu-id="432c9-116">Utilisation de l’élément Formulas</span><span class="sxs-lookup"><span data-stu-id="432c9-116">Using the Formulas Element</span></span>

<span data-ttu-id="432c9-117">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="432c9-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="432c9-118">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="432c9-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="432c9-119">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="432c9-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="432c9-120">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="432c9-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="432c9-121">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="432c9-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="432c9-122">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="432c9-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="432c9-123">Dans cette rubrique, nous allons vous montrer comment utiliser le `<formulas>` sous-élément pour définir un chemin d’accès réglable pour une forme.</span><span class="sxs-lookup"><span data-stu-id="432c9-123">In this topic, we will illustrate how to use the `<formulas>` sub-element to define an adjustable path for a shape.</span></span>

<span data-ttu-id="432c9-124">Vous pouvez placer le <formulas> sous-élément à l’intérieur de `<shape>` ou `<shapetype>` pour définir des formules qui peuvent varier le tracé d’une forme.</span><span class="sxs-lookup"><span data-stu-id="432c9-124">You can place the <formulas> sub-element inside `<shape>` or `<shapetype>` to define formulas that can vary the path of a shape.</span></span> <span data-ttu-id="432c9-125">Dans le `<formulas>` sous-élément, un sous-élément **f** définit une formule afin qu’une valeur soit évaluée en fonction de cette formule.</span><span class="sxs-lookup"><span data-stu-id="432c9-125">Inside the `<formulas>` sub-element, one **f** sub-element defines one formula so that one value is evaluated based upon that formula.</span></span> <span data-ttu-id="432c9-126">Par exemple, la formule `<v:f eqn="prod 10 4 5"/>` définit une valeur qui est équivalente à « 10 x 4/5 ».</span><span class="sxs-lookup"><span data-stu-id="432c9-126">For example, the formula, `<v:f eqn="prod 10 4 5"/>` defines a value that is equivalent to "10 x 4 / 5".</span></span>

<span data-ttu-id="432c9-127">Vous pouvez placer un grand nombre de sous-éléments **f** dans un `<formulas>` sous-élément.</span><span class="sxs-lookup"><span data-stu-id="432c9-127">You can place many **f** sub-elements inside one`<formulas>` sub-element.</span></span> <span data-ttu-id="432c9-128">Les formules peuvent référencer les valeurs définies précédemment dans d’autres formules au sein du même `<formulas>` sous-élément.</span><span class="sxs-lookup"><span data-stu-id="432c9-128">Formulas can reference the values that are defined earlier in other formulas within the same `<formulas>` sub-element.</span></span> <span data-ttu-id="432c9-129">La valeur définie dans la première formule peut être appelée @0 , mais la valeur définie dans la deuxième formule peut être appelée @1 , et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="432c9-129">The value that is defined in the first formula can be referred to as @0, the value that is defined in the second formula can be referred to as @1, and so on.</span></span>

<span data-ttu-id="432c9-130">En outre, vous pouvez spécifier l’attribut de propriété **Adj** de l' `<shape>` élément, par exemple adj = "100, 200, 150".</span><span class="sxs-lookup"><span data-stu-id="432c9-130">In addition, you can specify the **adj** property attribute of the `<shape>` element, such as adj="100, 200, 150".</span></span> <span data-ttu-id="432c9-131">À l’intérieur de l' `<formulas>` élément, vous pouvez référencer ces valeurs dans la liste **Adj** .</span><span class="sxs-lookup"><span data-stu-id="432c9-131">Inside the `<formulas>` element, you can then reference those values in the **adj** list.</span></span> <span data-ttu-id="432c9-132">La première valeur (100) dans la liste **Adj** peut être appelée \# 0, la seconde valeur (200) peut être appelée \# 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="432c9-132">The first value (100) in the **adj** list can be referred to as \#0, the second value (200) can be referred to as \#1, and so on.</span></span>

<span data-ttu-id="432c9-133">Par exemple, pour dessiner un visage souriant, vous pouvez taper la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="432c9-133">For example, to draw a smiling face, you can type the following VML representation:</span></span>

![shape1.gif (735 octets)](images/shape1f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="17520"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





-   <span data-ttu-id="432c9-135">`adj="17520"` définit une valeur (= 17520).</span><span class="sxs-lookup"><span data-stu-id="432c9-135">`adj="17520"` defines a value (= 17520).</span></span> <span data-ttu-id="432c9-136">Cette valeur peut être référencée sous la forme \# 0.</span><span class="sxs-lookup"><span data-stu-id="432c9-136">This value can be referenced as \#0.</span></span>
-   <span data-ttu-id="432c9-137">La première formule, `<v:f eqn="sum 33030 0 #0"/>` , définit la valeur (= 33030 + 0- \# 0).</span><span class="sxs-lookup"><span data-stu-id="432c9-137">The first formula, `<v:f eqn="sum 33030 0 #0"/>`, defines the value (= 33030 + 0 - \#0).</span></span> <span data-ttu-id="432c9-138">Cette valeur peut être référencée en tant que @0 .</span><span class="sxs-lookup"><span data-stu-id="432c9-138">This value can be referenced as @0.</span></span>
-   <span data-ttu-id="432c9-139">La deuxième formule, `<v:f eqn="prod #0 4 3"/>` , définit la valeur (= \# 0 \* 4/3).</span><span class="sxs-lookup"><span data-stu-id="432c9-139">The second formula, `<v:f eqn="prod #0 4 3"/>`, defines the value (= \#0 \* 4 / 3).</span></span> <span data-ttu-id="432c9-140">Cette valeur peut être référencée en tant que @1 .</span><span class="sxs-lookup"><span data-stu-id="432c9-140">This value can be referenced as @1.</span></span>
-   <span data-ttu-id="432c9-141">La troisième formule, `<v:f eqn="prod @0 1 3"/>` , définit la valeur (= @0 \* 1/3).</span><span class="sxs-lookup"><span data-stu-id="432c9-141">The third formula, `<v:f eqn="prod @0 1 3"/>`, defines the value (= @0 \* 1 / 3).</span></span> <span data-ttu-id="432c9-142">Cette valeur peut être référencée en tant que @2 .</span><span class="sxs-lookup"><span data-stu-id="432c9-142">This value can be referenced as @2.</span></span>
-   <span data-ttu-id="432c9-143">La quatrième formule, `<v:f eqn="sum @1 0 @2"/>` , définit la valeur (= @1 + 0 -@2 ).</span><span class="sxs-lookup"><span data-stu-id="432c9-143">The fourth formula, `<v:f eqn="sum @1 0 @2"/>`, defines the value (=@1 + 0 -@2).</span></span> <span data-ttu-id="432c9-144">Cette valeur peut être référencée en tant que @3 .</span><span class="sxs-lookup"><span data-stu-id="432c9-144">This value can be referenced as @3.</span></span>
-   <span data-ttu-id="432c9-145">À l’intérieur de l' `<path>` élément, les valeurs définies dans les formules First ( @0 ) et quatrième ( @3 ) sont utilisées pour déterminer le contour de la forme.</span><span class="sxs-lookup"><span data-stu-id="432c9-145">Inside the `<path>` element, the values defined in the first (@0) and the fourth (@3) formulas are used to determine the outline of the shape.</span></span>

<span data-ttu-id="432c9-146">Si vous modifiez la liste **Adj** , par exemple `adj="20000"` , les valeurs des formules qui font référence à la liste **Adj** sont également modifiées, ce qui affecte le visage souriant comme suit :</span><span class="sxs-lookup"><span data-stu-id="432c9-146">If you change the **adj** list, such as `adj="20000"`, the values of the formulas that reference the **adj** list will be changed as well, affecting the smiling face as follows:</span></span>

![shape2.gif (765 octets)](images/shape2f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="20000"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





<span data-ttu-id="432c9-148">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858392) .</span><span class="sxs-lookup"><span data-stu-id="432c9-148">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858392) .</span></span>

 

 