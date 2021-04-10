---
title: FitPath VML (attribut)
description: FitPath VML (attribut)
ms.assetid: f15775ed-f7b7-45d9-83ed-e307daf7451b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1805e59a50c63248ed936f6a849869057a34a6e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199366"
---
# <a name="vml-fitpath-attribute"></a><span data-ttu-id="81db3-103">FitPath VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="81db3-103">VML FitPath Attribute</span></span>

<span data-ttu-id="81db3-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="81db3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="81db3-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="81db3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="81db3-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="81db3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="81db3-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="81db3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="81db3-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="81db3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="81db3-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="81db3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="81db3-110">Définit si le texte correspond au tracé d’une forme.</span><span class="sxs-lookup"><span data-stu-id="81db3-110">Defines whether the text fits the path of a shape.</span></span> <span data-ttu-id="81db3-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="81db3-111">Read/write.</span></span> <span data-ttu-id="81db3-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="81db3-112">**VgTriState**.</span></span>

<span data-ttu-id="81db3-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="81db3-113">**Applies To**</span></span>

[<span data-ttu-id="81db3-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="81db3-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="81db3-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="81db3-115">**Tag Syntax**</span></span>

<span data-ttu-id="81db3-116"><v : *Element* fitpath = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="81db3-116"><v: *element* fitpath=" *expression* "></span></span>

<span data-ttu-id="81db3-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="81db3-117">**Script Syntax**</span></span>

<span data-ttu-id="81db3-118">*Element* . fitpath = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="81db3-118">*element* .fitpath="*expression*"</span></span>

<span data-ttu-id="81db3-119">*expression* = *élément*. fitpath</span><span class="sxs-lookup"><span data-stu-id="81db3-119">*expression*=*element*.fitpath</span></span>

<span data-ttu-id="81db3-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="81db3-120">**Remarks**</span></span>

<span data-ttu-id="81db3-121">Si la **valeur est true**, redimensionne le texte pour remplir le tracé sur lequel il se trouve.</span><span class="sxs-lookup"><span data-stu-id="81db3-121">If **True**, sizes the text to fill the path it lies out on.</span></span> <span data-ttu-id="81db3-122">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="81db3-122">The default is **False**.</span></span>

<span data-ttu-id="81db3-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="81db3-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="81db3-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="81db3-124">**Example**</span></span>

<span data-ttu-id="81db3-125">Le texte correspond au chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="81db3-125">The text will fit the path.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitpath="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 