---
title: Attribut des couleurs VML
description: Attribut des couleurs VML
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c5df5b2dc97c19441d6abaf6cd6c03d949c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508033"
---
# <a name="vml-colors-attribute"></a><span data-ttu-id="315db-103">Attribut des couleurs VML</span><span class="sxs-lookup"><span data-stu-id="315db-103">VML Colors Attribute</span></span>

<span data-ttu-id="315db-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="315db-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="315db-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="315db-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="315db-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="315db-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="315db-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="315db-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="315db-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="315db-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="315db-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="315db-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="315db-110">Définit plusieurs couleurs pour un remplissage dégradé.</span><span class="sxs-lookup"><span data-stu-id="315db-110">Defines multiple colors for a gradient fill.</span></span> <span data-ttu-id="315db-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="315db-111">Read/write.</span></span> <span data-ttu-id="315db-112">**IVgGradientColorArray**.</span><span class="sxs-lookup"><span data-stu-id="315db-112">**IVgGradientColorArray**.</span></span>

<span data-ttu-id="315db-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="315db-113">**Applies To**</span></span>

[<span data-ttu-id="315db-114">Complète</span><span class="sxs-lookup"><span data-stu-id="315db-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="315db-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="315db-115">**Tag Syntax**</span></span>

<span data-ttu-id="315db-116"><v : *Element* Colors = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="315db-116"><v: *element* colors=" *expression* "></span></span>

<span data-ttu-id="315db-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="315db-117">**Script Syntax**</span></span>

<span data-ttu-id="315db-118">*Element* . Colors = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="315db-118">*element* .colors="*expression*"</span></span>

<span data-ttu-id="315db-119">*expression* = *Element*. couleurs</span><span class="sxs-lookup"><span data-stu-id="315db-119">*expression*=*element*.colors</span></span>

<span data-ttu-id="315db-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="315db-120">**Remarks**</span></span>

<span data-ttu-id="315db-121">Utilisé pour définir un tableau constitué de valeurs jumelées de pourcentages ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) et de couleurs ([VgColor](msdn-online-vml-ivgcolor.md)).</span><span class="sxs-lookup"><span data-stu-id="315db-121">Used to define an array consisting of paired values of percentages ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) and color ([VgColor](msdn-online-vml-ivgcolor.md)).</span></span> <span data-ttu-id="315db-122">Le tableau crée un remplissage fusionné à l’aide de chaque point du tableau, en commençant à 0% (défini par la **couleur**) et en se terminant à 100% (défini par **Color2**).</span><span class="sxs-lookup"><span data-stu-id="315db-122">The array creates a blended fill using each point in the array, starting at 0% (defined by **Color**) and ending at 100% (defined by **Color2**).</span></span> <span data-ttu-id="315db-123">Les couleurs intermédiaires peuvent être définies en affectant une valeur de couleur à un pourcentage.</span><span class="sxs-lookup"><span data-stu-id="315db-123">Intermediate colors along the way can be defined by assigning a color value to a percentage.</span></span> <span data-ttu-id="315db-124">Les paires pourcentage et couleur ne sont pas séparées par une virgule, mais les paires sont séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="315db-124">The percent and color pair are not separated by a comma, but pairs are separated from each other by commas.</span></span>

<span data-ttu-id="315db-125">Attribut standard VML</span><span class="sxs-lookup"><span data-stu-id="315db-125">VML Standard Attribute</span></span>

<span data-ttu-id="315db-126">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="315db-126">**Example**</span></span>

<span data-ttu-id="315db-127">La forme a un remplissage dégradé constitué de quatre couleurs, en commençant par la couleur rouge, en utilisant la couleur jaune, puis en vert et en finallyblue.</span><span class="sxs-lookup"><span data-stu-id="315db-127">The shape has a gradient fill consisting of four colors, starting with red, blending to yellow, then green, and finallyblue.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   colors="30% yellow,70% green"/>
   </v:shape>
```



 

 