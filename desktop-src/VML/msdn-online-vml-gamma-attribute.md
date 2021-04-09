---
title: Attribut gamma VML
description: Attribut gamma VML
ms.assetid: 47a4d10e-f5ef-457b-92dd-bce5dae59b1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b74c80739d694038601588eee4c8ad7ed90923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101976"
---
# <a name="vml-gamma-attribute"></a><span data-ttu-id="46ee8-103">Attribut gamma VML</span><span class="sxs-lookup"><span data-stu-id="46ee8-103">VML Gamma Attribute</span></span>

<span data-ttu-id="46ee8-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="46ee8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="46ee8-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="46ee8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="46ee8-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="46ee8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="46ee8-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="46ee8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="46ee8-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="46ee8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="46ee8-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="46ee8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="46ee8-110">Définit la quantité de contraste pour une image.</span><span class="sxs-lookup"><span data-stu-id="46ee8-110">Defines the amount of contrast for an image.</span></span> <span data-ttu-id="46ee8-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="46ee8-111">Read/write.</span></span> <span data-ttu-id="46ee8-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="46ee8-112">**VgNumber**.</span></span>

<span data-ttu-id="46ee8-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="46ee8-113">**Applies To**</span></span>

[<span data-ttu-id="46ee8-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="46ee8-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="46ee8-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="46ee8-115">**Tag Syntax**</span></span>

<span data-ttu-id="46ee8-116"><v : *Element* gamma = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="46ee8-116"><v: *element* gamma=" *expression* "></span></span>

<span data-ttu-id="46ee8-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="46ee8-117">**Script Syntax**</span></span>

<span data-ttu-id="46ee8-118">*Element* . gamma = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="46ee8-118">*element* .gamma="*expression*"</span></span>

<span data-ttu-id="46ee8-119">*expression* = . gamma ( *élément*)</span><span class="sxs-lookup"><span data-stu-id="46ee8-119">*expression*=*element*.gamma</span></span>

<span data-ttu-id="46ee8-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="46ee8-120">**Remarks**</span></span>

<span data-ttu-id="46ee8-121">La diminution de la valeur gamma inférieure à 1 modifie une image pour la rendre plus contrastée, tandis que les valeurs supérieures à 1 diminuent le contraste.</span><span class="sxs-lookup"><span data-stu-id="46ee8-121">Decreasing the gamma below 1 modifies an image to make it more contrasty, while values greater than 1 decrease the contrast.</span></span> <span data-ttu-id="46ee8-122">Les valeurs utiles sont comprises entre 0,3 et environ 3.</span><span class="sxs-lookup"><span data-stu-id="46ee8-122">Useful values are from 0.3 to about 3.</span></span> <span data-ttu-id="46ee8-123">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="46ee8-123">The default value is 0.</span></span>

<span data-ttu-id="46ee8-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="46ee8-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="46ee8-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="46ee8-125">**Example**</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gamma=".7" src="gamera.jpg"/>
   </v:shape>
```



 

 