---
title: Attribut VML Path
description: Attribut VML Path
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e43e453e982327549475de4643cc0ad21bc0b4db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842694"
---
# <a name="vml-path-attribute"></a><span data-ttu-id="edff0-103">Attribut VML Path</span><span class="sxs-lookup"><span data-stu-id="edff0-103">VML Path Attribute</span></span>

<span data-ttu-id="edff0-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="edff0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="edff0-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="edff0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="edff0-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="edff0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="edff0-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="edff0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="edff0-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="edff0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="edff0-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="edff0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="edff0-110">Spécifie la ligne qui compose les bords d’une forme.</span><span class="sxs-lookup"><span data-stu-id="edff0-110">Specifies the line that makes up the edges of a shape.</span></span> <span data-ttu-id="edff0-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="edff0-111">Read/write.</span></span> <span data-ttu-id="edff0-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="edff0-112">**String**.</span></span>

<span data-ttu-id="edff0-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="edff0-113">**Applies To**</span></span>

[<span data-ttu-id="edff0-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="edff0-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="edff0-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="edff0-115">**Tag Syntax**</span></span>

<span data-ttu-id="edff0-116"><v : *Element* path = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="edff0-116"><v: *element* path=" *expression* "></span></span>

<span data-ttu-id="edff0-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="edff0-117">**Script Syntax**</span></span>

<span data-ttu-id="edff0-118">*Element* . Path = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="edff0-118">*element* .path="*expression*"</span></span>

<span data-ttu-id="edff0-119">*expression* = *Element*. Path</span><span class="sxs-lookup"><span data-stu-id="edff0-119">*expression*=*element*.path</span></span>

<span data-ttu-id="edff0-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="edff0-120">**Remarks**</span></span>

<span data-ttu-id="edff0-121">Si une forme contient l’élément [path](msdn-online-vml-path-element.md) , les commandes Path de l’élément Path ont priorité sur la valeur de l’attribut Shape.</span><span class="sxs-lookup"><span data-stu-id="edff0-121">If a shape contains the [Path](msdn-online-vml-path-element.md) element, the path commands of the Path element take precedence over the shape attribute value.</span></span> <span data-ttu-id="edff0-122">Pour plus d’informations sur le jeu de commandes utilisé pour les chemins d’accès, consultez la rubrique relative à l’élément **path** .</span><span class="sxs-lookup"><span data-stu-id="edff0-122">See the **Path** element topic for details on the command set used for paths.</span></span>

<span data-ttu-id="edff0-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="edff0-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="edff0-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="edff0-124">**Example**</span></span>

<span data-ttu-id="edff0-125">Un chemin d’accès carré fermé est défini dans la chaîne de l’attribut path.</span><span class="sxs-lookup"><span data-stu-id="edff0-125">A closed square path is defined in the string of the path attribute.</span></span> <span data-ttu-id="edff0-126">Un point initial est défini avec `m` (utilisé pour la commande **MoveTo** ) à 1, 1 et une ligne est dessinée avec `l` (la lettre « L » utilisée pour la commande **LineTo**) à partir de la position de départ (1,1) vers les trois autres points (dans l’ordre) : 1 200 ; 200 200 ; 200, 1.</span><span class="sxs-lookup"><span data-stu-id="edff0-126">An initial point is defined with `m` (used for the **moveto** command) at 1,1 and a line is drawn with `l` (the letter "L" used for the command **lineto**) from the starting position (1,1) to the other three points (in order): 1,200; 200,200; 200,1.</span></span> <span data-ttu-id="edff0-127">La ligne est fermée avec `x` (**Fermer**) et se termine par `e` (**fin**).</span><span class="sxs-lookup"><span data-stu-id="edff0-127">The line is closed with `x` (**close**) and ended with `e` (**end**).</span></span> <span data-ttu-id="edff0-128">Notez que les coordonnées sont fournies dans l’espace de coordonnées relatif et que la taille réelle est déterminée par la **largeur** et la **hauteur**.</span><span class="sxs-lookup"><span data-stu-id="edff0-128">Note that coordinates are given in the relative coordinate space and that the real size is determined by the **width** and **height**.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="edff0-129">[Exemple d’attribut path](/previous-versions/bb264089(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="edff0-129">[Path Attribute Example](/previous-versions/bb264089(v=vs.85)).</span></span> <span data-ttu-id="edff0-130">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="edff0-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 