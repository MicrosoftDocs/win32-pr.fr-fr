---
title: Attribut VML V-Text-Spacing-mode
description: Attribut VML V-Text-Spacing-mode
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a288f89a1405412ba8c582a5c52c7bfe56809c38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463671"
---
# <a name="vml-v-text-spacing-mode-attribute"></a><span data-ttu-id="31a37-103">Attribut VML V-Text-Spacing-mode</span><span class="sxs-lookup"><span data-stu-id="31a37-103">VML V-Text-Spacing-Mode Attribute</span></span>

<span data-ttu-id="31a37-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="31a37-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="31a37-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="31a37-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="31a37-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="31a37-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="31a37-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="31a37-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="31a37-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="31a37-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="31a37-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="31a37-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="31a37-110">Définit le mode pour letterSpacing.</span><span class="sxs-lookup"><span data-stu-id="31a37-110">Defines the mode for letterspacing.</span></span> <span data-ttu-id="31a37-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="31a37-111">Read/write.</span></span> <span data-ttu-id="31a37-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="31a37-112">**String**.</span></span>

<span data-ttu-id="31a37-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="31a37-113">**Applies To**</span></span>

[<span data-ttu-id="31a37-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="31a37-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="31a37-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="31a37-115">**Tag Syntax**</span></span>

<span data-ttu-id="31a37-116"><v : *Element* style = "v-Text-Spacing-mode : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="31a37-116"><v: *element* style="v-text-spacing-mode: *expression* "></span></span>

<span data-ttu-id="31a37-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="31a37-117">**Script Syntax**</span></span>

<span data-ttu-id="31a37-118">*Element* . style. v-Text-Spacing-mode = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="31a37-118">*element* .style.v-text-spacing-mode="*expression*"</span></span>

<span data-ttu-id="31a37-119">*expression* = *Element*. style. v-Text-Spacing-mode</span><span class="sxs-lookup"><span data-stu-id="31a37-119">*expression*=*element*.style.v-text-spacing-mode</span></span>

<span data-ttu-id="31a37-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="31a37-120">**Remarks**</span></span>

<span data-ttu-id="31a37-121">Les valeurs incluent</span><span class="sxs-lookup"><span data-stu-id="31a37-121">Values include</span></span>

-   <span data-ttu-id="31a37-122">**resserrer** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="31a37-122">**tightening** (default)</span></span>
-   <span data-ttu-id="31a37-123">**suivre**</span><span class="sxs-lookup"><span data-stu-id="31a37-123">**tracking**</span></span>

<span data-ttu-id="31a37-124">Cet attribut détermine si l’espace sera supprimé entre chaque lettre (resserrer) ou ajoutée entre chaque lettre (suivi).</span><span class="sxs-lookup"><span data-stu-id="31a37-124">This attribute determines whether space will be removed between each letter (tightening) or added between each letter (tracking).</span></span> <span data-ttu-id="31a37-125">La quantité de modification de l’letterSpacing est définie par l’attribut [V-Text-Spacing](msdn-online-vml-v-text-spacing-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="31a37-125">The amount of letterspacing change is defined by the [V-Text-Spacing](msdn-online-vml-v-text-spacing-attribute.md) attribute.</span></span>

<span data-ttu-id="31a37-126">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="31a37-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="31a37-127">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="31a37-127">**Example**</span></span>

<span data-ttu-id="31a37-128">L’letterSpacing entre chaque lettre est augmentée de 200 unités.</span><span class="sxs-lookup"><span data-stu-id="31a37-128">The letterspacing between each letter is increased by 200 units.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 