---
title: Attribut Matrix (Shadow) (VML)
description: Attribut Matrix (Shadow) (VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d599aa817e87481aefdec43dbe345b7235fc54bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382676"
---
# <a name="matrix-attribute-shadowvml"></a><span data-ttu-id="b917d-103">Attribut Matrix (Shadow) (VML)</span><span class="sxs-lookup"><span data-stu-id="b917d-103">Matrix Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="b917d-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b917d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b917d-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b917d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b917d-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="b917d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b917d-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="b917d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b917d-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b917d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b917d-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b917d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b917d-110">Définit une transformation de perspective pour une ombre.</span><span class="sxs-lookup"><span data-stu-id="b917d-110">Defines a perspective transform for a shadow.</span></span> <span data-ttu-id="b917d-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b917d-111">Read/write.</span></span> <span data-ttu-id="b917d-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="b917d-112">**String**.</span></span>

<span data-ttu-id="b917d-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b917d-113">**Applies To**</span></span>

[<span data-ttu-id="b917d-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="b917d-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="b917d-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="b917d-115">**Tag Syntax**</span></span>

<span data-ttu-id="b917d-116"><v : *Element* Matrix = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b917d-116"><v: *element* matrix=" *expression* "></span></span>

<span data-ttu-id="b917d-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="b917d-117">**Script Syntax**</span></span>

<span data-ttu-id="b917d-118">*Element* . Matrix = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b917d-118">*element* .matrix="*expression*"</span></span>

<span data-ttu-id="b917d-119">*expression* = *élément*. Matrix</span><span class="sxs-lookup"><span data-stu-id="b917d-119">*expression*=*element*.matrix</span></span>

<span data-ttu-id="b917d-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="b917d-120">**Remarks**</span></span>

<span data-ttu-id="b917d-121">Matrice de transformation de perspective sous la forme « Sxx, SXY, syx, SYY, PX, py » où s = Scale et p = perspective.</span><span class="sxs-lookup"><span data-stu-id="b917d-121">A perspective transform matrix in the form "sxx,sxy,syx,syy,px,py" where s= scale and p = perspective.</span></span> <span data-ttu-id="b917d-122">Si le décalage est en unités absolues alors que PX, py est en unités de 1/UME ; Sinon, il s’agit d’une fraction inverse de la taille de la forme.</span><span class="sxs-lookup"><span data-stu-id="b917d-122">If offset is in absolute units then px, py are in 1/emu units; otherwise they are an inverse fraction of the shape size.</span></span>

<span data-ttu-id="b917d-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="b917d-123">*VML Standard Attribute*</span></span>

 

 