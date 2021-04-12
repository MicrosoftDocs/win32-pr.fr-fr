---
title: VML V-Text-Spacing (attribut)
description: VML V-Text-Spacing (attribut)
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab31d1f0b0b1d41b7e99451c422028fe54498483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382306"
---
# <a name="vml-v-text-spacing-attribute"></a><span data-ttu-id="3c11c-103">VML V-Text-Spacing (attribut)</span><span class="sxs-lookup"><span data-stu-id="3c11c-103">VML V-Text-Spacing Attribute</span></span>

<span data-ttu-id="3c11c-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3c11c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3c11c-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3c11c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3c11c-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="3c11c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3c11c-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="3c11c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3c11c-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3c11c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3c11c-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3c11c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3c11c-110">Définit la quantité d’espacement du texte.</span><span class="sxs-lookup"><span data-stu-id="3c11c-110">Defines the amount of spacing for text.</span></span> <span data-ttu-id="3c11c-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3c11c-111">Read/write.</span></span> <span data-ttu-id="3c11c-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="3c11c-112">**VgNumber**.</span></span>

<span data-ttu-id="3c11c-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="3c11c-113">**Applies To**</span></span>

[<span data-ttu-id="3c11c-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="3c11c-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="3c11c-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="3c11c-115">**Tag Syntax**</span></span>

<span data-ttu-id="3c11c-116"><v : *Element* style = "v-Text-Spacing : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="3c11c-116"><v: *element* style="v-text-spacing: *expression* "></span></span>

<span data-ttu-id="3c11c-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="3c11c-117">**Script Syntax**</span></span>

<span data-ttu-id="3c11c-118">*Element* . style. v-Text-spacing = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="3c11c-118">*element* .style.v-text-spacing="*expression*"</span></span>

<span data-ttu-id="3c11c-119">*expression* = *élément*. style. v-espacement du texte</span><span class="sxs-lookup"><span data-stu-id="3c11c-119">*expression*=*element*.style.v-text-spacing</span></span>

<span data-ttu-id="3c11c-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="3c11c-120">**Remarks**</span></span>

<span data-ttu-id="3c11c-121">La valeur par défaut est 100.</span><span class="sxs-lookup"><span data-stu-id="3c11c-121">The default value is 100.</span></span> <span data-ttu-id="3c11c-122">Pour plus d’informations sur l’espacement du texte, consultez l’attribut [V-Text-Spacing-mode](msdn-online-vml-v-text-spacing-mode-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="3c11c-122">See the [V-Text-Spacing-Mode](msdn-online-vml-v-text-spacing-mode-attribute.md) attribute for more information about text spacing.</span></span>

<span data-ttu-id="3c11c-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="3c11c-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="3c11c-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="3c11c-124">**Example**</span></span>

<span data-ttu-id="3c11c-125">L’letterSpacing entre chaque lettre est serré par 200 unités.</span><span class="sxs-lookup"><span data-stu-id="3c11c-125">The letterspacing between each letter is tightened by 200 units.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 