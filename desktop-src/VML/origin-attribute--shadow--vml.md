---
title: Origin, attribut (Shadow) (VML)
description: Origin, attribut (Shadow) (VML)
ms.assetid: acef5134-dad6-4ba6-9d70-a9f56cd8c5ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481c3df832ec08bc193db021244049fae96d9e34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729996"
---
# <a name="origin-attribute-shadowvml"></a><span data-ttu-id="3badc-103">Origin, attribut (Shadow) (VML)</span><span class="sxs-lookup"><span data-stu-id="3badc-103">Origin Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="3badc-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3badc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3badc-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3badc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3badc-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="3badc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3badc-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="3badc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3badc-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3badc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3badc-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3badc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3badc-110">Définit le centre de l’ombre.</span><span class="sxs-lookup"><span data-stu-id="3badc-110">Defines the center of the shadow.</span></span> <span data-ttu-id="3badc-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3badc-111">Read/write.</span></span> <span data-ttu-id="3badc-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="3badc-112">**VgVector2D**.</span></span>

<span data-ttu-id="3badc-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="3badc-113">**Applies To**</span></span>

[<span data-ttu-id="3badc-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="3badc-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="3badc-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="3badc-115">**Tag Syntax**</span></span>

<span data-ttu-id="3badc-116"><v : *élément* Origin = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="3badc-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="3badc-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="3badc-117">**Script Syntax**</span></span>

<span data-ttu-id="3badc-118">*Element* . Origin = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="3badc-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="3badc-119">*expression* = *élément*. Origin</span><span class="sxs-lookup"><span data-stu-id="3badc-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="3badc-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="3badc-120">**Remarks**</span></span>

<span data-ttu-id="3badc-121">Paire de valeurs fractionnaires de la forme, comprise entre 50% et-50%.</span><span class="sxs-lookup"><span data-stu-id="3badc-121">A pair of fractional values of the shape, ranging from 50% to -50%.</span></span> <span data-ttu-id="3badc-122">La valeur par défaut est 0,0.</span><span class="sxs-lookup"><span data-stu-id="3badc-122">The default value is 0,0.</span></span>

<span data-ttu-id="3badc-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="3badc-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="3badc-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="3badc-124">**Example**</span></span>

<span data-ttu-id="3badc-125">L’ombre a une origine dont la valeur est inférieure à 20% et à 20% à droite de l’origine de la forme.</span><span class="sxs-lookup"><span data-stu-id="3badc-125">The shadow has an origin that is 20% down and 20% to the right of the shape's origin.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" origin="20%,20%"/>
   </v:shape>
```



 

 