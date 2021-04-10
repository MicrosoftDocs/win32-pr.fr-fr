---
title: StrokeOK VML (attribut)
description: StrokeOK VML (attribut)
ms.assetid: f150f87b-1ed9-4c53-bf7f-ebe1e81642fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7a2875e3e6e8374238340ff2a596852e5ebce7c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941201"
---
# <a name="vml-strokeok-attribute"></a><span data-ttu-id="b2128-103">StrokeOK VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="b2128-103">VML StrokeOK Attribute</span></span>

<span data-ttu-id="b2128-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b2128-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b2128-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b2128-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b2128-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="b2128-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b2128-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="b2128-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b2128-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b2128-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b2128-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b2128-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b2128-110">Détermine si un trait sera affiché.</span><span class="sxs-lookup"><span data-stu-id="b2128-110">Determines whether a stroke will be displayed.</span></span> <span data-ttu-id="b2128-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b2128-111">Read/write.</span></span> <span data-ttu-id="b2128-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="b2128-112">**VgTriState**.</span></span>

<span data-ttu-id="b2128-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b2128-113">**Applies To**</span></span>

[<span data-ttu-id="b2128-114">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b2128-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="b2128-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="b2128-115">**Tag Syntax**</span></span>

<span data-ttu-id="b2128-116"><v : *Element* strokeok = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b2128-116"><v: *element* strokeok=" *expression* "></span></span>

<span data-ttu-id="b2128-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="b2128-117">**Script Syntax**</span></span>

<span data-ttu-id="b2128-118">*Element* . strokeok = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b2128-118">*element* .strokeok="*expression*"</span></span>

<span data-ttu-id="b2128-119">*expression* = *élément*. strokeok</span><span class="sxs-lookup"><span data-stu-id="b2128-119">*expression*=*element*.strokeok</span></span>

<span data-ttu-id="b2128-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="b2128-120">**Remarks**</span></span>

<span data-ttu-id="b2128-121">Si la **valeur est false**, le tracé ne peut pas être rayé.</span><span class="sxs-lookup"><span data-stu-id="b2128-121">If **False**, the path cannot be stroked.</span></span> <span data-ttu-id="b2128-122">La valeur par défaut est **True**.</span><span class="sxs-lookup"><span data-stu-id="b2128-122">The default is **True**.</span></span> <span data-ttu-id="b2128-123">Cet attribut remplace tous les autres attributs de trait dans l’élément parent ou **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="b2128-123">This attribute overrides all other stroke attributes in the parent or **Stroke** element.</span></span>

<span data-ttu-id="b2128-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="b2128-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="b2128-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="b2128-125">**Example**</span></span>

<span data-ttu-id="b2128-126">Le chemin d’accès ne sera pas rayé.</span><span class="sxs-lookup"><span data-stu-id="b2128-126">The path will not be stroked.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" strokeok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 