---
title: Attribut de pondération VML
description: Attribut de pondération VML
ms.assetid: 40164818-6b04-4afe-91cc-9fb8b12cb718
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7a1a4d5dca91da6b3750f0d901d4e278a80dd7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512108"
---
# <a name="vml-weight-attribute"></a><span data-ttu-id="b7b78-103">Attribut de pondération VML</span><span class="sxs-lookup"><span data-stu-id="b7b78-103">VML Weight Attribute</span></span>

<span data-ttu-id="b7b78-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b7b78-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b7b78-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b7b78-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b7b78-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="b7b78-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b7b78-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="b7b78-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b7b78-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b7b78-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b7b78-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b7b78-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b7b78-110">Définit l’épaisseur d’un trait.</span><span class="sxs-lookup"><span data-stu-id="b7b78-110">Defines the thickness of a stroke.</span></span> <span data-ttu-id="b7b78-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b7b78-111">Read/write.</span></span> <span data-ttu-id="b7b78-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="b7b78-112">**String**.</span></span>

<span data-ttu-id="b7b78-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b7b78-113">**Applies To**</span></span>

[<span data-ttu-id="b7b78-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="b7b78-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="b7b78-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="b7b78-115">**Tag Syntax**</span></span>

<span data-ttu-id="b7b78-116"><v : poids de l' *élément* = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="b7b78-116"><v: *element* weight=" *expression* "></span></span>

<span data-ttu-id="b7b78-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="b7b78-117">**Script Syntax**</span></span>

<span data-ttu-id="b7b78-118">*Element* . Weight = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b7b78-118">*element* .weight="*expression*"</span></span>

<span data-ttu-id="b7b78-119">*expression* = *élément*. poids</span><span class="sxs-lookup"><span data-stu-id="b7b78-119">*expression*=*element*.weight</span></span>

<span data-ttu-id="b7b78-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="b7b78-120">**Remarks**</span></span>

<span data-ttu-id="b7b78-121">Cet attribut est le même que l’attribut **StrokeWeight** de **Shape** et le remplace.</span><span class="sxs-lookup"><span data-stu-id="b7b78-121">This attribute is the same as the **StrokeWeight** attribute of **Shape** and overrides it.</span></span> <span data-ttu-id="b7b78-122">La valeur par défaut est 1 point.</span><span class="sxs-lookup"><span data-stu-id="b7b78-122">The default value is 1 point.</span></span>

<span data-ttu-id="b7b78-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="b7b78-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="b7b78-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="b7b78-124">**Example**</span></span>

<span data-ttu-id="b7b78-125">Le trait a une épaisseur de 5 points, et non pas de 2 points.</span><span class="sxs-lookup"><span data-stu-id="b7b78-125">The stroke has a thickness of 5 points, not 2 points.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="2pt"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke weight="5pt"/>
   </v:shape>
```



 

 