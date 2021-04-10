---
title: Attribut de matrice (skew) (VML)
description: Attribut de matrice (skew) (VML)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8327acfebfe4d968e673060f2f3cbef69d3e9db6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031764"
---
# <a name="matrix-attribute-skewvml"></a><span data-ttu-id="8f4d9-103">Attribut de matrice (skew) (VML)</span><span class="sxs-lookup"><span data-stu-id="8f4d9-103">Matrix Attribute (Skew)(VML)</span></span>

<span data-ttu-id="8f4d9-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8f4d9-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8f4d9-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8f4d9-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8f4d9-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8f4d9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8f4d9-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8f4d9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8f4d9-110">Définit une transformation de perspective d’un skew.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-110">Defines a perspective transform of a skew.</span></span> <span data-ttu-id="8f4d9-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-111">Read/write.</span></span> <span data-ttu-id="8f4d9-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-112">**String**.</span></span>

<span data-ttu-id="8f4d9-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="8f4d9-113">**Applies To**</span></span>

[<span data-ttu-id="8f4d9-114">Appliquez</span><span class="sxs-lookup"><span data-stu-id="8f4d9-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="8f4d9-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="8f4d9-115">**Tag Syntax**</span></span>

<span data-ttu-id="8f4d9-116"><o : *Element* Matrix = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="8f4d9-116"><o: *element* matrix=" *expression* "></span></span>

<span data-ttu-id="8f4d9-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="8f4d9-117">**Script Syntax**</span></span>

<span data-ttu-id="8f4d9-118">*Element* . Matrix = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="8f4d9-118">*element* .matrix="*expression*"</span></span>

<span data-ttu-id="8f4d9-119">*expression* = *élément*. Matrix</span><span class="sxs-lookup"><span data-stu-id="8f4d9-119">*expression*=*element*.matrix</span></span>

<span data-ttu-id="8f4d9-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="8f4d9-120">**Remarks**</span></span>

<span data-ttu-id="8f4d9-121">La matrice est une chaîne au format « Sxx, SXY, syx, SYY, PX, py » où s est Scale, p est perspective et x et y sont des valeurs x et y.</span><span class="sxs-lookup"><span data-stu-id="8f4d9-121">The matrix is a string in the form "sxx, sxy, syx, syy, px, py" where s is scale, p is perspective, and x and y are x and y values.</span></span> <span data-ttu-id="8f4d9-122">Si le [décalage](offset-attribute--skew--vml.md) est en unités absolues, PX et PY sont en unités UME ^ [-1 (](msdn-online-vml-units.md) sinon, elles sont une fraction inverse de la taille de la forme).</span><span class="sxs-lookup"><span data-stu-id="8f4d9-122">If [Offset](offset-attribute--skew--vml.md) is in absolute units, then px and py are in emu^-1 [units](msdn-online-vml-units.md) (otherwise they are an inverse fraction of the shape size).</span></span> <span data-ttu-id="8f4d9-123">La valeur par défaut est « 1, 0, 0, 1, 0, 0 ».</span><span class="sxs-lookup"><span data-stu-id="8f4d9-123">The default value is "1,0,0,1,0,0".</span></span>

<span data-ttu-id="8f4d9-124">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="8f4d9-124">*Microsoft Office Extensions Attribute*</span></span>

 

 