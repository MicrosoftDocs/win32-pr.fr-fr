---
title: Attribut masqué VML
description: Attribut masqué VML
ms.assetid: b8cdb066-e4fc-4dd6-a55a-7c2488f89e61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e383061d3210c9c52dc8c89322bd617257555e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031444"
---
# <a name="vml-obscured-attribute"></a><span data-ttu-id="db3d6-103">Attribut masqué VML</span><span class="sxs-lookup"><span data-stu-id="db3d6-103">VML Obscured Attribute</span></span>

<span data-ttu-id="db3d6-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="db3d6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="db3d6-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="db3d6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="db3d6-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="db3d6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="db3d6-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="db3d6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="db3d6-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="db3d6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="db3d6-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="db3d6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="db3d6-110">Détermine si une ombre est transparente.</span><span class="sxs-lookup"><span data-stu-id="db3d6-110">Determines whether a shadow is transparent.</span></span> <span data-ttu-id="db3d6-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="db3d6-111">Read/write.</span></span> <span data-ttu-id="db3d6-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="db3d6-112">**VgTriState**.</span></span>

<span data-ttu-id="db3d6-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="db3d6-113">**Applies To**</span></span>

[<span data-ttu-id="db3d6-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="db3d6-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="db3d6-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="db3d6-115">**Tag Syntax**</span></span>

<span data-ttu-id="db3d6-116"><v : *Element* obscurcied = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="db3d6-116"><v: *element* obscured=" *expression* "></span></span>

<span data-ttu-id="db3d6-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="db3d6-117">**Script Syntax**</span></span>

<span data-ttu-id="db3d6-118">*Element* . obscurcied = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="db3d6-118">*element* .obscured="*expression*"</span></span>

<span data-ttu-id="db3d6-119">*expression* = *Element*. obscurcid</span><span class="sxs-lookup"><span data-stu-id="db3d6-119">*expression*=*element*.obscured</span></span>

<span data-ttu-id="db3d6-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="db3d6-120">**Remarks**</span></span>

<span data-ttu-id="db3d6-121">Si la **valeur est true**, vous permet de voir l’ombre si aucun remplissage n’est présent sur la forme.</span><span class="sxs-lookup"><span data-stu-id="db3d6-121">If **True**, lets you see through the shadow if there is no fill on the shape.</span></span> <span data-ttu-id="db3d6-122">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="db3d6-122">Default is **False**.</span></span>

<span data-ttu-id="db3d6-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="db3d6-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="db3d6-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="db3d6-124">**Example**</span></span>

<span data-ttu-id="db3d6-125">L’arrière-plan montre l’ombre.</span><span class="sxs-lookup"><span data-stu-id="db3d6-125">The background shows through the shadow.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" obscured="True"/>
   </v:shape>
```



 

 