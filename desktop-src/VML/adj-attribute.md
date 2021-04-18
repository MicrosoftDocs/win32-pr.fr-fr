---
title: Adj (attribut)
description: Adj (attribut)
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff83371cbca29ee687875343976b312466d6a78c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512738"
---
# <a name="adj-attribute"></a><span data-ttu-id="bc28a-103">Adj (attribut)</span><span class="sxs-lookup"><span data-stu-id="bc28a-103">Adj Attribute</span></span>

<span data-ttu-id="bc28a-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bc28a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bc28a-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="bc28a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bc28a-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="bc28a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bc28a-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="bc28a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bc28a-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bc28a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bc28a-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bc28a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bc28a-110">Spécifie une valeur d’ajustement utilisée pour définir les valeurs d’une formule.</span><span class="sxs-lookup"><span data-stu-id="bc28a-110">Specifies an adjustment value used to define values for a formula.</span></span> <span data-ttu-id="bc28a-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bc28a-111">Read/write.</span></span> <span data-ttu-id="bc28a-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="bc28a-112">**String**.</span></span>

<span data-ttu-id="bc28a-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="bc28a-113">**Applies To**</span></span>

[<span data-ttu-id="bc28a-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="bc28a-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="bc28a-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="bc28a-115">**Tag Syntax**</span></span>

<span data-ttu-id="bc28a-116"><v : *élément* adj = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="bc28a-116"><v: *element* adj=" *expression* "></span></span>

<span data-ttu-id="bc28a-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="bc28a-117">**Script Syntax**</span></span>

<span data-ttu-id="bc28a-118">*Element* . adj = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="bc28a-118">*element* .adj="*expression*"</span></span>

<span data-ttu-id="bc28a-119">*expression* = *élément*. adj</span><span class="sxs-lookup"><span data-stu-id="bc28a-119">*expression*=*element*.adj</span></span>

<span data-ttu-id="bc28a-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="bc28a-120">**Remarks**</span></span>

<span data-ttu-id="bc28a-121">**Adj** est utilisé pour fournir des points réglables pour une formule.</span><span class="sxs-lookup"><span data-stu-id="bc28a-121">**Adj** is used to provide adjustable points for a formula.</span></span> <span data-ttu-id="bc28a-122">S’il est utilisé dans les balises, **Adj** est une chaîne délimitée par des virgules pouvant comporter jusqu’à 8 valeurs.</span><span class="sxs-lookup"><span data-stu-id="bc28a-122">If used in tags, **Adj** is a comma-delimited string of up to 8 values.</span></span> <span data-ttu-id="bc28a-123">Certaines valeurs peuvent être omises.</span><span class="sxs-lookup"><span data-stu-id="bc28a-123">Some values may be omitted.</span></span> <span data-ttu-id="bc28a-124">Par exemple, « 0, 1, 2,, 4, 5,, 7 » serait une chaîne valide, alors que les quatrième et septième éléments n’auraient pas de valeurs (les éléments sont comptés à partir de 0).</span><span class="sxs-lookup"><span data-stu-id="bc28a-124">For example, "0,1,2,,4,5,,7" would be a valid string but the fourth and seventh items would not have values (items are counted starting from 0).</span></span>

<span data-ttu-id="bc28a-125">Pour les scripts, **Adj** utilise le type de données [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="bc28a-125">For scripting, **Adj** uses the [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) data type.</span></span>

<span data-ttu-id="bc28a-126">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="bc28a-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="bc28a-127">**Voir aussi**</span><span class="sxs-lookup"><span data-stu-id="bc28a-127">**See Also**</span></span>

[<span data-ttu-id="bc28a-128">Formule</span><span class="sxs-lookup"><span data-stu-id="bc28a-128">Formula</span></span>](msdn-online-vml-formulas-element.md)

<span data-ttu-id="bc28a-129">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bc28a-129">**Example**</span></span>

<span data-ttu-id="bc28a-130">Un carré simple est créé avec des ajustements.</span><span class="sxs-lookup"><span data-stu-id="bc28a-130">A simple square is created with adjustments.</span></span> <span data-ttu-id="bc28a-131">Tout d’abord, la chaîne **Adj** est créée pour définir huit valeurs d’ajustement.</span><span class="sxs-lookup"><span data-stu-id="bc28a-131">First the **Adj** string is created to define eight adjustment values.</span></span> <span data-ttu-id="bc28a-132">Ensuite, chaque valeur d’ajustement est référencée par l’une des huit formules, chaque valeur d’ajustement étant précédée d’un symbole dièse ( \# ).</span><span class="sxs-lookup"><span data-stu-id="bc28a-132">Then each adjustment value is referenced by one of the eight formulas, with each adjustment value preceeded by a number sign (\#) symbol.</span></span> <span data-ttu-id="bc28a-133">Enfin, un chemin d’accès est défini par une chaîne qui fait référence aux formules, chaque formule étant précédée du symbole arobase (@).</span><span class="sxs-lookup"><span data-stu-id="bc28a-133">Finally a path is defined by a string that references the formulas, with each formula preceeded by the "at" sign (@) symbol.</span></span>


```HTML
   <v:shape id="rect01" type="#myshape"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:30;left:30;width:20;height:20"
   adj="1, 1, 1, 200, 200, 200, 200, 1">
   <v:path v="m @0,@1 l @2,@3, @4,@5, @6,@7 x e"/>
   <v:formulas>
   <v:f eqn="val #0"/>
   <v:f eqn="val #1"/>
   <v:f eqn="val #2"/>
   <v:f eqn="val #3"/>
   <v:f eqn="val #4"/>
   <v:f eqn="val #5"/>
   <v:f eqn="val #6"/>
   <v:f eqn="val #7"/>
   </v:formulas>
   </v:shape>
```



<span data-ttu-id="bc28a-134">[Exemple d’attribut Adj](/previous-versions/bb229662(v=vs.85)) (nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="bc28a-134">[Adj Attribute Example](/previous-versions/bb229662(v=vs.85)) (Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 