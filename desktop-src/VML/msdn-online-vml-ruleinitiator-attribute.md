---
title: RuleInitiator VML (attribut)
description: RuleInitiator VML (attribut)
ms.assetid: 2c9b1131-b088-4b70-b132-bdb4296433ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80201ad80fbb8dc5bbff2e8ed4e0b8db2863fdad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316356"
---
# <a name="vml-ruleinitiator-attribute"></a><span data-ttu-id="c2975-103">RuleInitiator VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="c2975-103">VML RuleInitiator Attribute</span></span>

<span data-ttu-id="c2975-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c2975-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c2975-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c2975-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c2975-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="c2975-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c2975-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="c2975-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c2975-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c2975-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c2975-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c2975-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c2975-110">Détermine si un moteur de règles sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="c2975-110">Determines whether a rules engine will be used.</span></span> <span data-ttu-id="c2975-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c2975-111">Read/write.</span></span> <span data-ttu-id="c2975-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="c2975-112">**VgTriState**.</span></span>

<span data-ttu-id="c2975-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c2975-113">**Applies To**</span></span>

[<span data-ttu-id="c2975-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="c2975-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="c2975-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="c2975-115">**Tag Syntax**</span></span>

<span data-ttu-id="c2975-116"><v : *Element* o :ruleinitiator = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c2975-116"><v: *element* o:ruleinitiator=" *expression* "></span></span>

<span data-ttu-id="c2975-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="c2975-117">**Remarks**</span></span>

<span data-ttu-id="c2975-118">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="c2975-118">The default value is **False**.</span></span> <span data-ttu-id="c2975-119">Si la valeur est **true**, un moteur de règles est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c2975-119">If the value is **True**, a rules engine is used.</span></span>

<span data-ttu-id="c2975-120">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="c2975-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="c2975-121">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="c2975-121">**Example**</span></span>

<span data-ttu-id="c2975-122">La forme est traitée par un moteur de règles.</span><span class="sxs-lookup"><span data-stu-id="c2975-122">The shape will be processed by a rules engine.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" rulesinitiator="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 