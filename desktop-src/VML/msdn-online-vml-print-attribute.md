---
title: Attribut d’impression VML
description: Attribut d’impression VML
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55925621ab56f011c998f3feac21a892a4d7ea66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509035"
---
# <a name="vml-print-attribute"></a><span data-ttu-id="2f789-103">Attribut d’impression VML</span><span class="sxs-lookup"><span data-stu-id="2f789-103">VML Print Attribute</span></span>

<span data-ttu-id="2f789-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2f789-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2f789-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="2f789-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2f789-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="2f789-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2f789-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="2f789-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2f789-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2f789-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2f789-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2f789-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2f789-110">Détermine si la forme sera imprimée.</span><span class="sxs-lookup"><span data-stu-id="2f789-110">Determines whether the shape will be printed.</span></span> <span data-ttu-id="2f789-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2f789-111">Read/write.</span></span> <span data-ttu-id="2f789-112">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2f789-112">[VgTriState](msdn-online-vml-vgtristate.md).</span></span>

<span data-ttu-id="2f789-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="2f789-113">**Applies To**</span></span>

[<span data-ttu-id="2f789-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="2f789-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="2f789-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="2f789-115">**Tag Syntax**</span></span>

<span data-ttu-id="2f789-116"><v : *élément* Print = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="2f789-116"><v: *element* print=" *expression* "></span></span>

<span data-ttu-id="2f789-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="2f789-117">**Script Syntax**</span></span>

<span data-ttu-id="2f789-118">*Element* . Print = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="2f789-118">*element* .print="*expression*"</span></span>

<span data-ttu-id="2f789-119">*expression* = *élément*. Print</span><span class="sxs-lookup"><span data-stu-id="2f789-119">*expression*=*element*.print</span></span>

<span data-ttu-id="2f789-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="2f789-120">**Remarks**</span></span>

<span data-ttu-id="2f789-121">Fourni comme moyen de spécifier si les formes seront imprimées.</span><span class="sxs-lookup"><span data-stu-id="2f789-121">Provided as a way to specify whether shapes will be printed.</span></span> <span data-ttu-id="2f789-122">Notez qu’une forme peut toujours être affichée sur l’écran, même si elle n’est pas imprimée suite à l’affichage de cet attribut avec la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="2f789-122">Note that a shape can still be displayed on the screen, even if it is not printed as a result of this attribute being **False**.</span></span> <span data-ttu-id="2f789-123">La valeur par défaut est **True**.</span><span class="sxs-lookup"><span data-stu-id="2f789-123">The default value is **True**.</span></span>

<span data-ttu-id="2f789-124">Cet attribut est utilisé par Microsoft Office mais n’est pas utilisé par Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2f789-124">This attribute is used by Microsoft Office but is not used by Microsoft Internet Explorer.</span></span>

<span data-ttu-id="2f789-125">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="2f789-125">*Microsoft Office Extensions Attribute*</span></span>

 

 