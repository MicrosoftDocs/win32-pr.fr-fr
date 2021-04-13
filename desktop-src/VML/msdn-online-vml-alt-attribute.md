---
title: VML Alt (attribut)
description: VML Alt (attribut)
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b420d556e69ed2f987a3a3b10a5709f926dc5c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199352"
---
# <a name="vml-alt-attribute"></a><span data-ttu-id="ec6d4-103">VML Alt (attribut)</span><span class="sxs-lookup"><span data-stu-id="ec6d4-103">VML Alt Attribute</span></span>

<span data-ttu-id="ec6d4-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ec6d4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ec6d4-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ec6d4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ec6d4-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="ec6d4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ec6d4-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="ec6d4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ec6d4-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ec6d4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ec6d4-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ec6d4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ec6d4-110">Définit le texte de remplacement à afficher à la place d’un graphique.</span><span class="sxs-lookup"><span data-stu-id="ec6d4-110">Defines alternative text to be displayed instead of a graphic.</span></span> <span data-ttu-id="ec6d4-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ec6d4-111">Read/write.</span></span> <span data-ttu-id="ec6d4-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="ec6d4-112">**String**.</span></span>

<span data-ttu-id="ec6d4-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="ec6d4-113">**Applies To**</span></span>

[<span data-ttu-id="ec6d4-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="ec6d4-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="ec6d4-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="ec6d4-115">**Tag Syntax**</span></span>

<span data-ttu-id="ec6d4-116"><v : *Element* Alt = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ec6d4-116"><v: *element* alt=" *expression* "></span></span>

<span data-ttu-id="ec6d4-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="ec6d4-117">**Script Syntax**</span></span>

<span data-ttu-id="ec6d4-118">*Element* . Alt = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="ec6d4-118">*element* .alt="*expression*"</span></span>

<span data-ttu-id="ec6d4-119">*expression* = *élément*. Alt</span><span class="sxs-lookup"><span data-stu-id="ec6d4-119">*expression*=*element*.alt</span></span>

<span data-ttu-id="ec6d4-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="ec6d4-120">**Remarks**</span></span>

<span data-ttu-id="ec6d4-121">L’attribut **ALT** est semblable à l’attribut **ALT** HTML standard.</span><span class="sxs-lookup"><span data-stu-id="ec6d4-121">The **Alt** attribute is similar to the standard HTML **Alt** attribute.</span></span> <span data-ttu-id="ec6d4-122">Cet attribut permet aux navigateurs qui convertissent du texte en parole de décrire les éléments graphiques d’une page.</span><span class="sxs-lookup"><span data-stu-id="ec6d4-122">This attribute provides a way for browsers that convert text to speech to describe graphical elements on a page.</span></span>

<span data-ttu-id="ec6d4-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="ec6d4-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="ec6d4-124">**Voir aussi**</span><span class="sxs-lookup"><span data-stu-id="ec6d4-124">**See Also**</span></span>

[<span data-ttu-id="ec6d4-125">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="ec6d4-125">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="ec6d4-126">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="ec6d4-126">**Example**</span></span>

<span data-ttu-id="ec6d4-127">L’élément **ALT** ci-dessous affiche l’expression « rectangle rouge » dans les navigateurs qui convertissent les pages Web en expressions vocales.</span><span class="sxs-lookup"><span data-stu-id="ec6d4-127">The **Alt** element below will display the phrase "Red rectangle" in browsers that convert Web pages to spoken phrases.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="ec6d4-128">[Exemple d’attribut alt](/previous-versions/bb229663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ec6d4-128">[Alt Attribute Example](/previous-versions/bb229663(v=vs.85)).</span></span> <span data-ttu-id="ec6d4-129">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="ec6d4-129">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 