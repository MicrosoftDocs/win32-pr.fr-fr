---
title: Attribut CropTop de VML
description: Attribut CropTop de VML
ms.assetid: b54939b6-0505-43b0-bf82-c3df82dc2633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8b2606c7ac5835caeecc145a885de48eaeaf8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315318"
---
# <a name="vml-croptop-attribute"></a><span data-ttu-id="c9b94-103">Attribut CropTop de VML</span><span class="sxs-lookup"><span data-stu-id="c9b94-103">VML CropTop Attribute</span></span>

<span data-ttu-id="c9b94-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c9b94-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c9b94-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c9b94-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c9b94-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="c9b94-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c9b94-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="c9b94-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c9b94-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c9b94-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c9b94-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c9b94-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c9b94-110">Définit le pourcentage de suppression d’image du côté supérieur.</span><span class="sxs-lookup"><span data-stu-id="c9b94-110">Defines the percentage of picture removal from the top side.</span></span> <span data-ttu-id="c9b94-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c9b94-111">Read/write.</span></span> <span data-ttu-id="c9b94-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="c9b94-112">**VgNumber**.</span></span>

<span data-ttu-id="c9b94-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c9b94-113">**Applies To**</span></span>

[<span data-ttu-id="c9b94-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="c9b94-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="c9b94-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="c9b94-115">**Tag Syntax**</span></span>

<span data-ttu-id="c9b94-116"><v : *Element* CropTop = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c9b94-116"><v: *element* croptop=" *expression* "></span></span>

<span data-ttu-id="c9b94-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="c9b94-117">**Script Syntax**</span></span>

<span data-ttu-id="c9b94-118">*Element* . CropTop = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="c9b94-118">*element* .croptop="*expression*"</span></span>

<span data-ttu-id="c9b94-119">*expression* = . CropTop, *élément*</span><span class="sxs-lookup"><span data-stu-id="c9b94-119">*expression*=*element*.croptop</span></span>

<span data-ttu-id="c9b94-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="c9b94-120">**Remarks**</span></span>

<span data-ttu-id="c9b94-121">La quantité de rognage peut être comprise entre-1,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="c9b94-121">The amount of cropping can range from -1.0 to 1.0.</span></span> <span data-ttu-id="c9b94-122">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="c9b94-122">The default value is 0.</span></span> <span data-ttu-id="c9b94-123">Notez que la valeur 1 n’affiche aucune image.</span><span class="sxs-lookup"><span data-stu-id="c9b94-123">Note that a value of 1 will display no picture at all.</span></span> <span data-ttu-id="c9b94-124">Les valeurs négatives entraînent le redimensionnement de l’image à partir du bord en cours de rognage (l’espace vide entre l’image et le bord rogné est rempli par la couleur de remplissage de la forme).</span><span class="sxs-lookup"><span data-stu-id="c9b94-124">Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape).</span></span> <span data-ttu-id="c9b94-125">Les valeurs positives inférieures à 1 entraînent l’étirement de l’image restante pour l’adapter à la forme.</span><span class="sxs-lookup"><span data-stu-id="c9b94-125">Positive values less than 1 will result in the remaining picture being stretched to fit the shape.</span></span>

<span data-ttu-id="c9b94-126">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="c9b94-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="c9b94-127">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="c9b94-127">**Example**</span></span>

<span data-ttu-id="c9b94-128">L’image sera insérée dans un éclat étroit au bas de la forme.</span><span class="sxs-lookup"><span data-stu-id="c9b94-128">The picture will be squeezed into a narrow sliver at the bottom of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata croptop="-.8" src="kids.jpg"/>
   </v:shape>
```





 

 