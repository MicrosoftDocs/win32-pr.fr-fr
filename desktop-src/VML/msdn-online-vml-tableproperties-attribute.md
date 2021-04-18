---
title: TableProperties VML (attribut)
description: TableProperties VML (attribut)
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0f010f673b2663764814150f7a38fc06f23e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512502"
---
# <a name="vml-tableproperties-attribute"></a><span data-ttu-id="c95a2-103">TableProperties VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="c95a2-103">VML TableProperties Attribute</span></span>

<span data-ttu-id="c95a2-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c95a2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c95a2-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c95a2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c95a2-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="c95a2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c95a2-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="c95a2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c95a2-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c95a2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c95a2-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c95a2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c95a2-110">Détermine les propriétés de la table.</span><span class="sxs-lookup"><span data-stu-id="c95a2-110">Determines table properties.</span></span> <span data-ttu-id="c95a2-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c95a2-111">Read/write.</span></span> <span data-ttu-id="c95a2-112">**Integer**.</span><span class="sxs-lookup"><span data-stu-id="c95a2-112">**Integer**.</span></span>

<span data-ttu-id="c95a2-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c95a2-113">**Applies To**</span></span>

[<span data-ttu-id="c95a2-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="c95a2-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="c95a2-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="c95a2-115">**Tag Syntax**</span></span>

<span data-ttu-id="c95a2-116"><v : *Element* o :TableProperties = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c95a2-116"><v: *element* o:tableproperties=" *expression* "></span></span>

<span data-ttu-id="c95a2-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="c95a2-117">**Remarks**</span></span>

<span data-ttu-id="c95a2-118">Utilisé par Microsoft PowerPoint pour les tables natives.</span><span class="sxs-lookup"><span data-stu-id="c95a2-118">Used by Microsoft PowerPoint for native tables.</span></span> <span data-ttu-id="c95a2-119">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="c95a2-119">Default value is 0.</span></span> <span data-ttu-id="c95a2-120">Seuls les trois premiers bits de cet entier sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="c95a2-120">Only the first three bits of this integer are used.</span></span>

<span data-ttu-id="c95a2-121">Même si la valeur est stockée dans une forme, l’attribut n’est utile que lorsque la table est constituée de formes regroupées. Les bits peuvent être combinés.</span><span class="sxs-lookup"><span data-stu-id="c95a2-121">Even though the value is stored in a shape, the attribute is only useful when the table is made up of shapes that are grouped.Bits may be combined.</span></span>

<span data-ttu-id="c95a2-122">Les valeurs de bits suivantes sont incluses.</span><span class="sxs-lookup"><span data-stu-id="c95a2-122">The following bit values are included.</span></span>



| <span data-ttu-id="c95a2-123">bit</span><span class="sxs-lookup"><span data-stu-id="c95a2-123">Bit</span></span> | <span data-ttu-id="c95a2-124">Description</span><span class="sxs-lookup"><span data-stu-id="c95a2-124">Description</span></span>                              |
|-----|------------------------------------------|
| <span data-ttu-id="c95a2-125">1</span><span class="sxs-lookup"><span data-stu-id="c95a2-125">1</span></span>   | <span data-ttu-id="c95a2-126">Définit si le groupe de formes est une table.</span><span class="sxs-lookup"><span data-stu-id="c95a2-126">Set if the group of shapes is a table.</span></span>   |
| <span data-ttu-id="c95a2-127">2</span><span class="sxs-lookup"><span data-stu-id="c95a2-127">2</span></span>   | <span data-ttu-id="c95a2-128">Définit si la forme est un espace réservé.</span><span class="sxs-lookup"><span data-stu-id="c95a2-128">Set if the shape is a placeholder.</span></span>       |
| <span data-ttu-id="c95a2-129">3</span><span class="sxs-lookup"><span data-stu-id="c95a2-129">3</span></span>   | <span data-ttu-id="c95a2-130">Définit si le texte de la table est bidirectionnel.</span><span class="sxs-lookup"><span data-stu-id="c95a2-130">Set if the table text is bi-directional.</span></span> |



 

<span data-ttu-id="c95a2-131">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="c95a2-131">*Microsoft Office Extensions Attribute*</span></span>

 

 