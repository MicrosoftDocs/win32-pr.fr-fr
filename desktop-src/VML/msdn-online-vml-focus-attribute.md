---
title: Attribut Focus VML
description: Attribut Focus VML
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062b2900c2f980c9a1433e5e790a34d463def9be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031835"
---
# <a name="vml-focus-attribute"></a><span data-ttu-id="9a0d0-103">Attribut Focus VML</span><span class="sxs-lookup"><span data-stu-id="9a0d0-103">VML Focus Attribute</span></span>

<span data-ttu-id="9a0d0-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9a0d0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9a0d0-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9a0d0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9a0d0-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="9a0d0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9a0d0-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="9a0d0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9a0d0-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9a0d0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9a0d0-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9a0d0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9a0d0-110">Définit le centre d’un remplissage dégradé linéaire.</span><span class="sxs-lookup"><span data-stu-id="9a0d0-110">Defines the center of a linear gradient fill.</span></span> <span data-ttu-id="9a0d0-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9a0d0-111">Read/write.</span></span> <span data-ttu-id="9a0d0-112">**VgFraction**.</span><span class="sxs-lookup"><span data-stu-id="9a0d0-112">**VgFraction**.</span></span>

<span data-ttu-id="9a0d0-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="9a0d0-113">**Applies To**</span></span>

[<span data-ttu-id="9a0d0-114">Complète</span><span class="sxs-lookup"><span data-stu-id="9a0d0-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="9a0d0-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="9a0d0-115">**Tag Syntax**</span></span>

<span data-ttu-id="9a0d0-116"><v : Focus sur l' *élément* = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="9a0d0-116"><v: *element* focus=" *expression* "></span></span>

<span data-ttu-id="9a0d0-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="9a0d0-117">**Script Syntax**</span></span>

<span data-ttu-id="9a0d0-118">*Element* . Focus = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="9a0d0-118">*element* .focus="*expression*"</span></span>

<span data-ttu-id="9a0d0-119">*expression* = *élément*. Focus</span><span class="sxs-lookup"><span data-stu-id="9a0d0-119">*expression*=*element*.focus</span></span>

<span data-ttu-id="9a0d0-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="9a0d0-120">**Remarks**</span></span>

<span data-ttu-id="9a0d0-121">Définit la position de départ du centre de la fusion.</span><span class="sxs-lookup"><span data-stu-id="9a0d0-121">Defines the center starting position of the blend.</span></span> <span data-ttu-id="9a0d0-122">Les valeurs sont comprises entre 100% et-100%.</span><span class="sxs-lookup"><span data-stu-id="9a0d0-122">Values range from 100% to -100%.</span></span> <span data-ttu-id="9a0d0-123">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="9a0d0-123">The default value is 0.</span></span> <span data-ttu-id="9a0d0-124">Une valeur de 100% (ou-100%) déplace le focus de manière à ce que la direction du lissage soit inversée (en effet, inversement **couleur** et **Color2**).</span><span class="sxs-lookup"><span data-stu-id="9a0d0-124">A value of 100% (or -100%) will shift the focus so that the direction of the blend will reverse (in effect reversing **Color** and **Color2**).</span></span> <span data-ttu-id="9a0d0-125">Une valeur de 50% change la fusion afin que la **couleur** soit aux deux extrémités et que la couleur **Color2** soit au milieu.</span><span class="sxs-lookup"><span data-stu-id="9a0d0-125">A value of 50% will change the blend so that **Color** is at both ends and **Color2** is in the middle.</span></span> <span data-ttu-id="9a0d0-126">La valeur-50% change la fusion afin que **Color2** soit aux deux extrémités et que la **couleur** soit au milieu.</span><span class="sxs-lookup"><span data-stu-id="9a0d0-126">A value of -50% will change the blend so that **Color2** is at both ends and **Color** is in the middle.</span></span>

<span data-ttu-id="9a0d0-127">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="9a0d0-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="9a0d0-128">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="9a0d0-128">**Example**</span></span>

<span data-ttu-id="9a0d0-129">Le focus dégradé du remplissage est décalé de sorte que le rouge (**couleur**) soit une bande au centre de la forme et que le haut et le bas soient bleus (**Color2**).</span><span class="sxs-lookup"><span data-stu-id="9a0d0-129">The gradient focus of the fill is shifted so that red (**Color**) will be a band in the center of the shape and that the top and bottom will be blue (**Color2**).</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 