---
title: Offset2 VML (attribut)
description: Offset2 VML (attribut)
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b5253e1a27ce8292ee5fc4ce49259db9512a5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508090"
---
# <a name="vml-offset2-attribute"></a><span data-ttu-id="3363a-103">Offset2 VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="3363a-103">VML Offset2 Attribute</span></span>

<span data-ttu-id="3363a-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3363a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3363a-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3363a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3363a-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="3363a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3363a-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="3363a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3363a-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3363a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3363a-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3363a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3363a-110">Détermine un deuxième offset.</span><span class="sxs-lookup"><span data-stu-id="3363a-110">Determines a second offset.</span></span> <span data-ttu-id="3363a-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3363a-111">Read/write.</span></span> <span data-ttu-id="3363a-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="3363a-112">**VgVector2D**.</span></span>

<span data-ttu-id="3363a-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="3363a-113">**Applies To**</span></span>

[<span data-ttu-id="3363a-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="3363a-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="3363a-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="3363a-115">**Tag Syntax**</span></span>

<span data-ttu-id="3363a-116"><v : *Element* offset2 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="3363a-116"><v: *element* offset2=" *expression* "></span></span>

<span data-ttu-id="3363a-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="3363a-117">**Script Syntax**</span></span>

<span data-ttu-id="3363a-118">*Element* . offset2 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="3363a-118">*element* .offset2="*expression*"</span></span>

<span data-ttu-id="3363a-119">*expression* = *élément*. offset2</span><span class="sxs-lookup"><span data-stu-id="3363a-119">*expression*=*element*.offset2</span></span>

<span data-ttu-id="3363a-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="3363a-120">**Remarks**</span></span>

<span data-ttu-id="3363a-121">La valeur par défaut d’un deuxième décalage pour la valeur x est 0 et la valeur par défaut de la valeur y est 0.</span><span class="sxs-lookup"><span data-stu-id="3363a-121">The default for a second offset for the x value is 0 and the default for the y value is 0.</span></span> <span data-ttu-id="3363a-122">Les valeurs sont soit une mesure absolue, soit une valeur fractionnaire de forme.</span><span class="sxs-lookup"><span data-stu-id="3363a-122">Values are either an absolute measurement, or a fractional value of shape.</span></span> <span data-ttu-id="3363a-123">Si fractionnaires, les valeurs sont comprises entre 50% et-50%.</span><span class="sxs-lookup"><span data-stu-id="3363a-123">If fractional, the values range from 50% to -50%.</span></span>

<span data-ttu-id="3363a-124">Utilisez un deuxième décalage pour créer des effets d’ombre spéciaux.</span><span class="sxs-lookup"><span data-stu-id="3363a-124">Use a second offset to create special shadow effects.</span></span> <span data-ttu-id="3363a-125">Pour plus d’informations sur les deux décalages, consultez l’attribut [type](type-attribute--shadow--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="3363a-125">See the [Type](type-attribute--shadow--vml.md) attribute for more information about second offsets.</span></span>

<span data-ttu-id="3363a-126">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="3363a-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="3363a-127">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="3363a-127">**Example**</span></span>

<span data-ttu-id="3363a-128">Une double ombre est créée pour la forme.</span><span class="sxs-lookup"><span data-stu-id="3363a-128">A double shadow is created for the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 