---
title: Attribut de police VML
description: Attribut de police VML
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bace73b90cac7519ea6abacb73c80506c655e133
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106530797"
---
# <a name="vml-font-attribute"></a><span data-ttu-id="603ce-103">Attribut de police VML</span><span class="sxs-lookup"><span data-stu-id="603ce-103">VML Font Attribute</span></span>

<span data-ttu-id="603ce-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="603ce-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="603ce-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="603ce-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="603ce-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="603ce-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="603ce-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="603ce-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="603ce-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="603ce-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="603ce-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="603ce-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="603ce-110">Spécifie une valeur composée d’attributs de police.</span><span class="sxs-lookup"><span data-stu-id="603ce-110">Specifies a compound value of font attributes.</span></span> <span data-ttu-id="603ce-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="603ce-111">Read/write.</span></span> <span data-ttu-id="603ce-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="603ce-112">**String**.</span></span>

<span data-ttu-id="603ce-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="603ce-113">**Applies To**</span></span>

[<span data-ttu-id="603ce-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="603ce-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="603ce-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="603ce-115">**Tag Syntax**</span></span>

<span data-ttu-id="603ce-116"><v : *Element* style = "font : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="603ce-116"><v: *element* style="font: *expression* "></span></span>

<span data-ttu-id="603ce-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="603ce-117">**Script Syntax**</span></span>

<span data-ttu-id="603ce-118">*Element* . style. font = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="603ce-118">*element* .style.font="*expression*"</span></span>

<span data-ttu-id="603ce-119">*expression* = *Element*. style. font</span><span class="sxs-lookup"><span data-stu-id="603ce-119">*expression*=*element*.style.font</span></span>

<span data-ttu-id="603ce-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="603ce-120">**Remarks**</span></span>

<span data-ttu-id="603ce-121">Définit les attributs d’une police, y compris famille, style, poids, taille et variante.</span><span class="sxs-lookup"><span data-stu-id="603ce-121">Defines the attributes of a font, including family, style, weight, size, and variant.</span></span> <span data-ttu-id="603ce-122">L’ordre des définitions dans la chaîne est le suivant : **style de police**, **police-variante**, police **-poids**, **police-taille**, **hauteur de ligne** et **famille de polices**.</span><span class="sxs-lookup"><span data-stu-id="603ce-122">The order of definitions in the string is: **font-style**, **font-variant**, **font-weight**, **font-size**, **line-height**, and **font-family**.</span></span> <span data-ttu-id="603ce-123">Les valeurs sont les mêmes que les attributs de style HTML standard.</span><span class="sxs-lookup"><span data-stu-id="603ce-123">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="603ce-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="603ce-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="603ce-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="603ce-125">**Example**</span></span>

<span data-ttu-id="603ce-126">La police du texte TextPath est italique, petite majuscule, gras, 36 point Arial.</span><span class="sxs-lookup"><span data-stu-id="603ce-126">The font of the textpath text is italic, small-caps, bold, 36 point Arial.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 