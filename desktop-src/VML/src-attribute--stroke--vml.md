---
title: Attribut SRC (Stroke) (VML)
description: Attribut SRC (Stroke) (VML)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5833b24abf0f16c6e17fa3319931565ee6c232
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727541"
---
# <a name="src-attribute-strokevml"></a><span data-ttu-id="d766d-103">Attribut SRC (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="d766d-103">Src Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="d766d-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d766d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d766d-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d766d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d766d-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="d766d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d766d-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="d766d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d766d-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d766d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d766d-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d766d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d766d-110">Définit l’image source à charger pour un remplissage de trait.</span><span class="sxs-lookup"><span data-stu-id="d766d-110">Defines the source image to load for a stroke fill.</span></span> <span data-ttu-id="d766d-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d766d-111">Read/write.</span></span> <span data-ttu-id="d766d-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="d766d-112">**String**.</span></span>

<span data-ttu-id="d766d-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="d766d-113">**Applies To**</span></span>

[<span data-ttu-id="d766d-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="d766d-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="d766d-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="d766d-115">**Tag Syntax**</span></span>

<span data-ttu-id="d766d-116"><v : *Element* SRC = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="d766d-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="d766d-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="d766d-117">**Script Syntax**</span></span>

<span data-ttu-id="d766d-118">*Element* . src = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="d766d-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="d766d-119">*expression* = *élément*. SRC</span><span class="sxs-lookup"><span data-stu-id="d766d-119">*expression*=*element*.src</span></span>

<span data-ttu-id="d766d-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="d766d-120">**Remarks**</span></span>

<span data-ttu-id="d766d-121">URL vers une image à charger pour les remplissages d’image et de motif.</span><span class="sxs-lookup"><span data-stu-id="d766d-121">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="d766d-122">Cet attribut doit toujours être présent et pointer vers des données d’image valides pour qu’une image s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d766d-122">This attribute must always be present and point to valid image data for a picture to appear.</span></span> <span data-ttu-id="d766d-123">Si cet attribut apparaît seul, autrement dit, sans **href** ou **titre**, l’image est liée.</span><span class="sxs-lookup"><span data-stu-id="d766d-123">If this attribute appears alone, that is, no **HRef** or **Title**, then the image is linked.</span></span>

<span data-ttu-id="d766d-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="d766d-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="d766d-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="d766d-125">**Example**</span></span>

<span data-ttu-id="d766d-126">Le trait est créé avec l’image spécifiée par le fichier cylinder.gif.</span><span class="sxs-lookup"><span data-stu-id="d766d-126">The stroke is created with the image specified by the cylinder.gif file.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 