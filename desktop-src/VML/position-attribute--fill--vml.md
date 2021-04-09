---
title: Position, attribut (Fill) (VML)
description: Position, attribut (Fill) (VML)
ms.assetid: 0d532d4c-0c96-4f41-b54f-55b6aade0c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01fff487f134d50b5a72623abf21c0b5710f9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102269"
---
# <a name="position-attribute-fillvml"></a><span data-ttu-id="6cc0d-103">Position, attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="6cc0d-103">Position Attribute (Fill)(VML)</span></span>

<span data-ttu-id="6cc0d-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6cc0d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6cc0d-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6cc0d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6cc0d-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="6cc0d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6cc0d-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="6cc0d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6cc0d-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6cc0d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6cc0d-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6cc0d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6cc0d-110">Définit la position de l’image de remplissage.</span><span class="sxs-lookup"><span data-stu-id="6cc0d-110">Defines the position of fill image.</span></span> <span data-ttu-id="6cc0d-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6cc0d-111">Read/write.</span></span> <span data-ttu-id="6cc0d-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="6cc0d-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="6cc0d-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="6cc0d-113">**Applies To**</span></span>

[<span data-ttu-id="6cc0d-114">Complète</span><span class="sxs-lookup"><span data-stu-id="6cc0d-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="6cc0d-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="6cc0d-115">**Tag Syntax**</span></span>

<span data-ttu-id="6cc0d-116"><v : *Element* position = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="6cc0d-116"><v: *element* position=" *expression* "></span></span>

<span data-ttu-id="6cc0d-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="6cc0d-117">**Script Syntax**</span></span>

<span data-ttu-id="6cc0d-118">*Element* . position = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="6cc0d-118">*element* .position="*expression*"</span></span>

<span data-ttu-id="6cc0d-119">*expression* = *élément*. position</span><span class="sxs-lookup"><span data-stu-id="6cc0d-119">*expression*=*element*.position</span></span>

<span data-ttu-id="6cc0d-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="6cc0d-120">**Remarks**</span></span>

<span data-ttu-id="6cc0d-121">Spécifie un point dans la forme pour positionner l’origine de l’image.</span><span class="sxs-lookup"><span data-stu-id="6cc0d-121">Specifies a point in the shape to position the origin of the image.</span></span> <span data-ttu-id="6cc0d-122">La valeur par défaut est le centre du rectangle de conteneur.</span><span class="sxs-lookup"><span data-stu-id="6cc0d-122">Default is the center of the container rectangle.</span></span> <span data-ttu-id="6cc0d-123">Le vecteur est une fraction de la largeur et de la hauteur de l’image.</span><span class="sxs-lookup"><span data-stu-id="6cc0d-123">The vector is a fraction of the width and height of the image.</span></span>

<span data-ttu-id="6cc0d-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="6cc0d-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="6cc0d-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="6cc0d-125">**Example**</span></span>

<span data-ttu-id="6cc0d-126">L’image du remplissage est décalée vers la droite jusqu’au point 50% de la largeur de la forme.</span><span class="sxs-lookup"><span data-stu-id="6cc0d-126">The image of the fill is shifted right to a point 50% of the width of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" position="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 