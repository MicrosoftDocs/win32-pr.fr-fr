---
title: Utilisation de l’élément Handles
description: Utilisation de l’élément Handles
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- Atelier Web, élément Handles
- conception de pages Web, Handles, élément
- Langage VML (VML), Handles (élément)
- VML (langage VML), élément Handles
- Vector Graphics, Handles, élément
- élément Handles
- Éléments VML, Handles
- Formes VML, élément Handles
- Langage VML (VML), attacher du texte à des formes
- VML (langage VML), attacher du texte à des formes
- graphiques vectoriels, attacher du texte à des formes
- Formes VML, joindre du texte
- attacher du texte à des formes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54c721d50f51c46cd4bf08393e85ad83307fc1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031298"
---
# <a name="using-the-handles-element"></a><span data-ttu-id="c9ff2-116">Utilisation de l’élément Handles</span><span class="sxs-lookup"><span data-stu-id="c9ff2-116">Using the Handles Element</span></span>

<span data-ttu-id="c9ff2-117">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c9ff2-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c9ff2-118">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c9ff2-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c9ff2-119">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="c9ff2-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c9ff2-120">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="c9ff2-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c9ff2-121">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c9ff2-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c9ff2-122">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c9ff2-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c9ff2-123">Dans cette rubrique, nous allons vous montrer comment utiliser l' `<handles>` élément pour attacher du texte à une forme.</span><span class="sxs-lookup"><span data-stu-id="c9ff2-123">In this topic, we will illustrate how to use the `<handles>` element to attach text to a shape.</span></span>

<span data-ttu-id="c9ff2-124">Vous pouvez placer le `<handles>` sous-élément à l’intérieur de `<shape>` ou `<shapetype>` pour définir des éléments d’interface utilisateur qui peuvent faire varier les valeurs d' **ajustement** sur la forme.</span><span class="sxs-lookup"><span data-stu-id="c9ff2-124">You can place the `<handles>` sub-element inside `<shape>` or `<shapetype>` to define user interface elements that can vary the **adj** values on the shape.</span></span>

<span data-ttu-id="c9ff2-125">Par exemple, comme illustré dans la représentation VML suivante, vous pouvez fournir une poignée d’ajustement (zone jaune) que les utilisateurs peuvent simplement faire glisser pour ajuster la forme.</span><span class="sxs-lookup"><span data-stu-id="c9ff2-125">For example, as shown the following VML representation, you can provide an adjust handle (yellow box) that users can simply drag to adjust the shape.</span></span>

<span data-ttu-id="c9ff2-126">Remarque : les descripteurs sont disponibles lorsque cette forme VML est affichée dans Microsoft Office applications, où la forme est destinée à être manipulablee.</span><span class="sxs-lookup"><span data-stu-id="c9ff2-126">Note: the handles are available when this VML shape is viewed in Microsoft Office applications, where the shape is intended to be manipulable.</span></span>

![shape1.gif (564 octets)](images/shape1h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="16200,5400"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





<span data-ttu-id="c9ff2-128">Notez que la seule différence entre la représentation VML précédente et la seule qui suit est la valeur **Adj** .</span><span class="sxs-lookup"><span data-stu-id="c9ff2-128">Notice that the only difference between the preceding VML representation and the following one is the **adj** value.</span></span>

![shape2.gif (1361 octets)](images/shape2h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="11304,6600"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





<span data-ttu-id="c9ff2-130">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858393) .</span><span class="sxs-lookup"><span data-stu-id="c9ff2-130">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858393) .</span></span>

 

 