---
title: FillOK VML (attribut)
description: FillOK VML (attribut)
ms.assetid: 6855544d-0f12-4e21-8101-1bbf45795777
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 667524be103b7c641643a52a85368a82a1289e5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316410"
---
# <a name="vml-fillok-attribute"></a><span data-ttu-id="e3fd0-103">FillOK VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="e3fd0-103">VML FillOK Attribute</span></span>

<span data-ttu-id="e3fd0-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e3fd0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e3fd0-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e3fd0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e3fd0-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="e3fd0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e3fd0-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="e3fd0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e3fd0-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e3fd0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e3fd0-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e3fd0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e3fd0-110">Détermine si un remplissage est affiché.</span><span class="sxs-lookup"><span data-stu-id="e3fd0-110">Determines whether a fill will be displayed.</span></span> <span data-ttu-id="e3fd0-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e3fd0-111">Read/write.</span></span> <span data-ttu-id="e3fd0-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="e3fd0-112">**VgTriState**.</span></span>

<span data-ttu-id="e3fd0-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="e3fd0-113">**Applies To**</span></span>

[<span data-ttu-id="e3fd0-114">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="e3fd0-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="e3fd0-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="e3fd0-115">**Tag Syntax**</span></span>

<span data-ttu-id="e3fd0-116"><v : *Element* fillok = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="e3fd0-116"><v: *element* fillok=" *expression* "></span></span>

<span data-ttu-id="e3fd0-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="e3fd0-117">**Script Syntax**</span></span>

<span data-ttu-id="e3fd0-118">*Element* . fillok = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="e3fd0-118">*element* .fillok="*expression*"</span></span>

<span data-ttu-id="e3fd0-119">*expression* = *élément*. fillok</span><span class="sxs-lookup"><span data-stu-id="e3fd0-119">*expression*=*element*.fillok</span></span>

<span data-ttu-id="e3fd0-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="e3fd0-120">**Remarks**</span></span>

<span data-ttu-id="e3fd0-121">Si la **valeur est false**, le chemin d’accès ne peut pas être rempli.</span><span class="sxs-lookup"><span data-stu-id="e3fd0-121">If **False**, the path cannot be filled.</span></span> <span data-ttu-id="e3fd0-122">La valeur par défaut est **True**.</span><span class="sxs-lookup"><span data-stu-id="e3fd0-122">The default is **True**.</span></span> <span data-ttu-id="e3fd0-123">Cet attribut remplace tous les autres attributs de remplissage de l’élément parent ou **Fill** .</span><span class="sxs-lookup"><span data-stu-id="e3fd0-123">This attribute overrides all other fill attributes in the parent or **Fill** element.</span></span>

<span data-ttu-id="e3fd0-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="e3fd0-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="e3fd0-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="e3fd0-125">**Example**</span></span>

<span data-ttu-id="e3fd0-126">Le chemin d’accès ne sera pas rempli.</span><span class="sxs-lookup"><span data-stu-id="e3fd0-126">The path will not be filled.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" fillok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 