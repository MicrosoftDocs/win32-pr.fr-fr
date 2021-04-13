---
title: Attribut métallique VML
description: Attribut métallique VML
ms.assetid: 4d2efaed-d391-494f-9f0c-d57ad019f71d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d318724f0a8f3c5fbce1ee9045ed5d6e0d49686
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104381995"
---
# <a name="vml-metal-attribute"></a><span data-ttu-id="f53cb-103">Attribut métallique VML</span><span class="sxs-lookup"><span data-stu-id="f53cb-103">VML Metal Attribute</span></span>

<span data-ttu-id="f53cb-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f53cb-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f53cb-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f53cb-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f53cb-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="f53cb-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f53cb-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="f53cb-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f53cb-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f53cb-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f53cb-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f53cb-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f53cb-110">Détermine si la surface de la forme extrudée est semblable à Metal.</span><span class="sxs-lookup"><span data-stu-id="f53cb-110">Determines whether the surface of the extruded shape will resemble metal.</span></span> <span data-ttu-id="f53cb-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f53cb-111">Read/write.</span></span> <span data-ttu-id="f53cb-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="f53cb-112">**VgTriState**.</span></span>

<span data-ttu-id="f53cb-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="f53cb-113">**Applies To**</span></span>

[<span data-ttu-id="f53cb-114">Extrusion</span><span class="sxs-lookup"><span data-stu-id="f53cb-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="f53cb-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="f53cb-115">**Tag Syntax**</span></span>

<span data-ttu-id="f53cb-116"><o : *élément* Metal = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="f53cb-116"><o: *element* metal=" *expression* "></span></span>

<span data-ttu-id="f53cb-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="f53cb-117">**Script Syntax**</span></span>

<span data-ttu-id="f53cb-118">*Element* . Metal = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="f53cb-118">*element* .metal="*expression*"</span></span>

<span data-ttu-id="f53cb-119">*expression* = *élément*. Metal</span><span class="sxs-lookup"><span data-stu-id="f53cb-119">*expression*=*element*.metal</span></span>

<span data-ttu-id="f53cb-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="f53cb-120">**Remarks**</span></span>

<span data-ttu-id="f53cb-121">Si la valeur est **true**, cet attribut fait que le modèle éclairé réfléchi est la couleur matérielle au lieu de la couleur de la source de lumière, ce qui rend l’objet plus métallique. Pour rapprocher davantage un matériel métallique, specularity doit être relativement élevé (environ 1,2) et la diffusion est relativement faible (environ 0,6).</span><span class="sxs-lookup"><span data-stu-id="f53cb-121">If set to **True**, this attribute causes the specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.To further approximate a metallic material requires that specularity be relatively high (about 1.2) and diffusity be relatively low (about 0.6).</span></span> <span data-ttu-id="f53cb-122">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="f53cb-122">The default value is **False**.</span></span>

<span data-ttu-id="f53cb-123">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="f53cb-123">*Microsoft Office Extensions Attribute*</span></span>

 

 