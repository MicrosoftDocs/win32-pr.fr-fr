---
title: Attribut SRC (Fill) (VML)
description: Attribut SRC (Fill) (VML)
ms.assetid: 88ad9413-1863-41e2-855b-2bf155ce23cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddfcc6bb0ba7b4b026287c1efbbd8a20e09c37a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463186"
---
# <a name="src-attribute-fillvml"></a><span data-ttu-id="bfa02-103">Attribut SRC (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="bfa02-103">Src Attribute (Fill)(VML)</span></span>

<span data-ttu-id="bfa02-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bfa02-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bfa02-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="bfa02-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bfa02-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="bfa02-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bfa02-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="bfa02-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bfa02-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bfa02-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bfa02-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bfa02-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bfa02-110">Définit l’image à charger pour un remplissage.</span><span class="sxs-lookup"><span data-stu-id="bfa02-110">Defines the image to load for a fill.</span></span> <span data-ttu-id="bfa02-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bfa02-111">Read/write.</span></span> <span data-ttu-id="bfa02-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="bfa02-112">**String**.</span></span>

<span data-ttu-id="bfa02-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="bfa02-113">**Applies To**</span></span>

[<span data-ttu-id="bfa02-114">Complète</span><span class="sxs-lookup"><span data-stu-id="bfa02-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="bfa02-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="bfa02-115">**Tag Syntax**</span></span>

<span data-ttu-id="bfa02-116"><v : *Element* SRC = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="bfa02-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="bfa02-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="bfa02-117">**Script Syntax**</span></span>

<span data-ttu-id="bfa02-118">*Element* . src = "*expression \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="bfa02-118">*element* .src="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="bfa02-119">*expression* = *élément*. SRC</span><span class="sxs-lookup"><span data-stu-id="bfa02-119">*expression*=*element*.src</span></span>

<span data-ttu-id="bfa02-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="bfa02-120">**Remarks**</span></span>

<span data-ttu-id="bfa02-121">URL vers une image à charger pour les remplissages d’image et de motif.</span><span class="sxs-lookup"><span data-stu-id="bfa02-121">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="bfa02-122">Cet attribut doit toujours être présent et pointer vers des données d’image valides pour qu’une image s’affiche.</span><span class="sxs-lookup"><span data-stu-id="bfa02-122">This attribute must always be present and point to valid image data for a picture to appear.</span></span> <span data-ttu-id="bfa02-123">Si cet attribut apparaît seul (autrement dit, aucun attribut **href** ou **title** ), l’image est liée.</span><span class="sxs-lookup"><span data-stu-id="bfa02-123">If this attribute appears alone (that is, no **HRef** or **Title** attribute), then the image is linked.</span></span>

<span data-ttu-id="bfa02-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="bfa02-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="bfa02-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bfa02-125">**Example**</span></span>

<span data-ttu-id="bfa02-126">Une image en mosaïque utilisant le fichier myimage.gif en tant que source est affichée.</span><span class="sxs-lookup"><span data-stu-id="bfa02-126">A tiled image using the file myimage.gif as a source is displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 