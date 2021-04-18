---
title: ConnectorType VML (attribut)
description: ConnectorType VML (attribut)
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0be0309e478970b93324b98a5efaaae54964435
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512314"
---
# <a name="vml-connectortype-attribute"></a><span data-ttu-id="ef981-103">ConnectorType VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="ef981-103">VML ConnectorType Attribute</span></span>

<span data-ttu-id="ef981-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ef981-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ef981-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ef981-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ef981-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="ef981-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ef981-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="ef981-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ef981-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ef981-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ef981-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ef981-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ef981-110">Indique le type de connecteur utilisé pour joindre des formes.</span><span class="sxs-lookup"><span data-stu-id="ef981-110">Indicates the type of connector used for joining shapes.</span></span> <span data-ttu-id="ef981-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ef981-111">Read/write.</span></span> <span data-ttu-id="ef981-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="ef981-112">**String**.</span></span>

<span data-ttu-id="ef981-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="ef981-113">**Applies To**</span></span>

[<span data-ttu-id="ef981-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="ef981-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="ef981-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="ef981-115">**Tag Syntax**</span></span>

<span data-ttu-id="ef981-116"><v : *Element* o :ConnectorType = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ef981-116"><v: *element* o:connectortype=" *expression* "></span></span>

<span data-ttu-id="ef981-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="ef981-117">**Remarks**</span></span>

<span data-ttu-id="ef981-118">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="ef981-118">Values include:</span></span>



| <span data-ttu-id="ef981-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef981-119">Value</span></span>    | <span data-ttu-id="ef981-120">Description</span><span class="sxs-lookup"><span data-stu-id="ef981-120">Description</span></span>                    |
|----------|--------------------------------|
| <span data-ttu-id="ef981-121">aucun</span><span class="sxs-lookup"><span data-stu-id="ef981-121">none</span></span>     | <span data-ttu-id="ef981-122">Aucun connecteur.</span><span class="sxs-lookup"><span data-stu-id="ef981-122">No connector.</span></span>                  |
| <span data-ttu-id="ef981-123">angles</span><span class="sxs-lookup"><span data-stu-id="ef981-123">straight</span></span> | <span data-ttu-id="ef981-124">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="ef981-124">Default.</span></span> <span data-ttu-id="ef981-125">Connecteur droit.</span><span class="sxs-lookup"><span data-stu-id="ef981-125">A straight connector.</span></span> |
| <span data-ttu-id="ef981-126">coud</span><span class="sxs-lookup"><span data-stu-id="ef981-126">elbow</span></span>    | <span data-ttu-id="ef981-127">Connecteur en forme de coude.</span><span class="sxs-lookup"><span data-stu-id="ef981-127">An elbow-shaped connector.</span></span>     |
| <span data-ttu-id="ef981-128">courbe</span><span class="sxs-lookup"><span data-stu-id="ef981-128">curved</span></span>   | <span data-ttu-id="ef981-129">Connecteur courbé.</span><span class="sxs-lookup"><span data-stu-id="ef981-129">A curved connector.</span></span>            |



 

<span data-ttu-id="ef981-130">Cet attribut peut également être utilisé par un moteur de règles d’un éditeur graphique.</span><span class="sxs-lookup"><span data-stu-id="ef981-130">This attribute may also be used by a rules engine of a graphical editor.</span></span>

<span data-ttu-id="ef981-131">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="ef981-131">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="ef981-132">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="ef981-132">**Example**</span></span>

<span data-ttu-id="ef981-133">La forme utilise une ligne droite comme connecteur.</span><span class="sxs-lookup"><span data-stu-id="ef981-133">The shape uses a straight line as a connector.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 