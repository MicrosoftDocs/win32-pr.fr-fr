---
title: Color2, attribut (Shadow) (VML)
description: Color2, attribut (Shadow) (VML)
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e735d7672457153881d384c7b625199cf4a202e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729196"
---
# <a name="color2-attribute-shadowvml"></a><span data-ttu-id="9d24d-103">Color2, attribut (Shadow) (VML)</span><span class="sxs-lookup"><span data-stu-id="9d24d-103">Color2 Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="9d24d-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9d24d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9d24d-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9d24d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9d24d-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="9d24d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9d24d-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="9d24d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9d24d-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9d24d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9d24d-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9d24d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9d24d-110">Définit la deuxième couleur d’une ombre.</span><span class="sxs-lookup"><span data-stu-id="9d24d-110">Defines the second color of a shadow.</span></span> <span data-ttu-id="9d24d-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9d24d-111">Read/write.</span></span> <span data-ttu-id="9d24d-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="9d24d-112">**VgColor**.</span></span>

<span data-ttu-id="9d24d-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="9d24d-113">**Applies To**</span></span>

[<span data-ttu-id="9d24d-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="9d24d-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="9d24d-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="9d24d-115">**Tag Syntax**</span></span>

<span data-ttu-id="9d24d-116"><v : *élément* color2 = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="9d24d-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="9d24d-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="9d24d-117">**Script Syntax**</span></span>

<span data-ttu-id="9d24d-118">*Element* . color2 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="9d24d-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="9d24d-119">*expression* = *élément*. color2</span><span class="sxs-lookup"><span data-stu-id="9d24d-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="9d24d-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="9d24d-120">**Remarks**</span></span>

<span data-ttu-id="9d24d-121">Utilisez une deuxième couleur pour créer des effets d’ombre spéciaux.</span><span class="sxs-lookup"><span data-stu-id="9d24d-121">Use a second color to create special shadow effects.</span></span> <span data-ttu-id="9d24d-122">Pour plus d’informations sur les deuxièmes couleurs, consultez l’attribut [type](type-attribute--shadow--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="9d24d-122">See the [Type](type-attribute--shadow--vml.md) attribute for more information about second colors.</span></span>

<span data-ttu-id="9d24d-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="9d24d-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="9d24d-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="9d24d-124">**Example**</span></span>

<span data-ttu-id="9d24d-125">L’ombre est bleue pour une deuxième couleur.</span><span class="sxs-lookup"><span data-stu-id="9d24d-125">The shadow has blue for a second color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green" color2="blue"/>
   </v:shape>
```



 

 