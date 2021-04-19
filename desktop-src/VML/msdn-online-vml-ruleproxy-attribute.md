---
title: RuleProxy VML (attribut)
description: RuleProxy VML (attribut)
ms.assetid: 040e80f8-65b6-491d-812d-421800801374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c76116fc1f31c379f15c3229fcbe70dc7938f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510276"
---
# <a name="vml-ruleproxy-attribute"></a><span data-ttu-id="8e3da-103">RuleProxy VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="8e3da-103">VML RuleProxy Attribute</span></span>

<span data-ttu-id="8e3da-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8e3da-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8e3da-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="8e3da-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8e3da-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="8e3da-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8e3da-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="8e3da-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8e3da-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8e3da-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8e3da-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8e3da-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8e3da-110">Détermine si un proxy pour le moteur de règles sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="8e3da-110">Determines whether a proxy for the rules engine will be used.</span></span> <span data-ttu-id="8e3da-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8e3da-111">Read/write.</span></span> <span data-ttu-id="8e3da-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="8e3da-112">**VgTriState**.</span></span>

<span data-ttu-id="8e3da-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="8e3da-113">**Applies To**</span></span>

[<span data-ttu-id="8e3da-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="8e3da-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="8e3da-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="8e3da-115">**Tag Syntax**</span></span>

<span data-ttu-id="8e3da-116"><v : *Element* ruleproxy = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="8e3da-116"><v: *element* ruleproxy=" *expression* "></span></span>

<span data-ttu-id="8e3da-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="8e3da-117">**Remarks**</span></span>

<span data-ttu-id="8e3da-118">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="8e3da-118">The default value is **False**.</span></span> <span data-ttu-id="8e3da-119">Si la **valeur est true**, un proxy est utilisé.</span><span class="sxs-lookup"><span data-stu-id="8e3da-119">If **True**, a proxy is used.</span></span>

<span data-ttu-id="8e3da-120">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="8e3da-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="8e3da-121">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="8e3da-121">**Example**</span></span>

<span data-ttu-id="8e3da-122">Un proxy est utilisé pour traiter la forme.</span><span class="sxs-lookup"><span data-stu-id="8e3da-122">A proxy is used to process the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" ruleproxy="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 