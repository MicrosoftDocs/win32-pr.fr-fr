---
title: Attribut angle (remplissage) (VML)
description: Attribut angle (remplissage) (VML)
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4167c52d82fabc5804143966b13f9d24ff7b39d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031768"
---
# <a name="angle-attribute-fillvml"></a><span data-ttu-id="8bd8b-103">Attribut angle (remplissage) (VML)</span><span class="sxs-lookup"><span data-stu-id="8bd8b-103">Angle Attribute (Fill)(VML)</span></span>

<span data-ttu-id="8bd8b-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8bd8b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8bd8b-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="8bd8b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8bd8b-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="8bd8b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8bd8b-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="8bd8b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8bd8b-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8bd8b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8bd8b-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8bd8b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8bd8b-110">Définit l’angle d’un dégradé.</span><span class="sxs-lookup"><span data-stu-id="8bd8b-110">Defines the angle of a gradient fill.</span></span> <span data-ttu-id="8bd8b-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8bd8b-111">Read/write.</span></span> <span data-ttu-id="8bd8b-112">[VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="8bd8b-112">[VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="8bd8b-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="8bd8b-113">**Applies To**</span></span>

[<span data-ttu-id="8bd8b-114">Complète</span><span class="sxs-lookup"><span data-stu-id="8bd8b-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="8bd8b-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="8bd8b-115">**Tag Syntax**</span></span>

<span data-ttu-id="8bd8b-116"><v : angle d' *élément* = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="8bd8b-116"><v: *element* angle=" *expression* "></span></span>

<span data-ttu-id="8bd8b-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="8bd8b-117">**Script Syntax**</span></span>

<span data-ttu-id="8bd8b-118">*Element* . angle = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="8bd8b-118">*element* .angle="*expression*"</span></span>

<span data-ttu-id="8bd8b-119">*expression* = *Element*. angle</span><span class="sxs-lookup"><span data-stu-id="8bd8b-119">*expression*=*element*.angle</span></span>

<span data-ttu-id="8bd8b-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="8bd8b-120">**Remarks**</span></span>

<span data-ttu-id="8bd8b-121">Le vecteur d’un dégradé est perpendiculaire au vecteur du sens de fusion d’une couleur à l’autre.</span><span class="sxs-lookup"><span data-stu-id="8bd8b-121">The vector of a gradient is perpendicular to the vector of the blend direction from one color to another.</span></span> <span data-ttu-id="8bd8b-122">La valeur par défaut est 0 (zéro) degrés, qui est un vecteur horizontal de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="8bd8b-122">The default value is 0 (zero) degrees, which is a horizontal vector from left to right.</span></span> <span data-ttu-id="8bd8b-123">Les angles positifs font pivoter le dégradé dans un sens dans le sens inverse des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="8bd8b-123">Positive angles rotate the gradient in a counter-clockwise direction.</span></span>

<span data-ttu-id="8bd8b-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="8bd8b-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="8bd8b-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="8bd8b-125">**Example**</span></span>

<span data-ttu-id="8bd8b-126">Le remplissage de la forme est composé d’un dégradé de deux couleurs, en allant du bleu au rouge à un angle de 45 degrés.</span><span class="sxs-lookup"><span data-stu-id="8bd8b-126">The fill of the shape is composed of a gradient of two colors, running from blue to red at an angle of 45 degrees.</span></span> <span data-ttu-id="8bd8b-127">Le rouge se trouve dans le coin supérieur gauche et le bleu dans le coin inférieur droit.</span><span class="sxs-lookup"><span data-stu-id="8bd8b-127">Red will be in the top left corner and blue will be in the bottom right corner.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="blue" color2="red" angle="45"/>
   </v:shape>
```



 

 