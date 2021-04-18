---
title: Attribut de méthode VML
description: Attribut de méthode VML
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f7440e1e793e7ad34860524f63a3bfc38456f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511899"
---
# <a name="vml-method-attribute"></a><span data-ttu-id="8fd00-103">Attribut de méthode VML</span><span class="sxs-lookup"><span data-stu-id="8fd00-103">VML Method Attribute</span></span>

<span data-ttu-id="8fd00-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8fd00-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8fd00-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="8fd00-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8fd00-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="8fd00-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8fd00-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="8fd00-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8fd00-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8fd00-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8fd00-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8fd00-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8fd00-110">Définit la méthode utilisée pour générer un remplissage dégradé.</span><span class="sxs-lookup"><span data-stu-id="8fd00-110">Defines the method used to generate a gradient fill.</span></span> <span data-ttu-id="8fd00-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8fd00-111">Read/write.</span></span> <span data-ttu-id="8fd00-112">**VgSigmaType**.</span><span class="sxs-lookup"><span data-stu-id="8fd00-112">**VgSigmaType**.</span></span>

<span data-ttu-id="8fd00-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="8fd00-113">**Applies To**</span></span>

[<span data-ttu-id="8fd00-114">Complète</span><span class="sxs-lookup"><span data-stu-id="8fd00-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="8fd00-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="8fd00-115">**Tag Syntax**</span></span>

<span data-ttu-id="8fd00-116"><v : *Element* Method = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="8fd00-116"><v: *element* method=" *expression* "></span></span>

<span data-ttu-id="8fd00-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="8fd00-117">**Script Syntax**</span></span>

<span data-ttu-id="8fd00-118">*Element* . Method = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="8fd00-118">*element* .method="*expression*"</span></span>

<span data-ttu-id="8fd00-119">*expression* = *Element*. Method</span><span class="sxs-lookup"><span data-stu-id="8fd00-119">*expression*=*element*.method</span></span>

<span data-ttu-id="8fd00-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="8fd00-120">**Remarks**</span></span>

<span data-ttu-id="8fd00-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="8fd00-121">Values include:</span></span>



| <span data-ttu-id="8fd00-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fd00-122">Value</span></span>  | <span data-ttu-id="8fd00-123">Description</span><span class="sxs-lookup"><span data-stu-id="8fd00-123">Description</span></span>          |
|--------|----------------------|
| <span data-ttu-id="8fd00-124">Aucune</span><span class="sxs-lookup"><span data-stu-id="8fd00-124">None</span></span>   | <span data-ttu-id="8fd00-125">Aucun remplissage Sigma.</span><span class="sxs-lookup"><span data-stu-id="8fd00-125">No sigma fill.</span></span>       |
| <span data-ttu-id="8fd00-126">Linéaire</span><span class="sxs-lookup"><span data-stu-id="8fd00-126">Linear</span></span> | <span data-ttu-id="8fd00-127">Remplissage Sigma linéaire.</span><span class="sxs-lookup"><span data-stu-id="8fd00-127">Linear sigma fill.</span></span>   |
| <span data-ttu-id="8fd00-128">Sigma</span><span class="sxs-lookup"><span data-stu-id="8fd00-128">Sigma</span></span>  | <span data-ttu-id="8fd00-129">Remplissage Sigma.</span><span class="sxs-lookup"><span data-stu-id="8fd00-129">Sigma fill.</span></span> <span data-ttu-id="8fd00-130">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="8fd00-130">Default.</span></span> |
| <span data-ttu-id="8fd00-131">Quelconque</span><span class="sxs-lookup"><span data-stu-id="8fd00-131">Any</span></span>    | <span data-ttu-id="8fd00-132">Tout remplissage Sigma.</span><span class="sxs-lookup"><span data-stu-id="8fd00-132">Any sigma fill.</span></span>      |



 

<span data-ttu-id="8fd00-133">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="8fd00-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="8fd00-134">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="8fd00-134">**Example**</span></span>

<span data-ttu-id="8fd00-135">La forme aura un dégradé linéaire rouge.</span><span class="sxs-lookup"><span data-stu-id="8fd00-135">The shape will have a red linear gradient fill.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 