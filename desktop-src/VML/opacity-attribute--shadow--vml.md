---
title: Attribut Opacity (Shadow) (VML)
description: Attribut Opacity (Shadow) (VML)
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d09ca038a187c4a4ed1f914f5d05bcfd63e4a4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382088"
---
# <a name="opacity-attribute-shadowvml"></a><span data-ttu-id="40cfd-103">Attribut Opacity (Shadow) (VML)</span><span class="sxs-lookup"><span data-stu-id="40cfd-103">Opacity Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="40cfd-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="40cfd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="40cfd-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="40cfd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="40cfd-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="40cfd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="40cfd-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="40cfd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="40cfd-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="40cfd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="40cfd-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="40cfd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="40cfd-110">Détermine la transparence d’une ombre.</span><span class="sxs-lookup"><span data-stu-id="40cfd-110">Determines the transparency of a shadow.</span></span> <span data-ttu-id="40cfd-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="40cfd-111">Read/write.</span></span> <span data-ttu-id="40cfd-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="40cfd-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span></span>

<span data-ttu-id="40cfd-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="40cfd-113">**Applies To**</span></span>

[<span data-ttu-id="40cfd-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="40cfd-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="40cfd-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="40cfd-115">**Tag Syntax**</span></span>

<span data-ttu-id="40cfd-116"><v : *Element* Opacity = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="40cfd-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="40cfd-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="40cfd-117">**Script Syntax**</span></span>

<span data-ttu-id="40cfd-118">*Element* . Opacity = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="40cfd-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="40cfd-119">*expression* = *Element*. Opacity</span><span class="sxs-lookup"><span data-stu-id="40cfd-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="40cfd-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="40cfd-120">**Remarks**</span></span>

<span data-ttu-id="40cfd-121">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="40cfd-121">The default value is 1.</span></span> <span data-ttu-id="40cfd-122">La valeur 0 crée une ombre entièrement transparente.</span><span class="sxs-lookup"><span data-stu-id="40cfd-122">A value of 0 will make a completely transparent shadow.</span></span>

<span data-ttu-id="40cfd-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="40cfd-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="40cfd-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="40cfd-124">**Example**</span></span>

<span data-ttu-id="40cfd-125">La forme possède une ombre qui est transparente à 50%.</span><span class="sxs-lookup"><span data-stu-id="40cfd-125">The shape has a shadow that is 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 