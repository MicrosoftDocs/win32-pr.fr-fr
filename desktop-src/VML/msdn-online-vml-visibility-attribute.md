---
title: Attribut de visibilité VML
description: Attribut de visibilité VML
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7325d09f60da13f0c7c44e73b347fa579870fcd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106527555"
---
# <a name="vml-visibility-attribute"></a><span data-ttu-id="7ae60-103">Attribut de visibilité VML</span><span class="sxs-lookup"><span data-stu-id="7ae60-103">VML Visibility Attribute</span></span>

<span data-ttu-id="7ae60-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7ae60-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7ae60-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="7ae60-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7ae60-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="7ae60-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7ae60-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="7ae60-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7ae60-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7ae60-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7ae60-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7ae60-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7ae60-110">Détermine si une forme est affichée.</span><span class="sxs-lookup"><span data-stu-id="7ae60-110">Determines whether a shape is displayed.</span></span> <span data-ttu-id="7ae60-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7ae60-111">Read/write.</span></span> <span data-ttu-id="7ae60-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="7ae60-112">**String**.</span></span>

<span data-ttu-id="7ae60-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="7ae60-113">**Applies To**</span></span>

[<span data-ttu-id="7ae60-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="7ae60-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="7ae60-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="7ae60-115">**Tag Syntax**</span></span>

<span data-ttu-id="7ae60-116"><v : *Element* style = "Visibility : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="7ae60-116"><v: *element* style="visibility: *expression* "></span></span>

<span data-ttu-id="7ae60-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="7ae60-117">**Script Syntax**</span></span>

<span data-ttu-id="7ae60-118">*Element* . style. Visibility = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="7ae60-118">*element* .style.visibility="*expression*"</span></span>

<span data-ttu-id="7ae60-119">*expression* = *Element*. style. Visibility</span><span class="sxs-lookup"><span data-stu-id="7ae60-119">*expression*=*element*.style.visibility</span></span>

<span data-ttu-id="7ae60-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="7ae60-120">**Remarks**</span></span>

<span data-ttu-id="7ae60-121">L’attribut **Visibility** est semblable à l’attribut de **visibilité** HTML standard pour les styles.</span><span class="sxs-lookup"><span data-stu-id="7ae60-121">The **Visibility** attribute is similar to the standard HTML **Visibility** attribute for styles.</span></span>

<span data-ttu-id="7ae60-122">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="7ae60-122">Values include:</span></span>



| <span data-ttu-id="7ae60-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ae60-123">Value</span></span>    | <span data-ttu-id="7ae60-124">Description</span><span class="sxs-lookup"><span data-stu-id="7ae60-124">Description</span></span>                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae60-125">visible</span><span class="sxs-lookup"><span data-stu-id="7ae60-125">visible</span></span>  | <span data-ttu-id="7ae60-126">La forme est visible.</span><span class="sxs-lookup"><span data-stu-id="7ae60-126">The shape is visible.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="7ae60-127">hidden</span><span class="sxs-lookup"><span data-stu-id="7ae60-127">hidden</span></span>   | <span data-ttu-id="7ae60-128">La forme n’est pas visible, mais elle fait toujours partie du déroulement des objets dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="7ae60-128">The shape is not visible, but is still part of the flow of the objects in the browser.</span></span> <span data-ttu-id="7ae60-129">Les événements de souris ne sont pas traités.</span><span class="sxs-lookup"><span data-stu-id="7ae60-129">Mouse events are not processed.</span></span>                                                                  |
| <span data-ttu-id="7ae60-130">inherit</span><span class="sxs-lookup"><span data-stu-id="7ae60-130">inherit</span></span>  | <span data-ttu-id="7ae60-131">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ae60-131">Default.</span></span> <span data-ttu-id="7ae60-132">L’état de visibilité est hérité du parent de la forme.</span><span class="sxs-lookup"><span data-stu-id="7ae60-132">The visibility state is inherited from the parent of the shape.</span></span> <span data-ttu-id="7ae60-133">Microsoft Office applications utilisent uniquement **inherit** et **Hidden**; toutes les autres valeurs sont mappées à **inherit**.</span><span class="sxs-lookup"><span data-stu-id="7ae60-133">Microsoft Office applications only use **inherit** and **hidden**; any other values are mapped to **inherit**.</span></span> |
| <span data-ttu-id="7ae60-134">réduire</span><span class="sxs-lookup"><span data-stu-id="7ae60-134">collapse</span></span> | <span data-ttu-id="7ae60-135">Utilisé pour les applications de modification graphique qui peuvent réduire des groupes de formes ; par exemple, les plans.</span><span class="sxs-lookup"><span data-stu-id="7ae60-135">Used for graphical editing applications that can collapse groups of shapes; for example, outliners.</span></span>                                                                                     |



 

<span data-ttu-id="7ae60-136">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="7ae60-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="7ae60-137">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="7ae60-137">**Example**</span></span>

<span data-ttu-id="7ae60-138">Le code suivant crée une forme, mais la masque.</span><span class="sxs-lookup"><span data-stu-id="7ae60-138">The following code creates a shape but makes it hidden.</span></span> <span data-ttu-id="7ae60-139">Les autres objets du document s’entourent, ce qui laisse un espace de la même taille que la forme.</span><span class="sxs-lookup"><span data-stu-id="7ae60-139">Other objects in the document will flow around it, leaving a space the same size as the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



<span data-ttu-id="7ae60-140">[Exemple d’attribut Visibility](/previous-versions/bb264100(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7ae60-140">[Visibility Attribute Example](/previous-versions/bb264100(v=vs.85)).</span></span> <span data-ttu-id="7ae60-141">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="7ae60-141">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 