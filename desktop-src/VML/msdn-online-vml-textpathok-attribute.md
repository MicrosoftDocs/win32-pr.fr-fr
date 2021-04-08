---
title: TextPathOK VML (attribut)
description: TextPathOK VML (attribut)
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06046a4f29c147ef109f0e4670d9965bab77a9fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842341"
---
# <a name="vml-textpathok-attribute"></a><span data-ttu-id="ae1c4-103">TextPathOK VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="ae1c4-103">VML TextPathOK Attribute</span></span>

<span data-ttu-id="ae1c4-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ae1c4-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ae1c4-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ae1c4-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ae1c4-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ae1c4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ae1c4-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ae1c4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ae1c4-110">Détermine si un chemin d’accès de texte sera affiché.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-110">Determines whether a text path will be displayed.</span></span> <span data-ttu-id="ae1c4-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-111">Read/write.</span></span> <span data-ttu-id="ae1c4-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-112">**VgTriState**.</span></span>

<span data-ttu-id="ae1c4-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="ae1c4-113">**Applies To**</span></span>

[<span data-ttu-id="ae1c4-114">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="ae1c4-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="ae1c4-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="ae1c4-115">**Tag Syntax**</span></span>

<span data-ttu-id="ae1c4-116"><v : *Element* textpathok = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ae1c4-116"><v: *element* textpathok=" *expression* "></span></span>

<span data-ttu-id="ae1c4-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="ae1c4-117">**Script Syntax**</span></span>

<span data-ttu-id="ae1c4-118">*élément* .</span><span class="sxs-lookup"><span data-stu-id="ae1c4-118">*element* .</span></span> <span data-ttu-id="ae1c4-119">textpathok = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="ae1c4-119">textpathok= "*expression*"</span></span>

<span data-ttu-id="ae1c4-120">*expression* = *élément*.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-120">*expression*=*element*.</span></span> <span data-ttu-id="ae1c4-121">textpathok</span><span class="sxs-lookup"><span data-stu-id="ae1c4-121">textpathok</span></span>

<span data-ttu-id="ae1c4-122">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="ae1c4-122">**Remarks**</span></span>

<span data-ttu-id="ae1c4-123">Si la **valeur est false**, le chemin d’accès ne peut pas contenir de texte.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-123">If **False**, the path cannot have a text path.</span></span> <span data-ttu-id="ae1c4-124">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-124">The default is **False**.</span></span> <span data-ttu-id="ae1c4-125">Cet attribut doit avoir la valeur **true** pour afficher du texte sur un tracé.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-125">You must have this attribute set to **True** to display text on a path.</span></span>

<span data-ttu-id="ae1c4-126">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="ae1c4-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="ae1c4-127">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="ae1c4-127">**Example**</span></span>

<span data-ttu-id="ae1c4-128">La forme a un tracé de texte.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-128">The shape has a text path.</span></span> <span data-ttu-id="ae1c4-129">Le texte « Hello VML » s’affiche sur une courbe en forme de sourire.</span><span class="sxs-lookup"><span data-stu-id="ae1c4-129">The text "Hello VML" is displayed along a smile-shaped curve.</span></span>


```HTML
   <v:curve id="tc" style="position:relative"
   from="50px 100px" to="400px 100px"
   control1="200px 200px" control2="300px 200px">
   <v:stroke weight="1pt" color="blue"
   filltype="solid"/>
   <v:fill on="True" color="yellow" color2="green" type="gradient"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" id="mytp"
   style="font:normal normal normal 36pt Arial"
   fitpath="True" string="Hello VML"/>
   </v:curve>
```



 

 