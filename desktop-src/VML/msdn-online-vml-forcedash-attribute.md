---
title: ForceDash VML (attribut)
description: ForceDash VML (attribut)
ms.assetid: 659e99bb-16d9-425a-97b1-7767c065ec41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bcec4a694a6449412aa07ec69aa9a817aa917c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031550"
---
# <a name="vml-forcedash-attribute"></a><span data-ttu-id="a8fe1-103">ForceDash VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="a8fe1-103">VML ForceDash Attribute</span></span>

<span data-ttu-id="a8fe1-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a8fe1-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a8fe1-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a8fe1-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a8fe1-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a8fe1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a8fe1-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a8fe1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a8fe1-110">Détermine si un contour en pointillés est utilisé pour dessiner une forme lorsqu’une forme n’a pas de trait ou de remplissage.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-110">Determines whether a dashed outline is used to draw a shape when a shape has no line or fill.</span></span> <span data-ttu-id="a8fe1-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-111">Read/write.</span></span> <span data-ttu-id="a8fe1-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-112">**VgTriState**.</span></span>

<span data-ttu-id="a8fe1-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="a8fe1-113">**Applies To**</span></span>

[<span data-ttu-id="a8fe1-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="a8fe1-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a8fe1-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="a8fe1-115">**Tag Syntax**</span></span>

<span data-ttu-id="a8fe1-116"><v : *Element* o :forcedash = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a8fe1-116"><v: *element* o:forcedash=" *expression* "></span></span>

<span data-ttu-id="a8fe1-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="a8fe1-117">**Remarks**</span></span>

<span data-ttu-id="a8fe1-118">Utilisé par les espaces réservés Microsoft PowerPoint pour dessiner un contour en pointillés lorsqu’il n’y a pas de ligne et aucun remplissage pour une forme.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-118">Used by Microsoft PowerPoint placeholders to draw a dashed outline when there is no line and no fill for a shape.</span></span> <span data-ttu-id="a8fe1-119">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-119">Default is **False**.</span></span> <span data-ttu-id="a8fe1-120">Si la **valeur est true**, un contour en pointillés est utilisé pour indiquer un espace réservé.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-120">If **True**, a dashed outline will be used to indicate a placeholder.</span></span>

<span data-ttu-id="a8fe1-121">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="a8fe1-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="a8fe1-122">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="a8fe1-122">**Example**</span></span>

<span data-ttu-id="a8fe1-123">Une ligne en pointillés est utilisée pour afficher la forme en l’absence de ligne ou de remplissage.</span><span class="sxs-lookup"><span data-stu-id="a8fe1-123">A dashed line will be used to render the shape if there is no line or fill.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:forcedash="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 