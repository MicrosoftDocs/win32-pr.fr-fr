---
title: Color2, attribut (Fill) (VML)
description: Color2, attribut (Fill) (VML)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5689bba52277b4056f57a171f3ffc1e197aa4c8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106538599"
---
# <a name="color2-attribute-fillvml"></a><span data-ttu-id="f6e1f-103">Color2, attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="f6e1f-103">Color2 Attribute (Fill)(VML)</span></span>

<span data-ttu-id="f6e1f-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f6e1f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f6e1f-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f6e1f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f6e1f-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="f6e1f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f6e1f-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="f6e1f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f6e1f-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f6e1f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f6e1f-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f6e1f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f6e1f-110">Définit une deuxième couleur pour les remplissages.</span><span class="sxs-lookup"><span data-stu-id="f6e1f-110">Defines a second color for fills.</span></span> <span data-ttu-id="f6e1f-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f6e1f-111">Read/write.</span></span> <span data-ttu-id="f6e1f-112">[VgColor](msdn-online-vml-ivgcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="f6e1f-112">[VgColor](msdn-online-vml-ivgcolor.md) .</span></span>

<span data-ttu-id="f6e1f-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="f6e1f-113">**Applies To**</span></span>

[<span data-ttu-id="f6e1f-114">Complète</span><span class="sxs-lookup"><span data-stu-id="f6e1f-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="f6e1f-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="f6e1f-115">**Tag Syntax**</span></span>

<span data-ttu-id="f6e1f-116"><v : *élément* color2 = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="f6e1f-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="f6e1f-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="f6e1f-117">**Script Syntax**</span></span>

<span data-ttu-id="f6e1f-118">*Element* . color2 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="f6e1f-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="f6e1f-119">*expression* = *élément*. color2</span><span class="sxs-lookup"><span data-stu-id="f6e1f-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="f6e1f-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="f6e1f-120">**Remarks**</span></span>

<span data-ttu-id="f6e1f-121">Une deuxième couleur est utilisée lorsqu’un type de remplissage est un modèle ou un dégradé.</span><span class="sxs-lookup"><span data-stu-id="f6e1f-121">A second color is used when a fill type is a pattern or a gradient.</span></span> <span data-ttu-id="f6e1f-122">La valeur par défaut est **blanc**.</span><span class="sxs-lookup"><span data-stu-id="f6e1f-122">The default value is **White**.</span></span>

<span data-ttu-id="f6e1f-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="f6e1f-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="f6e1f-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f6e1f-124">**Example**</span></span>

<span data-ttu-id="f6e1f-125">Le type de remplissage de la forme est un modèle dans lequel le remplissage de premier plan est défini par l’image source, mais l’arrière-plan transparent est défini par la deuxième couleur.</span><span class="sxs-lookup"><span data-stu-id="f6e1f-125">The shape's fill type is a pattern where the foreground fill is defined by the source image but the transparent background is defined by the second color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 