---
title: ShadowOK VML (attribut)
description: ShadowOK VML (attribut)
ms.assetid: 88400bf5-f41c-4495-a5d0-9b35c1cae9f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9e6b4ca6b98ce66208e906c45fd560324121e8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031273"
---
# <a name="vml-shadowok-attribute"></a><span data-ttu-id="b38d9-103">ShadowOK VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="b38d9-103">VML ShadowOK Attribute</span></span>

<span data-ttu-id="b38d9-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b38d9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b38d9-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b38d9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b38d9-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="b38d9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b38d9-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="b38d9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b38d9-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b38d9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b38d9-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b38d9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b38d9-110">Détermine si une ombre sera affichée.</span><span class="sxs-lookup"><span data-stu-id="b38d9-110">Determines whether a shadow will be displayed.</span></span> <span data-ttu-id="b38d9-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b38d9-111">Read/write.</span></span> <span data-ttu-id="b38d9-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="b38d9-112">**VgTriState**.</span></span>

<span data-ttu-id="b38d9-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b38d9-113">**Applies To**</span></span>

[<span data-ttu-id="b38d9-114">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b38d9-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="b38d9-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="b38d9-115">**Tag Syntax**</span></span>

<span data-ttu-id="b38d9-116"><v : *Element* shadowok = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b38d9-116"><v: *element* shadowok=" *expression* "></span></span>

<span data-ttu-id="b38d9-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="b38d9-117">**Script Syntax**</span></span>

<span data-ttu-id="b38d9-118">*Element* . shadowok = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b38d9-118">*element* .shadowok="*expression*"</span></span>

<span data-ttu-id="b38d9-119">*expression* = *élément*. shadowok</span><span class="sxs-lookup"><span data-stu-id="b38d9-119">*expression*=*element*.shadowok</span></span>

<span data-ttu-id="b38d9-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="b38d9-120">**Remarks**</span></span>

<span data-ttu-id="b38d9-121">Si la **valeur est false**, le chemin d’accès ne peut pas avoir d’ombre.</span><span class="sxs-lookup"><span data-stu-id="b38d9-121">If **False**, the path cannot have a shadow.</span></span> <span data-ttu-id="b38d9-122">La valeur par défaut est **True**.</span><span class="sxs-lookup"><span data-stu-id="b38d9-122">The default is **True**.</span></span> <span data-ttu-id="b38d9-123">Cet attribut remplace tous les autres attributs fantômes dans l’élément parent ou le **cliché instantané** .</span><span class="sxs-lookup"><span data-stu-id="b38d9-123">This attribute overrides all other shadow attributes in the parent or **Shadow** element.</span></span>

<span data-ttu-id="b38d9-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="b38d9-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="b38d9-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="b38d9-125">**Example**</span></span>

<span data-ttu-id="b38d9-126">La forme n’a pas d’ombre.</span><span class="sxs-lookup"><span data-stu-id="b38d9-126">The shape will not have a shadow.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True" offset="5pt,5pt" color="blue"/>
   <v:path id= "myPath" shadowok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 