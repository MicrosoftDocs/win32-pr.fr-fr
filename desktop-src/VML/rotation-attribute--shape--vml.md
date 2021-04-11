---
title: Attribut rotation (Shape) (VML)
description: Attribut rotation (Shape) (VML)
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03b114c885cbeaf5392068e79cd7f63bbc1fc52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031806"
---
# <a name="rotation-attribute-shapevml"></a><span data-ttu-id="74e5a-103">Attribut rotation (Shape) (VML)</span><span class="sxs-lookup"><span data-stu-id="74e5a-103">Rotation Attribute (Shape)(VML)</span></span>

<span data-ttu-id="74e5a-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="74e5a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="74e5a-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="74e5a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="74e5a-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="74e5a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="74e5a-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="74e5a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="74e5a-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="74e5a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="74e5a-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="74e5a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="74e5a-110">Définit l’angle de rotation d’une forme.</span><span class="sxs-lookup"><span data-stu-id="74e5a-110">Defines the angle that a shape is rotated.</span></span> <span data-ttu-id="74e5a-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="74e5a-111">Read/write.</span></span> <span data-ttu-id="74e5a-112">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="74e5a-112">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span>

<span data-ttu-id="74e5a-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="74e5a-113">**Applies To**</span></span>

[<span data-ttu-id="74e5a-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="74e5a-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="74e5a-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="74e5a-115">**Tag Syntax**</span></span>

<span data-ttu-id="74e5a-116"><v : *Element* style = "rotation : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="74e5a-116"><v: *element* style="rotation: *expression* "></span></span>

<span data-ttu-id="74e5a-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="74e5a-117">**Script Syntax**</span></span>

<span data-ttu-id="74e5a-118">*Element* . rotation = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="74e5a-118">*element* .rotation="*expression*"</span></span>

<span data-ttu-id="74e5a-119">*expression* = *Element*. rotation</span><span class="sxs-lookup"><span data-stu-id="74e5a-119">*expression*=*element*.rotation</span></span>

<span data-ttu-id="74e5a-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="74e5a-120">**Remarks**</span></span>

<span data-ttu-id="74e5a-121">La valeur en degrés peut être positive ou négative, et les valeurs supérieures à 360 sont modulées sur un cercle de 360 degrés.</span><span class="sxs-lookup"><span data-stu-id="74e5a-121">The value in degrees can be positive or negative, and values greater than 360 are modularized to a 360-degree circle.</span></span> <span data-ttu-id="74e5a-122">Les angles positifs sont dans le sens horaire.</span><span class="sxs-lookup"><span data-stu-id="74e5a-122">Positive angles are clockwise.</span></span> <span data-ttu-id="74e5a-123">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="74e5a-123">The default value is 0.</span></span>

<span data-ttu-id="74e5a-124">Notez que la forme est repositionnée après la rotation pour refléter les nouvelles coordonnées du rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="74e5a-124">Note that the shape is repositioned after the rotation to reflect the new bounding box coordinates.</span></span>

<span data-ttu-id="74e5a-125">Notez également que pour les scripts, l’attribut de **style** n’est pas utilisé et que la **rotation** est traitée comme un attribut direct de la forme.</span><span class="sxs-lookup"><span data-stu-id="74e5a-125">Also note that for scripting, the **style** attribute is not used and that **Rotation** is treated as a direct attribute of the shape.</span></span>

<span data-ttu-id="74e5a-126">L’attribut **rotation** est semblable à l’attribut de **rotation** HTML standard pour les styles.</span><span class="sxs-lookup"><span data-stu-id="74e5a-126">The **Rotation** attribute is similar to the standard HTML **Rotation** attribute for styles.</span></span>

<span data-ttu-id="74e5a-127">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="74e5a-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="74e5a-128">**Voir aussi**</span><span class="sxs-lookup"><span data-stu-id="74e5a-128">**See Also**</span></span>

<span data-ttu-id="74e5a-129">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="74e5a-129">**Example**</span></span>

<span data-ttu-id="74e5a-130">Le rectangle sera incliné 45 degrés.</span><span class="sxs-lookup"><span data-stu-id="74e5a-130">The rectangle will be tilted 45 degrees.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



<span data-ttu-id="74e5a-131">[Exemple d’attribut de rotation](/previous-versions/bb264091(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="74e5a-131">[Rotation Attribute Example](/previous-versions/bb264091(v=vs.85)).</span></span> <span data-ttu-id="74e5a-132">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="74e5a-132">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 