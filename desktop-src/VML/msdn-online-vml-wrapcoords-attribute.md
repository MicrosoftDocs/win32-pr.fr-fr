---
title: WrapCoords VML (attribut)
description: WrapCoords VML (attribut)
ms.assetid: 14a67ca9-3d36-4523-bdb1-5b7c36cd3d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4dc57b37cd84563c8ba3132244dff6daf6b23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727964"
---
# <a name="vml-wrapcoords-attribute"></a><span data-ttu-id="cde66-103">WrapCoords VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="cde66-103">VML WrapCoords Attribute</span></span>

<span data-ttu-id="cde66-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cde66-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cde66-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cde66-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cde66-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="cde66-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cde66-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="cde66-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cde66-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cde66-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cde66-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cde66-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cde66-110">Définit le polygone englobant qui entoure une forme.</span><span class="sxs-lookup"><span data-stu-id="cde66-110">Defines the bounding polygon that surrounds a shape.</span></span> <span data-ttu-id="cde66-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="cde66-111">Read/write.</span></span> <span data-ttu-id="cde66-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="cde66-112">**String**.</span></span>

<span data-ttu-id="cde66-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="cde66-113">**Applies To**</span></span>

[<span data-ttu-id="cde66-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="cde66-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="cde66-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="cde66-115">**Tag Syntax**</span></span>

<span data-ttu-id="cde66-116"><v : *Element* o :wrapcoords = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="cde66-116"><v: *element* o:wrapcoords=" *expression* "></span></span>

<span data-ttu-id="cde66-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="cde66-117">**Remarks**</span></span>

<span data-ttu-id="cde66-118">Décrit une liste de x et ycoordinates délimitée par des virgules ; autrement dit, « x1, y1, x2, Y2, x3, Y3,... » Cela est utilisé lorsque le texte est fortement enveloppé autour d’une forme.</span><span class="sxs-lookup"><span data-stu-id="cde66-118">Describes a comma-delimited list of x and ycoordinates; that is, "x1,y1,x2,y2,x3,y3,..." This is used when text is tightly wrapped around a shape.</span></span> <span data-ttu-id="cde66-119">La valeur par défaut est **null** (une chaîne vide) jusqu’à ce que l’attribut **mso-Wrap-mode** soit défini sur **Elevé** ou **sur**.</span><span class="sxs-lookup"><span data-stu-id="cde66-119">The default is **NULL** (an empty string) until the **MSO-Wrap-Mode** attribute is set to **tight** or **through**.</span></span>

<span data-ttu-id="cde66-120">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="cde66-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="cde66-121">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="cde66-121">**Example**</span></span>

<span data-ttu-id="cde66-122">La forme comporte un rectangle englobant de texte de retour de 5 unités plus grande que le tracé.</span><span class="sxs-lookup"><span data-stu-id="cde66-122">The shape has a text wrap bounding box that is 5 units larger than the path.</span></span>


```HTML
   <v:shape id="rect01" WrapCoords="0,0 0,200, 200,200, 200,0"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 