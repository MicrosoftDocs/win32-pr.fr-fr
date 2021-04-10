---
title: ID, attribut (VMLFrame) (VML)
description: ID, attribut (VMLFrame) (VML)
ms.assetid: 3580fad7-b49e-44d7-b266-90fbfc2a02c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f9c5254a2dca186651bb49b677febe747f37c4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031454"
---
# <a name="id-attribute-vmlframevml"></a><span data-ttu-id="c18c5-103">ID, attribut (VMLFrame) (VML)</span><span class="sxs-lookup"><span data-stu-id="c18c5-103">ID Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="c18c5-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c18c5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c18c5-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c18c5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c18c5-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="c18c5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c18c5-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="c18c5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c18c5-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c18c5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c18c5-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c18c5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c18c5-110">Définit un identificateur unique pour le frame.</span><span class="sxs-lookup"><span data-stu-id="c18c5-110">Defines a unique identifier for the frame.</span></span> <span data-ttu-id="c18c5-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c18c5-111">Read/write.</span></span> <span data-ttu-id="c18c5-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="c18c5-112">**String**.</span></span>

<span data-ttu-id="c18c5-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c18c5-113">**Applies To**</span></span>

[<span data-ttu-id="c18c5-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="c18c5-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="c18c5-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="c18c5-115">**Tag Syntax**</span></span>

<span data-ttu-id="c18c5-116"><v : *élément* ID = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="c18c5-116"><v: *element* ID=" *expression* "></span></span>

<span data-ttu-id="c18c5-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="c18c5-117">**Script Syntax**</span></span>

<span data-ttu-id="c18c5-118">*Element* . ID = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="c18c5-118">*element* .ID="*expression*"</span></span>

<span data-ttu-id="c18c5-119">*expression* = *élément*. ID</span><span class="sxs-lookup"><span data-stu-id="c18c5-119">*expression*=*element*.ID</span></span>

<span data-ttu-id="c18c5-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="c18c5-120">**Remarks**</span></span>

<span data-ttu-id="c18c5-121">Utilisez l' **ID** pour référencer un frame.</span><span class="sxs-lookup"><span data-stu-id="c18c5-121">Use **ID** to reference a frame.</span></span> <span data-ttu-id="c18c5-122">Par exemple, vous pouvez déplacer le cadre sur la page en modifiant la position de cadre référencée par l' **ID**.</span><span class="sxs-lookup"><span data-stu-id="c18c5-122">For example, you can move the frame around on the page by changing the frame position referenced by the **ID**.</span></span>

<span data-ttu-id="c18c5-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="c18c5-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="c18c5-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="c18c5-124">**Example**</span></span>

<span data-ttu-id="c18c5-125">L' **ID** du frame est « frame01 ».</span><span class="sxs-lookup"><span data-stu-id="c18c5-125">The **ID** of the frame is "frame01".</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 