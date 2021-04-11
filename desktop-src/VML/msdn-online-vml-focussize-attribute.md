---
title: FocusSize VML (attribut)
description: FocusSize VML (attribut)
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8149973932e9601be2caa0306eefcec08951b238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031833"
---
# <a name="vml-focussize-attribute"></a><span data-ttu-id="b4aa4-103">FocusSize VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="b4aa4-103">VML FocusSize Attribute</span></span>

<span data-ttu-id="b4aa4-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b4aa4-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b4aa4-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b4aa4-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b4aa4-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b4aa4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b4aa4-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b4aa4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b4aa4-110">Définit la taille du focus pour les remplissages radiaux.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-110">Defines the focus size for radial fills.</span></span> <span data-ttu-id="b4aa4-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-111">Read/write.</span></span> <span data-ttu-id="b4aa4-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-112">**VgVector2D**.</span></span>

<span data-ttu-id="b4aa4-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b4aa4-113">**Applies To**</span></span>

[<span data-ttu-id="b4aa4-114">Complète</span><span class="sxs-lookup"><span data-stu-id="b4aa4-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="b4aa4-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="b4aa4-115">**Tag Syntax**</span></span>

<span data-ttu-id="b4aa4-116"><v : *Element* focussize = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b4aa4-116"><v: *element* focussize=" *expression* "></span></span>

<span data-ttu-id="b4aa4-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="b4aa4-117">**Script Syntax**</span></span>

<span data-ttu-id="b4aa4-118">*Element* . focussize = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b4aa4-118">*element* .focussize="*expression*"</span></span>

<span data-ttu-id="b4aa4-119">*expression* = *élément*. focussize</span><span class="sxs-lookup"><span data-stu-id="b4aa4-119">*expression*=*element*.focussize</span></span>

<span data-ttu-id="b4aa4-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="b4aa4-120">**Remarks**</span></span>

<span data-ttu-id="b4aa4-121">Les valeurs sont des fractions de la largeur et de la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-121">The values are fractions of the width and height of the shape.</span></span> <span data-ttu-id="b4aa4-122">Le premier est un pourcentage du remplissage jusqu’au bord droit de la forme et le deuxième est un pourcentage du remplissage jusqu’au fond de la forme.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-122">The first is a percentage of the fill to the right edge of the shape and the second is a percentage of the fill to the bottom of the shape.</span></span> <span data-ttu-id="b4aa4-123">La valeur par défaut est 0,0.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-123">The default value is 0,0.</span></span> <span data-ttu-id="b4aa4-124">Une valeur **FocusSize** de 100%, 100% et un **FocusPosition** de 0, 0 ferait que Color2 domine complètement la fusion.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-124">A **FocusSize** value of 100%,100% and a **FocusPosition** of 0,0 would make Color2 dominate the blend completely.</span></span> <span data-ttu-id="b4aa4-125">Les petites valeurs d’environ 10%, 10% sont recommandées pour les fusions équilibrées.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-125">Small values of around 10%,10% are recommended for balanced blends.</span></span>

<span data-ttu-id="b4aa4-126">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="b4aa4-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="b4aa4-127">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="b4aa4-127">**Example**</span></span>

<span data-ttu-id="b4aa4-128">Le remplissage radial crée une fusion à partir du centre en bleu et devient rouge sur les quatre bords.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-128">The radial fill will create a blend starting in the center as blue and becoming red on all four edges.</span></span> <span data-ttu-id="b4aa4-129">Le centre de la fusion est défini par **FocusPosition** et la taille de la couleur de début interne est déterminée par **FocusSize**.</span><span class="sxs-lookup"><span data-stu-id="b4aa4-129">The center of the blend is defined by **FocusPosition** and the size of the inner starting color is determined by **FocusSize**.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l1,200, 200,200, 200,1 x e">
   <v:fill type="gradientradial" color="red" color2="blue"
   focusposition=".5,.5" focussize=".1,.1"/>
   </v:shape>
```



 

 