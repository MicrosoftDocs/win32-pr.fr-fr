---
title: VML, attribut de classe
description: VML, attribut de classe
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94bdc723ba9be335afc43023ab89b88834c55474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941155"
---
# <a name="vml-class-attribute"></a><span data-ttu-id="658d8-103">VML, attribut de classe</span><span class="sxs-lookup"><span data-stu-id="658d8-103">VML Class Attribute</span></span>

<span data-ttu-id="658d8-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="658d8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="658d8-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="658d8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="658d8-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="658d8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="658d8-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="658d8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="658d8-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="658d8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="658d8-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="658d8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="658d8-110">Fait référence à une définition d’un style CSS.</span><span class="sxs-lookup"><span data-stu-id="658d8-110">Refers to a definition of a CSS style.</span></span> <span data-ttu-id="658d8-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="658d8-111">Read/write.</span></span> <span data-ttu-id="658d8-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="658d8-112">**String**.</span></span>

<span data-ttu-id="658d8-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="658d8-113">**Applies To**</span></span>

[<span data-ttu-id="658d8-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="658d8-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="658d8-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="658d8-115">**Tag Syntax**</span></span>

<span data-ttu-id="658d8-116"><v : *Element* Class = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="658d8-116"><v: *element* class=" *expression* "></span></span>

<span data-ttu-id="658d8-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="658d8-117">**Script Syntax**</span></span>

<span data-ttu-id="658d8-118">*Element* . ClassName = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="658d8-118">*element* .classname="*expression*"</span></span>

<span data-ttu-id="658d8-119">*expression* = *élément*. ClassName</span><span class="sxs-lookup"><span data-stu-id="658d8-119">*expression*=*element*.classname</span></span>

<span data-ttu-id="658d8-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="658d8-120">**Remarks**</span></span>

<span data-ttu-id="658d8-121">L’attribut de **classe** est semblable à l’attribut de **classe** HTML standard utilisé avec les feuilles de style CSS.</span><span class="sxs-lookup"><span data-stu-id="658d8-121">The **class** attribute is similar to the standard HTML **class** attribute used with CSS style sheets.</span></span>

<span data-ttu-id="658d8-122">Notez que **className** est utilisé à la place de **Class** pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="658d8-122">Note that **classname** is used instead of **class** for scripting.</span></span> <span data-ttu-id="658d8-123">Notez également que pour les scripts, la **className** peut uniquement être lue. la modification de la valeur de **className** ne modifiera pas le rendu de la forme.</span><span class="sxs-lookup"><span data-stu-id="658d8-123">Also note that for scripting, the **classname** can only be read; changing the value of **classname** will not change the rendering of the shape.</span></span>

<span data-ttu-id="658d8-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="658d8-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="658d8-125">**Voir aussi**</span><span class="sxs-lookup"><span data-stu-id="658d8-125">**See Also**</span></span>

[<span data-ttu-id="658d8-126">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="658d8-126">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="658d8-127">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="658d8-127">**Example**</span></span>

<span data-ttu-id="658d8-128">Une classe pour **Width** est créée avec le style</span><span class="sxs-lookup"><span data-stu-id="658d8-128">A class for **width** is created with the style</span></span>


```HTML
   .narrowstyle {width:50;height:100}
```



<span data-ttu-id="658d8-129">La largeur est alors référencée par l’inclusion du style.</span><span class="sxs-lookup"><span data-stu-id="658d8-129">Then the width is referenced by including the style.</span></span> <span data-ttu-id="658d8-130">Notez que la largeur andheight n’est pas définie dans l’attribut **style** , mais sera définie par le style.</span><span class="sxs-lookup"><span data-stu-id="658d8-130">Note that the width andheight is not defined in the **style** attribute, but will be defined by the style.</span></span>


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="658d8-131">Notez que la **classe** s’applique uniquement aux attributs CSS-type.</span><span class="sxs-lookup"><span data-stu-id="658d8-131">Note that **Class** only applies to CSS-type attributes.</span></span>

 

 