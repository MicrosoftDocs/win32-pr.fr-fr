---
title: Attribut VML de VML
description: Attribut VML de VML
ms.assetid: 1e2bd8e8-3d56-435d-bfaf-fb07f6b6fba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21604fb341840847690e9e086386d46f7124908a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463194"
---
# <a name="vml-cropright-attribute"></a><span data-ttu-id="76eba-103">Attribut VML de VML</span><span class="sxs-lookup"><span data-stu-id="76eba-103">VML CropRight Attribute</span></span>

<span data-ttu-id="76eba-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="76eba-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="76eba-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="76eba-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="76eba-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="76eba-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="76eba-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="76eba-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="76eba-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="76eba-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="76eba-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="76eba-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="76eba-110">Définit le pourcentage de suppression d’image du côté droit.</span><span class="sxs-lookup"><span data-stu-id="76eba-110">Defines the percentage of picture removal from the right side.</span></span> <span data-ttu-id="76eba-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="76eba-111">Read/write.</span></span> <span data-ttu-id="76eba-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="76eba-112">**VgNumber**.</span></span>

<span data-ttu-id="76eba-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="76eba-113">**Applies To**</span></span>

[<span data-ttu-id="76eba-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="76eba-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="76eba-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="76eba-115">**Tag Syntax**</span></span>

<span data-ttu-id="76eba-116"><v : *Element* CropRight = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="76eba-116"><v: *element* cropright=" *expression* "></span></span>

<span data-ttu-id="76eba-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="76eba-117">**Script Syntax**</span></span>

<span data-ttu-id="76eba-118">*Element* . CropRight = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="76eba-118">*element* .cropright="*expression*"</span></span>

<span data-ttu-id="76eba-119">*expression* = *Element*. CropRight</span><span class="sxs-lookup"><span data-stu-id="76eba-119">*expression*=*element*.cropright</span></span>

<span data-ttu-id="76eba-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="76eba-120">**Remarks**</span></span>

<span data-ttu-id="76eba-121">La quantité de rognage peut être comprise entre-1,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="76eba-121">The amount of cropping can range from -1.0 to 1.0.</span></span> <span data-ttu-id="76eba-122">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="76eba-122">The default value is 0.</span></span> <span data-ttu-id="76eba-123">Notez que la valeur 1 n’affiche aucune image.</span><span class="sxs-lookup"><span data-stu-id="76eba-123">Note that a value of 1 will display no picture at all.</span></span> <span data-ttu-id="76eba-124">Les valeurs négatives entraînent le redimensionnement de l’image à partir du bord en cours de rognage (l’espace vide entre l’image et le bord rogné est rempli par la couleur de remplissage de la forme).</span><span class="sxs-lookup"><span data-stu-id="76eba-124">Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape).</span></span> <span data-ttu-id="76eba-125">Les valeurs positives inférieures à 1 entraînent l’étirement de l’image restante pour l’adapter à la forme.</span><span class="sxs-lookup"><span data-stu-id="76eba-125">Positive values less than 1 will result in the remaining picture being stretched to fit the shape.</span></span>

<span data-ttu-id="76eba-126">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="76eba-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="76eba-127">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="76eba-127">**Example**</span></span>

<span data-ttu-id="76eba-128">L’image est retirée du côté droit de 20% de la largeur.</span><span class="sxs-lookup"><span data-stu-id="76eba-128">The picture will be squeezed from the right side by 20% of the width.</span></span> <span data-ttu-id="76eba-129">L’espace vide entre l’image et le bord droit est rempli par la couleur de remplissage de la forme.</span><span class="sxs-lookup"><span data-stu-id="76eba-129">The empty space between the picture and the right edge will be filled by the fill color of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="blue"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropright="-.2" src="kids.jpg"/>
   </v:shape>
```





 

 