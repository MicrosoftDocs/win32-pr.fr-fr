---
title: Présentation de VML
description: Présentation de VML
ms.assetid: 8b603e95-3f02-47d6-9c5c-c781fa5d8459
keywords:
- Langage VML (VML), référence
- VML (langage VML), référence
- graphiques vectoriels, référence VML
- graphismes vectoriels, langage VML (VML)
- référence pour langage VML (VML)
- Référence VML
- Langage VML (VML), élément de forme
- VML (langage VML), élément de forme
- graphismes vectoriels, élément Shape
- Élément Shape
- Éléments VML, forme
- Langage VML (VML), VBScript
- VML (langage VML), VBScript
- Langage VML (VML), JavaScript
- VML (langage VML), JavaScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7a370519e3f173e7418f1aa0510cac768ff46c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382113"
---
# <a name="vml-introduction"></a><span data-ttu-id="e8114-118">Présentation de VML</span><span class="sxs-lookup"><span data-stu-id="e8114-118">VML Introduction</span></span>

<span data-ttu-id="e8114-119">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e8114-119">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e8114-120">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e8114-120">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e8114-121">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="e8114-121">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e8114-122">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="e8114-122">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e8114-123">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e8114-123">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e8114-124">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e8114-124">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e8114-125">Ce document fournit une référence détaillée complète sur l’implémentation du langage VML (VML) fourni avec Microsoft Office 2000.</span><span class="sxs-lookup"><span data-stu-id="e8114-125">This document gives a complete detailed reference to the implementation of the Vector Markup Language (VML) that is shipped with Microsoft Office 2000.</span></span> <span data-ttu-id="e8114-126">D’autres implémentations peuvent varier.</span><span class="sxs-lookup"><span data-stu-id="e8114-126">Other implementations may vary.</span></span> <span data-ttu-id="e8114-127">Consultez la [spécification VML](https://www.w3.org/TR/NOTE-datetime.html) pour plus d’informations sur VML comme standard.</span><span class="sxs-lookup"><span data-stu-id="e8114-127">Consult the [VML specification](https://www.w3.org/TR/NOTE-datetime.html) for more information about VML as a standard.</span></span>

<span data-ttu-id="e8114-128">VML est défini comme un ensemble d’éléments XML et les attributs correspondants pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="e8114-128">VML is defined as a set of XML elements and the corresponding attributes for each element.</span></span> <span data-ttu-id="e8114-129">Étant donné que l’élément **Shape** est le bloc de construction de base de VML, cliquez [ici](shape-element--vml.md) pour commencer la référence.</span><span class="sxs-lookup"><span data-stu-id="e8114-129">Since the **Shape** element is the basic building block of VML, click [here](shape-element--vml.md) to begin the reference.</span></span>

<span data-ttu-id="e8114-130">Notez que cette référence contient plusieurs exemples et démonstrations.</span><span class="sxs-lookup"><span data-stu-id="e8114-130">Note that this reference contains several examples and demos.</span></span> <span data-ttu-id="e8114-131">Vous devez avoir installé Microsoft Internet Explorer 5,0 ou version ultérieure pour afficher le VML en direct.</span><span class="sxs-lookup"><span data-stu-id="e8114-131">You must have Microsoft Internet Explorer 5.0 or greater installed to view the live VML.</span></span>

<span data-ttu-id="e8114-132">En plus des informations sur l’utilisation des éléments et des attributs en tant que balises XML qui étendent du code HTML, cette référence contient la syntaxe et des exemples qui montrent comment utiliser les fonctionnalités de script et de Document Object Model d’Internet Explorer 5 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e8114-132">In addition to the information about using elements and attributes as XML tags that extend HTML, this reference contains syntax and examples that show how to use the scripting and the Document Object Model features of Internet Explorer 5 or greater.</span></span> <span data-ttu-id="e8114-133">L’utilisation de script avec VML vous permet de créer des éléments « à la volée » et de manipuler des attributs en temps réel.</span><span class="sxs-lookup"><span data-stu-id="e8114-133">Using script with VML enables you to create elements "on the fly" and manipulate attributes in real time.</span></span>

<span data-ttu-id="e8114-134">Les exemples de cette référence utilisent VBScript et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e8114-134">This examples in this reference uses VBScript and Javascript.</span></span> <span data-ttu-id="e8114-135">Si vous utilisez un langage de script différent de celui indiqué dans un exemple, vous devez respecter la casse de tous les noms d’éléments et d’attributs.</span><span class="sxs-lookup"><span data-stu-id="e8114-135">If you use use a different scripting language than the one shown in an example, you must match the case of all element and attribute names.</span></span> <span data-ttu-id="e8114-136">La référence fournit une syntaxe de script correcte pour les langages qui respectent la casse, tels que JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e8114-136">The reference gives scripting syntax that is correct for case-sensitive languages such as JavaScript.</span></span> <span data-ttu-id="e8114-137">En cas de doute sur le caractère correct, utilisez un Explorateur d’objets (tel que OLEView) pour explorer l' VGX.DLL afin de déterminer la casse exacte d’un élément ou d’un attribut.</span><span class="sxs-lookup"><span data-stu-id="e8114-137">If in doubt regarding the correct character case, use an object browser (such as OLEView) to explore the VGX.DLL to determine the exact case of an element or attribute.</span></span> <span data-ttu-id="e8114-138">Notez que lorsque VML est utilisé en tant que balises XML, le respect de la casse dépend du type de document du document sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="e8114-138">Note that when VML is used as XML tags, case sensitivity depends on the document type of you underlying document.</span></span> <span data-ttu-id="e8114-139">Si vous utilisez un mode strict ! DOCTYPE, les éléments et les attributs sont sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="e8114-139">If you are using a strict mode !DOCTYPE, elements and attributes will be case sensitive.</span></span>

[<span data-ttu-id="e8114-140">Référence VML</span><span class="sxs-lookup"><span data-stu-id="e8114-140">The VML Reference</span></span>](shape-element--vml.md)

 

 