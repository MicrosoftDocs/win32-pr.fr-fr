---
title: Attribut Font-Size VML
description: Attribut Font-Size VML
ms.assetid: 49394cd5-3009-424a-97d3-28c85d874bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c02b2df8fb0076ed6df6342e40b980ed8aa248e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463675"
---
# <a name="vml-font-size-attribute"></a><span data-ttu-id="2f4b4-103">Attribut Font-Size VML</span><span class="sxs-lookup"><span data-stu-id="2f4b4-103">VML Font-Size Attribute</span></span>

<span data-ttu-id="2f4b4-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2f4b4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2f4b4-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="2f4b4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2f4b4-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="2f4b4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2f4b4-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="2f4b4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2f4b4-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2f4b4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2f4b4-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2f4b4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2f4b4-110">Définit la taille de la police.</span><span class="sxs-lookup"><span data-stu-id="2f4b4-110">Defines the size of the font.</span></span> <span data-ttu-id="2f4b4-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2f4b4-111">Read/write.</span></span> <span data-ttu-id="2f4b4-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="2f4b4-112">**String**.</span></span>

<span data-ttu-id="2f4b4-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="2f4b4-113">**Applies To**</span></span>

[<span data-ttu-id="2f4b4-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="2f4b4-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="2f4b4-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="2f4b4-115">**Tag Syntax**</span></span>

<span data-ttu-id="2f4b4-116"><v : *Element* style = "font-size : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="2f4b4-116"><v: *element* style="font-size: *expression* "></span></span>

<span data-ttu-id="2f4b4-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="2f4b4-117">**Script Syntax**</span></span>

<span data-ttu-id="2f4b4-118">*Element* . style. FontSize = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="2f4b4-118">*element* .style.fontsize="*expression*"</span></span>

<span data-ttu-id="2f4b4-119">*expression* = *Element*. style. FontSize</span><span class="sxs-lookup"><span data-stu-id="2f4b4-119">*expression*=*element*.style.fontsize</span></span>

<span data-ttu-id="2f4b4-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="2f4b4-120">**Remarks**</span></span>

<span data-ttu-id="2f4b4-121">La taille de police est définie en points.</span><span class="sxs-lookup"><span data-stu-id="2f4b4-121">The font size is defined in points.</span></span> <span data-ttu-id="2f4b4-122">Les valeurs sont les mêmes que les attributs de style HTML standard.</span><span class="sxs-lookup"><span data-stu-id="2f4b4-122">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="2f4b4-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="2f4b4-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="2f4b4-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2f4b4-124">**Example**</span></span>

<span data-ttu-id="2f4b4-125">La taille de police est de 36 points.</span><span class="sxs-lookup"><span data-stu-id="2f4b4-125">The font size is 36 points.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 