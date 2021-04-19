---
title: Color, attribut (Shadow) (VML)
description: Color, attribut (Shadow) (VML)
ms.assetid: 677615b7-b4a4-411f-b04e-3ed0399f4c05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73df77e65a3ae0f74c6e79b9c179c31da27698f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511078"
---
# <a name="color-attribute-shadowvml"></a><span data-ttu-id="a1761-103">Color, attribut (Shadow) (VML)</span><span class="sxs-lookup"><span data-stu-id="a1761-103">Color Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="a1761-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a1761-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a1761-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a1761-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a1761-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="a1761-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a1761-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="a1761-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a1761-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a1761-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a1761-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a1761-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a1761-110">Définit la couleur de l’ombre.</span><span class="sxs-lookup"><span data-stu-id="a1761-110">Defines the color of the shadow.</span></span> <span data-ttu-id="a1761-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a1761-111">Read/write.</span></span> <span data-ttu-id="a1761-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="a1761-112">**VgColor**.</span></span>

<span data-ttu-id="a1761-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="a1761-113">**Applies To**</span></span>

[<span data-ttu-id="a1761-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="a1761-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="a1761-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="a1761-115">**Tag Syntax**</span></span>

<span data-ttu-id="a1761-116"><v : *Element* Color = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a1761-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="a1761-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="a1761-117">**Script Syntax**</span></span>

<span data-ttu-id="a1761-118">*Element* . Color = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="a1761-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="a1761-119">*expression* = *Element*. Color</span><span class="sxs-lookup"><span data-stu-id="a1761-119">*expression*=*element*.color</span></span>

<span data-ttu-id="a1761-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="a1761-120">**Remarks**</span></span>

<span data-ttu-id="a1761-121">Utilisez l’attribut Color pour définir ou obtenir la couleur d’une ombre.</span><span class="sxs-lookup"><span data-stu-id="a1761-121">Use the color attribute to set or get the color of a shadow.</span></span>

<span data-ttu-id="a1761-122">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="a1761-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="a1761-123">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="a1761-123">**Example**</span></span>

<span data-ttu-id="a1761-124">L’ombre est verte.</span><span class="sxs-lookup"><span data-stu-id="a1761-124">The shadow is green.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green"/>
   </v:shape>
```



 

 