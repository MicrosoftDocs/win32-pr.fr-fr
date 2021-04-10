---
title: On, attribut (Shadow) (VML)
description: On, attribut (Shadow) (VML)
ms.assetid: 234fe63e-8a4a-4067-9d05-a8990d1cee5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83df69d8c90c99839f55836941746717a205d07a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941199"
---
# <a name="on-attribute-shadowvml"></a><span data-ttu-id="c8e41-103">On, attribut (Shadow) (VML)</span><span class="sxs-lookup"><span data-stu-id="c8e41-103">On Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="c8e41-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c8e41-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c8e41-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c8e41-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c8e41-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="c8e41-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c8e41-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="c8e41-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c8e41-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c8e41-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c8e41-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c8e41-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c8e41-110">Détermine si une ombre sera affichée.</span><span class="sxs-lookup"><span data-stu-id="c8e41-110">Determines whether a shadow will be displayed.</span></span> <span data-ttu-id="c8e41-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c8e41-111">Read/write.</span></span> <span data-ttu-id="c8e41-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="c8e41-112">**VgTriState**.</span></span>

<span data-ttu-id="c8e41-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c8e41-113">**Applies To**</span></span>

[<span data-ttu-id="c8e41-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="c8e41-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="c8e41-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="c8e41-115">**Tag Syntax**</span></span>

<span data-ttu-id="c8e41-116"><v : *Element* on = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c8e41-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="c8e41-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="c8e41-117">**Script Syntax**</span></span>

<span data-ttu-id="c8e41-118">*Element* . on = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="c8e41-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="c8e41-119">*expression* = *élément*. on</span><span class="sxs-lookup"><span data-stu-id="c8e41-119">*expression*=*element*.on</span></span>

<span data-ttu-id="c8e41-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="c8e41-120">**Remarks**</span></span>

<span data-ttu-id="c8e41-121">Si la **valeur est true**, l’ombre est affichée.</span><span class="sxs-lookup"><span data-stu-id="c8e41-121">If **True**, the shadow will be displayed.</span></span> <span data-ttu-id="c8e41-122">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="c8e41-122">The default value is **False**.</span></span>

<span data-ttu-id="c8e41-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="c8e41-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="c8e41-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="c8e41-124">**Example**</span></span>

<span data-ttu-id="c8e41-125">L’ombre s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c8e41-125">The shadow will be displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True"/>
   </v:shape>
```





 

 