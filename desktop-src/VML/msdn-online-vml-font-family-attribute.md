---
title: Attribut Font-Family VML
description: Attribut Font-Family VML
ms.assetid: 10586ae0-1480-4ffe-a690-ce8464e9bf41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29aa72775e8f00e195462cf3df06097d267b908
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031834"
---
# <a name="vml-font-family-attribute"></a><span data-ttu-id="e65ec-103">Attribut Font-Family VML</span><span class="sxs-lookup"><span data-stu-id="e65ec-103">VML Font-Family Attribute</span></span>

<span data-ttu-id="e65ec-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e65ec-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e65ec-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e65ec-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e65ec-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="e65ec-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e65ec-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="e65ec-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e65ec-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e65ec-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e65ec-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e65ec-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e65ec-110">Définit la famille de la police TextPath.</span><span class="sxs-lookup"><span data-stu-id="e65ec-110">Defines the family of the textpath font.</span></span> <span data-ttu-id="e65ec-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e65ec-111">Read/write.</span></span> <span data-ttu-id="e65ec-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="e65ec-112">**String**.</span></span>

<span data-ttu-id="e65ec-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="e65ec-113">**Applies To**</span></span>

[<span data-ttu-id="e65ec-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="e65ec-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="e65ec-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="e65ec-115">**Tag Syntax**</span></span>

<span data-ttu-id="e65ec-116"><v : *Element* style = "font-family : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="e65ec-116"><v: *element* style="font-family: *expression* "></span></span>

<span data-ttu-id="e65ec-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="e65ec-117">**Script Syntax**</span></span>

<span data-ttu-id="e65ec-118">*Element* . style. FontFamily = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="e65ec-118">*element* .style.fontfamily="*expression*"</span></span>

<span data-ttu-id="e65ec-119">*expression* = *Element*. style. FontFamily</span><span class="sxs-lookup"><span data-stu-id="e65ec-119">*expression*=*element*.style.fontfamily</span></span>

<span data-ttu-id="e65ec-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="e65ec-120">**Remarks**</span></span>

<span data-ttu-id="e65ec-121">Définit le nom de la police.</span><span class="sxs-lookup"><span data-stu-id="e65ec-121">Defines the font name.</span></span> <span data-ttu-id="e65ec-122">Des noms spécifiques tels que Arial peuvent être utilisés ou des types génériques tels qu’Serif, sans serif, cursive, fantastique ou à espacement fixe.</span><span class="sxs-lookup"><span data-stu-id="e65ec-122">Specific names such as Arial can be used or generic types such as serif, sans-serif, cursive, fantasy, or monospace.</span></span> <span data-ttu-id="e65ec-123">Les valeurs sont les mêmes que les attributs de style HTML standard.</span><span class="sxs-lookup"><span data-stu-id="e65ec-123">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="e65ec-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="e65ec-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="e65ec-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="e65ec-125">**Example**</span></span>

<span data-ttu-id="e65ec-126">La famille de polices du texte est Arial.</span><span class="sxs-lookup"><span data-stu-id="e65ec-126">The font family of the text is Arial.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 