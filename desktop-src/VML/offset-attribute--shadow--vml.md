---
title: Offset, attribut (Shadow) (VML)
description: Offset, attribut (Shadow) (VML)
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61daaf3b311a87a3e3bcf064ceffc491e1134fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941055"
---
# <a name="offset-attribute-shadowvml"></a><span data-ttu-id="d754d-103">Offset, attribut (Shadow) (VML)</span><span class="sxs-lookup"><span data-stu-id="d754d-103">Offset Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="d754d-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d754d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d754d-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d754d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d754d-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="d754d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d754d-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="d754d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d754d-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d754d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d754d-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d754d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d754d-110">Définit le degré d’extension de l’ombre au-delà de la forme.</span><span class="sxs-lookup"><span data-stu-id="d754d-110">Defines how far the shadow extends past the shape.</span></span> <span data-ttu-id="d754d-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d754d-111">Read/write.</span></span> <span data-ttu-id="d754d-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="d754d-112">**VgVector2D**.</span></span>

<span data-ttu-id="d754d-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="d754d-113">**Applies To**</span></span>

[<span data-ttu-id="d754d-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="d754d-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="d754d-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="d754d-115">**Tag Syntax**</span></span>

<span data-ttu-id="d754d-116"><v : offset de l' *élément* = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="d754d-116"><v: *element* offset=" *expression* "></span></span>

<span data-ttu-id="d754d-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="d754d-117">**Script Syntax**</span></span>

<span data-ttu-id="d754d-118">*Element* . Offset = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="d754d-118">*element* .offset="*expression*"</span></span>

<span data-ttu-id="d754d-119">*expression* = *Element*. Offset</span><span class="sxs-lookup"><span data-stu-id="d754d-119">*expression*=*element*.offset</span></span>

<span data-ttu-id="d754d-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="d754d-120">**Remarks**</span></span>

<span data-ttu-id="d754d-121">Le décalage par défaut de la valeur x est 2pt et la valeur par défaut de la valeur y est 2pt.</span><span class="sxs-lookup"><span data-stu-id="d754d-121">The default offset for the x value is 2pt and the default for the y value is 2pt.</span></span> <span data-ttu-id="d754d-122">Les valeurs sont soit une mesure absolue, soit une valeur fractionnaire de forme.</span><span class="sxs-lookup"><span data-stu-id="d754d-122">Values are either an absolute measurement, or a fractional value of shape.</span></span> <span data-ttu-id="d754d-123">Si fractionnaires, elles sont comprises entre 50% et-50%.</span><span class="sxs-lookup"><span data-stu-id="d754d-123">If fractional, they range from 50% to -50%.</span></span>

<span data-ttu-id="d754d-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="d754d-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="d754d-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="d754d-125">**Example**</span></span>

<span data-ttu-id="d754d-126">La forme a une ombre avec un décalage de 5 points vers le dessous et de 10 points vers la droite.</span><span class="sxs-lookup"><span data-stu-id="d754d-126">The shape has a shadow with an offset of 5 points down and 10 points to the right.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 