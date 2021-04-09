---
title: ConnectType VML (attribut)
description: ConnectType VML (attribut)
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a54135dcb4ffe0a86f781d68b8babe1259029be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101664"
---
# <a name="vml-connecttype-attribute"></a><span data-ttu-id="b1690-103">ConnectType VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="b1690-103">VML ConnectType Attribute</span></span>

<span data-ttu-id="b1690-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b1690-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b1690-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b1690-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b1690-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="b1690-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b1690-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="b1690-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b1690-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b1690-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b1690-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b1690-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b1690-110">Définit le type de points de connexion utilisé pour attacher des formes à d’autres formes.</span><span class="sxs-lookup"><span data-stu-id="b1690-110">Defines the type of connection points used for attaching shapes to other shapes.</span></span> <span data-ttu-id="b1690-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b1690-111">Read/write.</span></span> <span data-ttu-id="b1690-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="b1690-112">**String**.</span></span>

<span data-ttu-id="b1690-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b1690-113">**Applies To**</span></span>

[<span data-ttu-id="b1690-114">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b1690-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="b1690-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="b1690-115">**Tag Syntax**</span></span>

<span data-ttu-id="b1690-116"><v : *Element* o :connecttype = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b1690-116"><v: *element* o:connecttype=" *expression* "></span></span>

<span data-ttu-id="b1690-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="b1690-117">**Remarks**</span></span>

<span data-ttu-id="b1690-118">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="b1690-118">Values include:</span></span>



| <span data-ttu-id="b1690-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1690-119">Value</span></span>    | <span data-ttu-id="b1690-120">Description</span><span class="sxs-lookup"><span data-stu-id="b1690-120">Description</span></span>                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1690-121">aucun</span><span class="sxs-lookup"><span data-stu-id="b1690-121">none</span></span>     | <span data-ttu-id="b1690-122">Aucun site de connexion.</span><span class="sxs-lookup"><span data-stu-id="b1690-122">No connection sites.</span></span> <span data-ttu-id="b1690-123">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="b1690-123">Default.</span></span>                                                                                                         |
| <span data-ttu-id="b1690-124">rect</span><span class="sxs-lookup"><span data-stu-id="b1690-124">rect</span></span>     | <span data-ttu-id="b1690-125">Quatre points de connexion standard aux milieux des côtés supérieur, inférieur, gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="b1690-125">Standard four connection points at midpoints of top, bottom, left, and right sides.</span></span>                                                   |
| <span data-ttu-id="b1690-126">segments</span><span class="sxs-lookup"><span data-stu-id="b1690-126">segments</span></span> | <span data-ttu-id="b1690-127">Les points d’édition de la forme sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="b1690-127">The edit points of the shape are used.</span></span> <span data-ttu-id="b1690-128">Les points de modification sont les points noirs d’un éditeur graphique qui permettent de sélectionner des parties d’une forme.</span><span class="sxs-lookup"><span data-stu-id="b1690-128">Edit points are the black dots in a graphical editor that are used to select parts of a shape.</span></span> |
| <span data-ttu-id="b1690-129">custom</span><span class="sxs-lookup"><span data-stu-id="b1690-129">custom</span></span>   | <span data-ttu-id="b1690-130">Tableau personnalisé d’emplacements de connexion.</span><span class="sxs-lookup"><span data-stu-id="b1690-130">A custom array of connection locations.</span></span>                                                                                               |



 

<span data-ttu-id="b1690-131">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="b1690-131">*Microsoft Office Extensions Attribute*</span></span>

 

 