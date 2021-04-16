---
title: Attribut titre (Shape) (VML)
description: Attribut titre (Shape) (VML)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075b1cf078617abd3486ba55008794e1342efa63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463663"
---
# <a name="title-attribute-shapevml"></a><span data-ttu-id="74446-103">Attribut titre (Shape) (VML)</span><span class="sxs-lookup"><span data-stu-id="74446-103">Title Attribute (Shape)(VML)</span></span>

<span data-ttu-id="74446-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="74446-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="74446-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="74446-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="74446-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="74446-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="74446-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="74446-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="74446-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="74446-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="74446-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="74446-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="74446-110">Définit le texte affiché lorsque le pointeur de la souris se déplace sur la forme.</span><span class="sxs-lookup"><span data-stu-id="74446-110">Defines the text displayed when the mouse pointer moves over the shape.</span></span> <span data-ttu-id="74446-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="74446-111">Read/write.</span></span> <span data-ttu-id="74446-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="74446-112">**String**.</span></span>

<span data-ttu-id="74446-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="74446-113">**Applies To**</span></span>

[<span data-ttu-id="74446-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="74446-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="74446-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="74446-115">**Tag Syntax**</span></span>

<span data-ttu-id="74446-116"><v : *élément* title = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="74446-116"><v: *element* title=" *expression* "></span></span>

<span data-ttu-id="74446-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="74446-117">**Script Syntax**</span></span>

<span data-ttu-id="74446-118">*Element* . title = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="74446-118">*element* .title="*expression*"</span></span>

<span data-ttu-id="74446-119">*expression* = *Element*. title</span><span class="sxs-lookup"><span data-stu-id="74446-119">*expression*=*element*.title</span></span>

<span data-ttu-id="74446-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="74446-120">**Remarks**</span></span>

<span data-ttu-id="74446-121">L’attribut **title** est semblable à l’attribut de **titre** HTML standard.</span><span class="sxs-lookup"><span data-stu-id="74446-121">The **Title** attribute is similar to the standard HTML **Title** attribute.</span></span> <span data-ttu-id="74446-122">Le comportement d’un titre est semblable à celui d’une info-bulle Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="74446-122">The behavior of a title is similar to a Microsoft Windows ToolTip.</span></span>

<span data-ttu-id="74446-123">**Attribut standard VML**</span><span class="sxs-lookup"><span data-stu-id="74446-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="74446-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="74446-124">**Example**</span></span>

<span data-ttu-id="74446-125">Le titre de la forme est « affichage de l’info-bulle » et s’affiche lorsque le pointeur de la souris se déplace au-dessus de la forme.</span><span class="sxs-lookup"><span data-stu-id="74446-125">The title of the shape is "ToolTip display" and will appear when the mouse pointer moves over the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="74446-126">[Exemple d’attribut title](/previous-versions/bb264097(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="74446-126">[Title Attribute Example](/previous-versions/bb264097(v=vs.85)).</span></span> <span data-ttu-id="74446-127">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="74446-127">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 