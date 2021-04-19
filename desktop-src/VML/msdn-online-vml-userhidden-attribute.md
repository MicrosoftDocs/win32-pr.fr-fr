---
title: UserHidden VML (attribut)
description: UserHidden VML (attribut)
ms.assetid: 0e4616c7-a456-4157-b77a-56cd289e913c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 519857d53cbec985afae31a5e7dea8811773dc43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106544153"
---
# <a name="vml-userhidden-attribute"></a><span data-ttu-id="22a7d-103">UserHidden VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="22a7d-103">VML UserHidden Attribute</span></span>

<span data-ttu-id="22a7d-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="22a7d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="22a7d-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="22a7d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="22a7d-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="22a7d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="22a7d-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="22a7d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="22a7d-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="22a7d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="22a7d-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="22a7d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="22a7d-110">Détermine si une ancre de script est masquée.</span><span class="sxs-lookup"><span data-stu-id="22a7d-110">Determines whether a script anchor is hidden.</span></span> <span data-ttu-id="22a7d-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="22a7d-111">Read/write.</span></span> <span data-ttu-id="22a7d-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="22a7d-112">**VgTriState**.</span></span>

<span data-ttu-id="22a7d-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="22a7d-113">**Applies To**</span></span>

[<span data-ttu-id="22a7d-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="22a7d-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="22a7d-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="22a7d-115">**Tag Syntax**</span></span>

<span data-ttu-id="22a7d-116"><v : *Element* o :userhidden = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="22a7d-116"><v: *element* o:userhidden=" *expression* "></span></span>

<span data-ttu-id="22a7d-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="22a7d-117">**Remarks**</span></span>

<span data-ttu-id="22a7d-118">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="22a7d-118">The default is **False**.</span></span> <span data-ttu-id="22a7d-119">Si la **valeur est true**, les ancres de script restent masquées même si la forme est visible dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="22a7d-119">If **True**, script anchors stay hidden even if the shape is otherwise visible.</span></span>

<span data-ttu-id="22a7d-120">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="22a7d-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="22a7d-121">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="22a7d-121">**Example**</span></span>

<span data-ttu-id="22a7d-122">L’ancre de script de la forme est masquée.</span><span class="sxs-lookup"><span data-stu-id="22a7d-122">The script anchor of the shape is hidden.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" userhidden="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 