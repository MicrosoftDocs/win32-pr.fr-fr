---
title: Élément de format VML VML
description: Élément de format VML VML
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbb35eef0a3c987fe1e6ec35d15701236ae0af1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199269"
---
# <a name="vml-shapetype-element"></a><span data-ttu-id="08e5e-103">Élément de format VML VML</span><span class="sxs-lookup"><span data-stu-id="08e5e-103">VML ShapeType Element</span></span>

<span data-ttu-id="08e5e-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="08e5e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="08e5e-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="08e5e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="08e5e-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="08e5e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="08e5e-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="08e5e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="08e5e-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="08e5e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="08e5e-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="08e5e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="08e5e-110">Définit une forme qui peut être utilisée pour créer d’autres formes.</span><span class="sxs-lookup"><span data-stu-id="08e5e-110">Defines a shape that can be used to create other shapes.</span></span>

<span data-ttu-id="08e5e-111">L’attribut suivant modifie un **Typedeforme**.</span><span class="sxs-lookup"><span data-stu-id="08e5e-111">The following attribute modifies a **ShapeType**.</span></span>



| <span data-ttu-id="08e5e-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="08e5e-112">Attribute</span></span>                                      | <span data-ttu-id="08e5e-113">Description</span><span class="sxs-lookup"><span data-stu-id="08e5e-113">Description</span></span>                                             |
|------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="08e5e-114">Master</span><span class="sxs-lookup"><span data-stu-id="08e5e-114">Master</span></span>](msdn-online-vml-master-attribute.md) | <span data-ttu-id="08e5e-115">Détermine si un **Typedeforme** est un élément principal.</span><span class="sxs-lookup"><span data-stu-id="08e5e-115">Determines whether a **ShapeType** is a master element.</span></span> |



 

<span data-ttu-id="08e5e-116">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="08e5e-116">**Remarks**</span></span>

<span data-ttu-id="08e5e-117">**Typedeforme** est identique à l’élément **Shape** , à ceci près qu’il ne peut pas faire référence à un autre élément **Typedeforme** .</span><span class="sxs-lookup"><span data-stu-id="08e5e-117">**ShapeType** is identical to the **Shape** element except it cannot reference another **ShapeType** element.</span></span>

<span data-ttu-id="08e5e-118">Lorsqu’un élément **Shape** fait référence à un **Typedeforme**, la **forme** peut dupliquer certaines des propriétés qui ont déjà été spécifiées dans **Typedeforme**.</span><span class="sxs-lookup"><span data-stu-id="08e5e-118">When a **Shape** element makes reference to a **ShapeType**, the **Shape** may duplicate some of the properties that have already been specified in the **ShapeType**.</span></span> <span data-ttu-id="08e5e-119">Dans ces cas, les attributs de la **forme** remplacent ceux du **Typedeforme**.</span><span class="sxs-lookup"><span data-stu-id="08e5e-119">In these cases, the attributes in the **Shape** override those of the **ShapeType**.</span></span>

<span data-ttu-id="08e5e-120">L’attribut **type** ne peut pas être utilisé avec **Typedeforme**.</span><span class="sxs-lookup"><span data-stu-id="08e5e-120">The **Type** attribute may not be used with **ShapeType**.</span></span>

<span data-ttu-id="08e5e-121">Les attributs de positionnement CSS (tels que **haut**, **gauche**, etc.) ne sont pas transmis à une **forme** à partir d’un **Typedeforme**.</span><span class="sxs-lookup"><span data-stu-id="08e5e-121">CSS positioning attributes (such as **Top**, **Left**, etc.) are not passed to a **Shape** from a **ShapeType**.</span></span>

<span data-ttu-id="08e5e-122">Pour utiliser cet élément, créez un **Typedeforme** avec un attribut d' [ID](id-attribute--vml.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="08e5e-122">To use this element, create a **ShapeType** with a specific [ID](id-attribute--vml.md) attribute.</span></span> <span data-ttu-id="08e5e-123">Créez ensuite une **forme** et référencez le **Typedeforme** avec l’attribut **type** .</span><span class="sxs-lookup"><span data-stu-id="08e5e-123">Then create a **Shape** and reference the **ShapeType** with the **Type** attribute.</span></span> <span data-ttu-id="08e5e-124">Pour plus d’informations, consultez l’attribut [type](type-attribute--shape--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="08e5e-124">See the [Type](type-attribute--shape--vml.md) attribute for more information.</span></span>

 

 