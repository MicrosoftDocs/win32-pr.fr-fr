---
title: Attribut de diffusion VML
description: Attribut de diffusion VML
ms.assetid: 1d131540-9166-47fc-bb0d-fada38f6a3de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a8e51750bcd71421609221812eb38bbf709657
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510685"
---
# <a name="vml-diffusity-attribute"></a><span data-ttu-id="69e3c-103">Attribut de diffusion VML</span><span class="sxs-lookup"><span data-stu-id="69e3c-103">VML Diffusity Attribute</span></span>

<span data-ttu-id="69e3c-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="69e3c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="69e3c-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="69e3c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="69e3c-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="69e3c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="69e3c-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="69e3c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="69e3c-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="69e3c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="69e3c-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="69e3c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="69e3c-110">Définit la quantité de diffusion de la lumière réfléchie à partir d’une forme extrudée.</span><span class="sxs-lookup"><span data-stu-id="69e3c-110">Defines the amount of diffusion of reflected light from an extruded shape.</span></span> <span data-ttu-id="69e3c-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="69e3c-111">Read/write.</span></span> <span data-ttu-id="69e3c-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="69e3c-112">**VgNumber**.</span></span>

<span data-ttu-id="69e3c-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="69e3c-113">**Applies To**</span></span>

[<span data-ttu-id="69e3c-114">Extrusion</span><span class="sxs-lookup"><span data-stu-id="69e3c-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="69e3c-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="69e3c-115">**Tag Syntax**</span></span>

<span data-ttu-id="69e3c-116"><o : diffusion d' *élément* = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="69e3c-116"><o: *element* diffusity=" *expression* "></span></span>

<span data-ttu-id="69e3c-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="69e3c-117">**Script Syntax**</span></span>

<span data-ttu-id="69e3c-118">*Element* . diffusion = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="69e3c-118">*element* .diffusity="*expression*"</span></span>

<span data-ttu-id="69e3c-119">*expression* = *élément*. diffusion</span><span class="sxs-lookup"><span data-stu-id="69e3c-119">*expression*=*element*.diffusity</span></span>

<span data-ttu-id="69e3c-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="69e3c-120">**Remarks**</span></span>

<span data-ttu-id="69e3c-121">Cette valeur définit le rapport entre l’incident et la lumière réfléchie.</span><span class="sxs-lookup"><span data-stu-id="69e3c-121">This value defines the ratio of incident light to diffused reflected light.</span></span> <span data-ttu-id="69e3c-122">Les valeurs normales sont comprises entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="69e3c-122">Normal values range from 0 to 1.</span></span> <span data-ttu-id="69e3c-123">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="69e3c-123">The default value is 0.</span></span>

<span data-ttu-id="69e3c-124">Si les valeurs supérieures à 1 sont spécifiées, des effets inhabituels peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="69e3c-124">If values greater than 1 are specified, unusual effects can result.</span></span>

<span data-ttu-id="69e3c-125">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="69e3c-125">*Microsoft Office Extensions Attribute*</span></span>

 

 