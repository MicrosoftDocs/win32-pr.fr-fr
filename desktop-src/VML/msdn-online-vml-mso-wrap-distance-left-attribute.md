---
title: VML DCL-Wrap-distance-attribut à gauche
description: VML DCL-Wrap-distance-attribut à gauche
ms.assetid: 25dcb5d0-a839-4a4b-8969-8e5dcf1baa47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d1e47fff0f9dceff5fd98ad526208bf487d851
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315431"
---
# <a name="vml-mso-wrap-distance-left-attribute"></a><span data-ttu-id="34b60-103">VML DCL-Wrap-distance-attribut à gauche</span><span class="sxs-lookup"><span data-stu-id="34b60-103">VML MSO-Wrap-Distance-Left Attribute</span></span>

<span data-ttu-id="34b60-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="34b60-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="34b60-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="34b60-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="34b60-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="34b60-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="34b60-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="34b60-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="34b60-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="34b60-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="34b60-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="34b60-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="34b60-110">Définit la distance entre le côté gauche de la forme et le texte qui l’entoure.</span><span class="sxs-lookup"><span data-stu-id="34b60-110">Defines the distance from the left side of the shape to the text that wraps around it.</span></span> <span data-ttu-id="34b60-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="34b60-111">Read/write.</span></span> <span data-ttu-id="34b60-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="34b60-112">**String**.</span></span>

<span data-ttu-id="34b60-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="34b60-113">**Applies To**</span></span>

[<span data-ttu-id="34b60-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="34b60-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="34b60-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="34b60-115">**Tag Syntax**</span></span>

<span data-ttu-id="34b60-116"><v : *Element* style = "mso-Wrap-distance-left : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="34b60-116"><v: *element* style="mso-wrap-distance-left: *expression* "></span></span>

<span data-ttu-id="34b60-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="34b60-117">**Remarks**</span></span>

<span data-ttu-id="34b60-118">Notez que cet attribut est différent de l’attribut **Margin** CSS.</span><span class="sxs-lookup"><span data-stu-id="34b60-118">Note that this attribute is different from the CSS **Margin** attribute.</span></span> <span data-ttu-id="34b60-119">La **marge** modifie l’origine de la forme pour inclure les zones de marge, mais la distance de retour à la ligne dans Microsoft Office ne modifie pas l’origine de la forme.</span><span class="sxs-lookup"><span data-stu-id="34b60-119">**Margin** changes the origin of the shape to include the margin areas, but the wrap-distance in Microsoft Office does not change the origin of the shape.</span></span>

<span data-ttu-id="34b60-120">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="34b60-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="34b60-121">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="34b60-121">**Example**</span></span>

<span data-ttu-id="34b60-122">La forme a une distance de retour à la ligne à gauche de 10 points.</span><span class="sxs-lookup"><span data-stu-id="34b60-122">The shape has a left wrap-distance of 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-left:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 