---
title: Attribut OnEd de VML
description: Attribut OnEd de VML
ms.assetid: d24137c3-73cb-4b92-bf25-ffe4aa8b0069
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1892d5ed185358c4abc5fa6fdaf6448ac5b6317c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316290"
---
# <a name="vml-oned-attribute"></a><span data-ttu-id="e2cf2-103">Attribut OnEd de VML</span><span class="sxs-lookup"><span data-stu-id="e2cf2-103">VML OnEd Attribute</span></span>

<span data-ttu-id="e2cf2-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e2cf2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e2cf2-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e2cf2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e2cf2-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="e2cf2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e2cf2-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="e2cf2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e2cf2-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e2cf2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e2cf2-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e2cf2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e2cf2-110">Détermine si les poignées supplémentaires d’une forme sont masquées.</span><span class="sxs-lookup"><span data-stu-id="e2cf2-110">Determines whether the extra handles of a shape are hidden.</span></span> <span data-ttu-id="e2cf2-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e2cf2-111">Read/write.</span></span> <span data-ttu-id="e2cf2-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="e2cf2-112">**VgTriState**.</span></span>

<span data-ttu-id="e2cf2-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="e2cf2-113">**Applies To**</span></span>

[<span data-ttu-id="e2cf2-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="e2cf2-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="e2cf2-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="e2cf2-115">**Tag Syntax**</span></span>

<span data-ttu-id="e2cf2-116"><v : *Element* o :ONED = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="e2cf2-116"><v: *element* o:oned=" *expression* "></span></span>

<span data-ttu-id="e2cf2-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="e2cf2-117">**Remarks**</span></span>

<span data-ttu-id="e2cf2-118">Masque toutes les poignées de forme à l’exception des poignées supérieure gauche et inférieure droite ; autrement dit, les mêmes Handles utilisés pour un segment de ligne droite.</span><span class="sxs-lookup"><span data-stu-id="e2cf2-118">Hides all shape handles except the top left and bottom right; that is, the same handles that are used for a straight line segment.</span></span> <span data-ttu-id="e2cf2-119">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="e2cf2-119">The default is **False**.</span></span>

<span data-ttu-id="e2cf2-120">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="e2cf2-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="e2cf2-121">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="e2cf2-121">**Example**</span></span>

<span data-ttu-id="e2cf2-122">Toutes les poignées, sauf les poignées supérieure gauche et inférieure droite de la forme, sont masquées.</span><span class="sxs-lookup"><span data-stu-id="e2cf2-122">All but the top left and bottom right handles of the shape are hidden.</span></span>


```HTML
   <v:shape id="rect01" OnEd="True"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 