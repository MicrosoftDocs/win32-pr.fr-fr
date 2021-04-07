---
title: InvX VML (attribut)
description: InvX VML (attribut)
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d244b5feff319112959d3093927f11d1e92164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728076"
---
# <a name="vml-invx-attribute"></a><span data-ttu-id="1fede-103">InvX VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="1fede-103">VML InvX Attribute</span></span>

<span data-ttu-id="1fede-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1fede-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1fede-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="1fede-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1fede-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="1fede-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1fede-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="1fede-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1fede-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1fede-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1fede-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1fede-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1fede-110">Détermine si la position x du handle est inversée.</span><span class="sxs-lookup"><span data-stu-id="1fede-110">Determines whether the x position of the handle is inverted.</span></span> <span data-ttu-id="1fede-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1fede-111">Read/write.</span></span> <span data-ttu-id="1fede-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="1fede-112">**VgTriState**.</span></span>

<span data-ttu-id="1fede-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="1fede-113">**Applies To**</span></span>

<span data-ttu-id="1fede-114">[H](msdn-online-vml-h-element.md) (sous-élément de [Handles](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="1fede-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="1fede-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="1fede-115">**Tag Syntax**</span></span>

<span data-ttu-id="1fede-116"><v : *Element* INVX = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="1fede-116"><v: *element* invx=" *expression* "></span></span>

<span data-ttu-id="1fede-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="1fede-117">**Remarks**</span></span>

<span data-ttu-id="1fede-118">Si la valeur est **true**, la position x du handle est inversée en soustrayant la valeur x de la valeur x de **CoordOrigin** ajoutée à la valeur x de **CoordSize**.</span><span class="sxs-lookup"><span data-stu-id="1fede-118">If **True**, the x position of the handle is inverted by subtracting the x value from the x value of **CoordOrigin** added to the x value of **CoordSize**.</span></span> <span data-ttu-id="1fede-119">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="1fede-119">The default value is **False**.</span></span>

<span data-ttu-id="1fede-120">Cet attribut est l’équivalent de</span><span class="sxs-lookup"><span data-stu-id="1fede-120">This attribute is the equivalent of</span></span>

<span data-ttu-id="1fede-121">coordorigin. x + coordsize. x-h. position. x</span><span class="sxs-lookup"><span data-stu-id="1fede-121">coordorigin.x + coordsize.x - h.position.x</span></span>

<span data-ttu-id="1fede-122">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="1fede-122">*VML Standard Attribute*</span></span>

 

 