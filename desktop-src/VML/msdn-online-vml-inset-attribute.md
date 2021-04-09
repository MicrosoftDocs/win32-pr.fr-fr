---
title: Attribut incrusté VML
description: Attribut incrusté VML
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83f2ea38ef4ca90f6687196335d2edd2d39c09c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101796"
---
# <a name="vml-inset-attribute"></a><span data-ttu-id="0962e-103">Attribut incrusté VML</span><span class="sxs-lookup"><span data-stu-id="0962e-103">VML Inset Attribute</span></span>

<span data-ttu-id="0962e-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0962e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0962e-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0962e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0962e-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="0962e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0962e-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="0962e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0962e-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0962e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0962e-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0962e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0962e-110">Spécifie les valeurs de marge intérieure pour le texte de zone de texte.</span><span class="sxs-lookup"><span data-stu-id="0962e-110">Specifies inner margin values for textbox text.</span></span> <span data-ttu-id="0962e-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0962e-111">Read/write.</span></span> <span data-ttu-id="0962e-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="0962e-112">**String**.</span></span>

<span data-ttu-id="0962e-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="0962e-113">**Applies To**</span></span>

[<span data-ttu-id="0962e-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="0962e-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="0962e-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="0962e-115">**Tag Syntax**</span></span>

<span data-ttu-id="0962e-116"><v : *élément* incrusté = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="0962e-116"><v: *element* inset=" *expression* "></span></span>

<span data-ttu-id="0962e-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="0962e-117">**Script Syntax**</span></span>

<span data-ttu-id="0962e-118">*Element* . incrusté = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="0962e-118">*element* .inset="*expression*"</span></span>

<span data-ttu-id="0962e-119">*expression* = *élément*. incrusté</span><span class="sxs-lookup"><span data-stu-id="0962e-119">*expression*=*element*.inset</span></span>

<span data-ttu-id="0962e-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="0962e-120">**Remarks**</span></span>

<span data-ttu-id="0962e-121">La valeur de marge de texte interne est spécifiée sous la forme d’une chaîne contenant quatre valeurs, séparées par des virgules ou des espaces.</span><span class="sxs-lookup"><span data-stu-id="0962e-121">The internal text margin value is specified as a string containing four values, each separated by commas or spaces.</span></span> <span data-ttu-id="0962e-122">Les valeurs mesurent les incrustations à partir des bords gauche, supérieur, droit et inférieur de la zone spécifiée par l’attribut [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) de **path**.</span><span class="sxs-lookup"><span data-stu-id="0962e-122">The values measure inset from the left, top, right, and bottom edges of the box specified by the [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) attribute of **Path**.</span></span> <span data-ttu-id="0962e-123">Les valeurs manquantes sont définies sur la valeur par défaut, soit « 0.1 in, 0,05 dans, 0.1 in, 0,05 dans ».</span><span class="sxs-lookup"><span data-stu-id="0962e-123">Missing values are set to the default, which is "0.1in, 0.05in, 0.1in, 0.05in".</span></span>

<span data-ttu-id="0962e-124">Pour les formes pivotées dans des navigateurs qui ne prennent pas en charge la rotation, le cadre englobant sera aligné sur le multiple le plus proche de 90 degrés.</span><span class="sxs-lookup"><span data-stu-id="0962e-124">For rotated shapes in browsers that do not support rotation, the bounding box will snap to the closest multiple of 90 degrees.</span></span>

<span data-ttu-id="0962e-125">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="0962e-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="0962e-126">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="0962e-126">**Example**</span></span>

<span data-ttu-id="0962e-127">La zone de texte aura une marge en incrustation de 10 pixels.</span><span class="sxs-lookup"><span data-stu-id="0962e-127">The textbox will have an inset margin of 10 pixels.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox" inset="10px, 10px, 10px, 10px">
   VML
   </v:textbox/>
   </v:shape>
```



 

 