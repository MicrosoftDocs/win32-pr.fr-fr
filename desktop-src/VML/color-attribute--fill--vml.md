---
title: Color, attribut (Fill) (VML)
description: Color, attribut (Fill) (VML)
ms.assetid: 38e75bf5-4da9-4c58-af86-3554d03a6b7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8480b3a013add36533a82b31338fba301e8353db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463198"
---
# <a name="color-attribute-fillvml"></a><span data-ttu-id="c6f64-103">Color, attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="c6f64-103">Color Attribute (Fill)(VML)</span></span>

<span data-ttu-id="c6f64-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c6f64-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c6f64-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c6f64-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c6f64-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="c6f64-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c6f64-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="c6f64-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c6f64-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c6f64-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c6f64-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c6f64-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c6f64-110">Définit la couleur d’un remplissage.</span><span class="sxs-lookup"><span data-stu-id="c6f64-110">Defines the color of a fill.</span></span> <span data-ttu-id="c6f64-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c6f64-111">Read/write.</span></span> <span data-ttu-id="c6f64-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="c6f64-112">**VgColor**.</span></span>

<span data-ttu-id="c6f64-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c6f64-113">**Applies To**</span></span>

[<span data-ttu-id="c6f64-114">Complète</span><span class="sxs-lookup"><span data-stu-id="c6f64-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="c6f64-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="c6f64-115">**Tag Syntax**</span></span>

<span data-ttu-id="c6f64-116"><v : *Element* Color = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c6f64-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="c6f64-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="c6f64-117">**Script Syntax**</span></span>

<span data-ttu-id="c6f64-118">*Element* . Color = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="c6f64-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="c6f64-119">*expression* = *Element*. Color</span><span class="sxs-lookup"><span data-stu-id="c6f64-119">*expression*=*element*.color</span></span>

<span data-ttu-id="c6f64-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="c6f64-120">**Remarks**</span></span>

<span data-ttu-id="c6f64-121">Remplace l’attribut **FillColor** d’une forme.</span><span class="sxs-lookup"><span data-stu-id="c6f64-121">Overrides the **FillColor** attribute of a shape.</span></span> <span data-ttu-id="c6f64-122">La valeur par défaut est **blanc**.</span><span class="sxs-lookup"><span data-stu-id="c6f64-122">The default value is **White**.</span></span>

<span data-ttu-id="c6f64-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="c6f64-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="c6f64-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="c6f64-124">**Example**</span></span>

<span data-ttu-id="c6f64-125">La couleur de remplissage de la forme est verte.</span><span class="sxs-lookup"><span data-stu-id="c6f64-125">The fill color of the shape is green.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="green"/>
   </v:shape>
```



 

 