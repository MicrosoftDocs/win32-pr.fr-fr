---
title: ReGroupID VML (attribut)
description: ReGroupID VML (attribut)
ms.assetid: 2fbcc8c5-6e31-4301-9fb8-c2618bb17a1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384703d3fc5675013de09c4e3b5dec7505cf4164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382071"
---
# <a name="vml-regroupid-attribute"></a><span data-ttu-id="9d786-103">ReGroupID VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="9d786-103">VML ReGroupID Attribute</span></span>

<span data-ttu-id="9d786-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9d786-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9d786-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9d786-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9d786-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="9d786-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9d786-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="9d786-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9d786-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9d786-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9d786-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9d786-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9d786-110">Définit un groupe précédent pour une forme.</span><span class="sxs-lookup"><span data-stu-id="9d786-110">Defines a previous group for a shape.</span></span> <span data-ttu-id="9d786-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9d786-111">Read/write.</span></span> <span data-ttu-id="9d786-112">**VgInteger**.</span><span class="sxs-lookup"><span data-stu-id="9d786-112">**VgInteger**.</span></span>

<span data-ttu-id="9d786-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="9d786-113">**Applies To**</span></span>

[<span data-ttu-id="9d786-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="9d786-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="9d786-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="9d786-115">**Tag Syntax**</span></span>

<span data-ttu-id="9d786-116"><v : *Element* o :regroupid = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="9d786-116"><v: *element* o:regroupid=" *expression* "></span></span>

<span data-ttu-id="9d786-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="9d786-117">**Remarks**</span></span>

<span data-ttu-id="9d786-118">Un numéro d’identification est utilisé pour identifier des groupes de formes qui ne sont plus regroupées.</span><span class="sxs-lookup"><span data-stu-id="9d786-118">An ID number is used to identify groups of shapes that are no longer grouped.</span></span> <span data-ttu-id="9d786-119">Permet de regrouper les formes par programmation.</span><span class="sxs-lookup"><span data-stu-id="9d786-119">Allows shapes to be regrouped programmatically.</span></span>

<span data-ttu-id="9d786-120">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="9d786-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="9d786-121">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="9d786-121">**Example**</span></span>

<span data-ttu-id="9d786-122">La forme faisait partie d’un groupe désigné par l’ID de groupe 040754.</span><span class="sxs-lookup"><span data-stu-id="9d786-122">The shape was part of a group denoted by the group ID 040754.</span></span>


```HTML
   <v:shape id="rect01" ReGroupID="040754"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 