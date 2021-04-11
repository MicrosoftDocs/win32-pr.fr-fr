---
title: Attribut VML XScale
description: Attribut VML XScale
ms.assetid: b876201d-87d1-4795-8f7f-33712a8bf493
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3221ab44cad9eb9f422ce451f618eb8eeba55bcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315305"
---
# <a name="vml-xscale-attribute"></a><span data-ttu-id="55bdc-103">Attribut VML XScale</span><span class="sxs-lookup"><span data-stu-id="55bdc-103">VML XScale Attribute</span></span>

<span data-ttu-id="55bdc-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="55bdc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="55bdc-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="55bdc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="55bdc-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="55bdc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="55bdc-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="55bdc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="55bdc-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="55bdc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="55bdc-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="55bdc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="55bdc-110">Détermine si un TextPath droit est utilisé à la place du tracé de la forme.</span><span class="sxs-lookup"><span data-stu-id="55bdc-110">Determines whether a straight textpath will be used instead of the shape path.</span></span> <span data-ttu-id="55bdc-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="55bdc-111">Read/write.</span></span> <span data-ttu-id="55bdc-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="55bdc-112">**VgTriState**.</span></span>

<span data-ttu-id="55bdc-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="55bdc-113">**Applies To**</span></span>

[<span data-ttu-id="55bdc-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="55bdc-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="55bdc-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="55bdc-115">**Tag Syntax**</span></span>

<span data-ttu-id="55bdc-116"><v : *Element* style = "XScale : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="55bdc-116"><v: *element* style="xscale: *expression* "></span></span>

<span data-ttu-id="55bdc-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="55bdc-117">**Script Syntax**</span></span>

<span data-ttu-id="55bdc-118">*Element* . style. XScale = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="55bdc-118">*element* .style.xscale="*expression*"</span></span>

<span data-ttu-id="55bdc-119">*expression* = *Element*. style. XScale</span><span class="sxs-lookup"><span data-stu-id="55bdc-119">*expression*=*element*.style.xscale</span></span>

<span data-ttu-id="55bdc-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="55bdc-120">**Remarks**</span></span>

<span data-ttu-id="55bdc-121">Si la valeur est **true**, le texte est exécuté le long de APATH de gauche à droite le long de la valeur x de la limite inférieure de la forme.</span><span class="sxs-lookup"><span data-stu-id="55bdc-121">If **True**, the text runs along apath from left to right along the x value of the lower boundary of the shape.</span></span> <span data-ttu-id="55bdc-122">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="55bdc-122">The default value is **False**.</span></span>

<span data-ttu-id="55bdc-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="55bdc-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="55bdc-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="55bdc-124">**Example**</span></span>

<span data-ttu-id="55bdc-125">Le texte s’affiche comme s’il était dessiné sur une ligne horizontale, même si le tracé de la forme est une diagonale.</span><span class="sxs-lookup"><span data-stu-id="55bdc-125">The text will appear as if it were drawn on a horizontal line, even though the shape path is a diagonal.</span></span>


```HTML
   <v:line from="100 100" to="400 400">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="xscale:true;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 