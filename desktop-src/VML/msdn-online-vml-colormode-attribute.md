---
title: Attribut ColorMode de VML
description: Attribut ColorMode de VML
ms.assetid: 92c885ca-7912-42ff-8f07-e6e779e0ef05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7126a3f5a95910eb85007fe9a80d500c5233e5e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382172"
---
# <a name="vml-colormode-attribute"></a><span data-ttu-id="9fbe1-103">Attribut ColorMode de VML</span><span class="sxs-lookup"><span data-stu-id="9fbe1-103">VML ColorMode Attribute</span></span>

<span data-ttu-id="9fbe1-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9fbe1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9fbe1-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9fbe1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9fbe1-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="9fbe1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9fbe1-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="9fbe1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9fbe1-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9fbe1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9fbe1-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9fbe1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9fbe1-110">Détermine le mode de couleur de l’extrusion.</span><span class="sxs-lookup"><span data-stu-id="9fbe1-110">Determines the mode of extrusion color.</span></span> <span data-ttu-id="9fbe1-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9fbe1-111">Read/write.</span></span> <span data-ttu-id="9fbe1-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="9fbe1-112">**VgTriState**.</span></span>

<span data-ttu-id="9fbe1-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="9fbe1-113">**Applies To**</span></span>

[<span data-ttu-id="9fbe1-114">Extrusion</span><span class="sxs-lookup"><span data-stu-id="9fbe1-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="9fbe1-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="9fbe1-115">**Tag Syntax**</span></span>

<span data-ttu-id="9fbe1-116"><o : *Element* ColorMode = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="9fbe1-116"><o: *element* colormode=" *expression* "></span></span>

<span data-ttu-id="9fbe1-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="9fbe1-117">**Script Syntax**</span></span>

<span data-ttu-id="9fbe1-118">*Element* . ColorMode = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="9fbe1-118">*element* .colormode="*expression*"</span></span>

<span data-ttu-id="9fbe1-119">*expression* = *élément*. ColorMode</span><span class="sxs-lookup"><span data-stu-id="9fbe1-119">*expression*=*element*.colormode</span></span>

<span data-ttu-id="9fbe1-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="9fbe1-120">**Remarks**</span></span>

<span data-ttu-id="9fbe1-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="9fbe1-121">Values include:</span></span>



| <span data-ttu-id="9fbe1-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fbe1-122">Value</span></span>  | <span data-ttu-id="9fbe1-123">Description</span><span class="sxs-lookup"><span data-stu-id="9fbe1-123">Description</span></span>                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fbe1-124">auto</span><span class="sxs-lookup"><span data-stu-id="9fbe1-124">auto</span></span>   | <span data-ttu-id="9fbe1-125">Spécifie que la couleur de l’extrusion est identique à la couleur de remplissage de la forme.</span><span class="sxs-lookup"><span data-stu-id="9fbe1-125">Specifies that the color of the extrusion is the same as the fill color of the shape.</span></span> <span data-ttu-id="9fbe1-126">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="9fbe1-126">Default.</span></span>                |
| <span data-ttu-id="9fbe1-127">custom</span><span class="sxs-lookup"><span data-stu-id="9fbe1-127">custom</span></span> | <span data-ttu-id="9fbe1-128">Spécifie que l’extrusion sera la couleur de l’attribut [Color](color-attribute--extrusion--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="9fbe1-128">Specifies that the extrusion will be the color of the [Color](color-attribute--extrusion--vml.md) attribute.</span></span> |



 

<span data-ttu-id="9fbe1-129">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="9fbe1-129">*Microsoft Office Extensions Attribute*</span></span>

 

 