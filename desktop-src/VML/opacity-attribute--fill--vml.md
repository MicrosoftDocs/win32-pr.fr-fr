---
title: Attribut Opacity (Fill) (VML)
description: Attribut Opacity (Fill) (VML)
ms.assetid: abd2fe4d-6391-4413-80f0-549bcc74f42e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b913498705e65fa7211db4b4cef039894d573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730133"
---
# <a name="opacity-attribute-fillvml"></a><span data-ttu-id="adacd-103">Attribut Opacity (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="adacd-103">Opacity Attribute (Fill)(VML)</span></span>

<span data-ttu-id="adacd-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="adacd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="adacd-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="adacd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="adacd-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="adacd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="adacd-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="adacd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="adacd-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="adacd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="adacd-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="adacd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="adacd-110">Définit la transparence d’un remplissage.</span><span class="sxs-lookup"><span data-stu-id="adacd-110">Defines the transparency of a fill.</span></span> <span data-ttu-id="adacd-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="adacd-111">Read/write.</span></span> <span data-ttu-id="adacd-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="adacd-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span>

<span data-ttu-id="adacd-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="adacd-113">**Applies To**</span></span>

[<span data-ttu-id="adacd-114">Complète</span><span class="sxs-lookup"><span data-stu-id="adacd-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="adacd-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="adacd-115">**Tag Syntax**</span></span>

<span data-ttu-id="adacd-116"><v : *Element* Opacity = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="adacd-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="adacd-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="adacd-117">**Script Syntax**</span></span>

<span data-ttu-id="adacd-118">*Element* . Opacity = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="adacd-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="adacd-119">*expression* = *Element*. Opacity</span><span class="sxs-lookup"><span data-stu-id="adacd-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="adacd-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="adacd-120">**Remarks**</span></span>

<span data-ttu-id="adacd-121">La valeur par défaut est 1,0.</span><span class="sxs-lookup"><span data-stu-id="adacd-121">The default value is 1.0.</span></span>

<span data-ttu-id="adacd-122">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="adacd-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="adacd-123">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="adacd-123">**Example**</span></span>

<span data-ttu-id="adacd-124">Le remplissage de la forme est transparent à 50%.</span><span class="sxs-lookup"><span data-stu-id="adacd-124">The fill of the shape will be 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill opacity="50%" color="red"/>
   </v:shape>
```



 

 