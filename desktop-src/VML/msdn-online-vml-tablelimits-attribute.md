---
title: TableLimits VML (attribut)
description: TableLimits VML (attribut)
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b35a7449cc2f348e6040161c1fb599c29972803
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727580"
---
# <a name="vml-tablelimits-attribute"></a><span data-ttu-id="1c6a2-103">TableLimits VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="1c6a2-103">VML TableLimits Attribute</span></span>

<span data-ttu-id="1c6a2-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1c6a2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1c6a2-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="1c6a2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1c6a2-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="1c6a2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1c6a2-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="1c6a2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1c6a2-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1c6a2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1c6a2-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1c6a2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1c6a2-110">Liste des valeurs de hauteur minimale pour chaque ligne d’une table.</span><span class="sxs-lookup"><span data-stu-id="1c6a2-110">List of minimum height values for each row in a table.</span></span> <span data-ttu-id="1c6a2-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1c6a2-111">Read/write.</span></span> <span data-ttu-id="1c6a2-112">**VgLengthArray**.</span><span class="sxs-lookup"><span data-stu-id="1c6a2-112">**VgLengthArray**.</span></span>

<span data-ttu-id="1c6a2-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="1c6a2-113">**Applies To**</span></span>

[<span data-ttu-id="1c6a2-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="1c6a2-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="1c6a2-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="1c6a2-115">**Tag Syntax**</span></span>

<span data-ttu-id="1c6a2-116"><v : *Element* o :tablelimits = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="1c6a2-116"><v: *element* o:tablelimits=" *expression* "></span></span>

<span data-ttu-id="1c6a2-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="1c6a2-117">**Remarks**</span></span>

<span data-ttu-id="1c6a2-118">Utilisé par Microsoft PowerPoint pour les tables natives.</span><span class="sxs-lookup"><span data-stu-id="1c6a2-118">Used by Microsoft PowerPoint for native tables.</span></span> <span data-ttu-id="1c6a2-119">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="1c6a2-119">Default value is **Null**.</span></span>

<span data-ttu-id="1c6a2-120">Même si la valeur est stockée dans une forme, l’attribut n’est utile que lorsque la table est constituée de formes regroupées.</span><span class="sxs-lookup"><span data-stu-id="1c6a2-120">Even though the value is stored in a shape, the attribute is only useful when the table is made up of shapes that are grouped.</span></span> <span data-ttu-id="1c6a2-121">Lorsque du texte est ajouté à des cellules de tableau, la hauteur de ligne peut augmenter.</span><span class="sxs-lookup"><span data-stu-id="1c6a2-121">When text is added to table cells, the row height may increase.</span></span> <span data-ttu-id="1c6a2-122">L’attribut **TableLimits** stocke la hauteur de ligne d’origine, de sorte que si le texte est supprimé, la hauteur de ligne ne sera pas inférieure à la valeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="1c6a2-122">The **TableLimits** attribute stores the original row height so that if text is deleted, the row height will not fall below the original value.</span></span>

<span data-ttu-id="1c6a2-123">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="1c6a2-123">*Microsoft Office Extensions Attribute*</span></span>

 

 