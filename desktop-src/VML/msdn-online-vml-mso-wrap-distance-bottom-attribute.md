---
title: VML DCL-Wrap-distance-attribut inférieur
description: VML DCL-Wrap-distance-attribut inférieur
ms.assetid: b096fc67-dd99-4833-bb82-73de7b06f43c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7c3ec66ae23994184227d857e269318606d9ea4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941151"
---
# <a name="vml-mso-wrap-distance-bottom-attribute"></a><span data-ttu-id="01ec4-103">VML DCL-Wrap-distance-attribut inférieur</span><span class="sxs-lookup"><span data-stu-id="01ec4-103">VML MSO-Wrap-Distance-Bottom Attribute</span></span>

<span data-ttu-id="01ec4-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="01ec4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="01ec4-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="01ec4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="01ec4-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="01ec4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="01ec4-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="01ec4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="01ec4-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="01ec4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="01ec4-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="01ec4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="01ec4-110">Définit la distance entre le côté inférieur de la forme et le texte qui l’entoure.</span><span class="sxs-lookup"><span data-stu-id="01ec4-110">Defines the distance from the bottom side of the shape to the text that wraps around it.</span></span> <span data-ttu-id="01ec4-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="01ec4-111">Read/write.</span></span> <span data-ttu-id="01ec4-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="01ec4-112">**String**.</span></span>

<span data-ttu-id="01ec4-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="01ec4-113">**Applies To**</span></span>

[<span data-ttu-id="01ec4-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="01ec4-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="01ec4-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="01ec4-115">**Tag Syntax**</span></span>

<span data-ttu-id="01ec4-116"><v : *Element* style = "mso-Wrap-distance-bottom : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="01ec4-116"><v: *element* style="mso-wrap-distance-bottom: *expression* "></span></span>

<span data-ttu-id="01ec4-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="01ec4-117">**Remarks**</span></span>

<span data-ttu-id="01ec4-118">Notez que cet attribut est différent de l’attribut **Margin** CSS.</span><span class="sxs-lookup"><span data-stu-id="01ec4-118">Note that this attribute is different from the CSS **Margin** attribute.</span></span> <span data-ttu-id="01ec4-119">La **marge** modifie l’origine de la forme pour inclure les zones de marge, mais la distance de retour à la ligne dans Microsoft Office ne modifie pas l’origine de la forme.</span><span class="sxs-lookup"><span data-stu-id="01ec4-119">**Margin** changes the origin of the shape to include the margin areas, but the wrap distance in Microsoft Office does not change the origin of the shape.</span></span>

<span data-ttu-id="01ec4-120">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="01ec4-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="01ec4-121">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="01ec4-121">**Example**</span></span>

<span data-ttu-id="01ec4-122">La forme a une distance inférieure de 10 points.</span><span class="sxs-lookup"><span data-stu-id="01ec4-122">The shape has a bottom wrap distance of 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-bottom:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 