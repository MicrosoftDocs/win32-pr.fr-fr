---
title: EndArrowLength VML (attribut)
description: EndArrowLength VML (attribut)
ms.assetid: aab898b6-4c59-4471-81fd-621f79610d63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d9d8bfbd24a6a1b79208d50d4d2aef956a5bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509033"
---
# <a name="vml-endarrowlength-attribute"></a><span data-ttu-id="53fc5-103">EndArrowLength VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="53fc5-103">VML EndArrowLength Attribute</span></span>

<span data-ttu-id="53fc5-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="53fc5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="53fc5-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="53fc5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="53fc5-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="53fc5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="53fc5-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="53fc5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="53fc5-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="53fc5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="53fc5-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="53fc5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="53fc5-110">Définit une longueur de flèche pour la fin d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="53fc5-110">Defines an arrowhead length for the end of a line.</span></span> <span data-ttu-id="53fc5-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="53fc5-111">Read/write.</span></span> <span data-ttu-id="53fc5-112">**VgArrowheadLength**.</span><span class="sxs-lookup"><span data-stu-id="53fc5-112">**VgArrowheadLength**.</span></span>

<span data-ttu-id="53fc5-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="53fc5-113">**Applies To**</span></span>

[<span data-ttu-id="53fc5-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="53fc5-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="53fc5-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="53fc5-115">**Tag Syntax**</span></span>

<span data-ttu-id="53fc5-116"><v : *Element* endarrowlength = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="53fc5-116"><v: *element* endarrowlength=" *expression* "></span></span>

<span data-ttu-id="53fc5-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="53fc5-117">**Script Syntax**</span></span>

<span data-ttu-id="53fc5-118">*Element* . endarrowlength = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="53fc5-118">*element* .endarrowlength="*expression*"</span></span>

<span data-ttu-id="53fc5-119">*expression* = *élément*. endarrowlength</span><span class="sxs-lookup"><span data-stu-id="53fc5-119">*expression*=*element*.endarrowlength</span></span>

<span data-ttu-id="53fc5-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="53fc5-120">**Remarks**</span></span>

<span data-ttu-id="53fc5-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="53fc5-121">Values include:</span></span>

-   <span data-ttu-id="53fc5-122">Court</span><span class="sxs-lookup"><span data-stu-id="53fc5-122">Short</span></span>
-   <span data-ttu-id="53fc5-123">Moyenne (par défaut)</span><span class="sxs-lookup"><span data-stu-id="53fc5-123">Medium (default)</span></span>
-   <span data-ttu-id="53fc5-124">Long</span><span class="sxs-lookup"><span data-stu-id="53fc5-124">Long</span></span>

<span data-ttu-id="53fc5-125">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="53fc5-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="53fc5-126">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="53fc5-126">**Example**</span></span>

<span data-ttu-id="53fc5-127">Une ligne est dessinée avec une petite flèche classique à la fin du trait.</span><span class="sxs-lookup"><span data-stu-id="53fc5-127">A line is drawn with a short classic arrowhead on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowlength="short"/>
   </v:line>
```



 

 