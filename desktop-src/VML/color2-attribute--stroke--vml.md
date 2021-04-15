---
title: Color2, attribut (Stroke) (VML)
description: Color2, attribut (Stroke) (VML)
ms.assetid: 60b8035e-9477-4f8b-817b-dd6c41bdfa79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d577843b7d65de4f6197beabc877c308cf00154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463467"
---
# <a name="color2-attribute-strokevml"></a><span data-ttu-id="4512d-103">Color2, attribut (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="4512d-103">Color2 Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="4512d-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4512d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4512d-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4512d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4512d-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="4512d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4512d-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="4512d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4512d-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4512d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4512d-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4512d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4512d-110">Définit une deuxième couleur pour les traits.</span><span class="sxs-lookup"><span data-stu-id="4512d-110">Defines a second color for strokes.</span></span> <span data-ttu-id="4512d-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4512d-111">Read/write.</span></span> <span data-ttu-id="4512d-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="4512d-112">**String**.</span></span>

<span data-ttu-id="4512d-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="4512d-113">**Applies To**</span></span>

[<span data-ttu-id="4512d-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="4512d-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="4512d-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="4512d-115">**Tag Syntax**</span></span>

<span data-ttu-id="4512d-116"><v : *élément* color2 = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="4512d-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="4512d-117">Syntaxe du script</span><span class="sxs-lookup"><span data-stu-id="4512d-117">Script Syntax</span></span>

<span data-ttu-id="4512d-118">*Element* . color2 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="4512d-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="4512d-119">*expression* = *élément*. color2</span><span class="sxs-lookup"><span data-stu-id="4512d-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="4512d-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="4512d-120">**Remarks**</span></span>

<span data-ttu-id="4512d-121">Une deuxième couleur est utilisée lorsque le type de remplissage d’un trait est un modèle.</span><span class="sxs-lookup"><span data-stu-id="4512d-121">A second color is used when a stroke's fill type is a pattern.</span></span>

<span data-ttu-id="4512d-122">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="4512d-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="4512d-123">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="4512d-123">**Example**</span></span>

<span data-ttu-id="4512d-124">Le trait de la forme est un motif de remplissage dans lequel le remplissage est défini par l’image source, mais l’arrière-plan transparent est défini par la deuxième couleur.</span><span class="sxs-lookup"><span data-stu-id="4512d-124">The shape's stroke is a pattern fill where the fill is defined by the source image but the transparent background is defined by the second color.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke filltype="pattern" width="5pt" src="cylinder.gif" color2="green"/>
   </v:shape>
```



 

 