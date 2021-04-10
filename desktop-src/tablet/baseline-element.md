---
description: Fournit des informations (x, y) pour les points de départ et de fin de la ligne de base d’un paragraphe dans le document journal. L’espace de coordonnées utilisé pour ces valeurs est HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Élément de ligne de base
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b64986707eaa1b382d2f88851367b9147c59c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201218"
---
# <a name="baseline-element"></a><span data-ttu-id="09c22-104">Élément de ligne de base</span><span class="sxs-lookup"><span data-stu-id="09c22-104">Baseline Element</span></span>

<span data-ttu-id="09c22-105">Fournit des informations (x, y) pour les points de départ et de fin de la ligne de base d’un paragraphe dans le document journal.</span><span class="sxs-lookup"><span data-stu-id="09c22-105">Provides (x, y) information for the starting and ending points of the baseline of a paragraph in the Journal document.</span></span> <span data-ttu-id="09c22-106">L’espace de coordonnées utilisé pour ces valeurs est **HIMETRIC**.</span><span class="sxs-lookup"><span data-stu-id="09c22-106">The coordinate space used for these values is **HIMETRIC**.</span></span>

## <a name="definition"></a><span data-ttu-id="09c22-107">Définition</span><span class="sxs-lookup"><span data-stu-id="09c22-107">Definition</span></span>

``` syntax
<xs:element name="Baseline" type="BaseLineType" />
```

## <a name="parent-elements"></a><span data-ttu-id="09c22-108">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="09c22-108">Parent Elements</span></span>

[<span data-ttu-id="09c22-109">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="09c22-109">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="child-elements"></a><span data-ttu-id="09c22-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="09c22-110">Child Elements</span></span>

<span data-ttu-id="09c22-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="09c22-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="09c22-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="09c22-112">Attributes</span></span>



| <span data-ttu-id="09c22-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="09c22-113">Attribute</span></span>  | <span data-ttu-id="09c22-114">Type</span><span class="sxs-lookup"><span data-stu-id="09c22-114">Type</span></span>                      | <span data-ttu-id="09c22-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="09c22-115">Required</span></span> | <span data-ttu-id="09c22-116">Description</span><span class="sxs-lookup"><span data-stu-id="09c22-116">Description</span></span>                                                      | <span data-ttu-id="09c22-117">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="09c22-117">Possible Values</span></span>           |
|------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="09c22-118">**StartX**</span><span class="sxs-lookup"><span data-stu-id="09c22-118">**StartX**</span></span> | <span data-ttu-id="09c22-119">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="09c22-119">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="09c22-120">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="09c22-120">Required</span></span> | <span data-ttu-id="09c22-121">Valeur X du point marquant le début de la ligne de base.</span><span class="sxs-lookup"><span data-stu-id="09c22-121">The X value for the point marking the beginning of the baseline.</span></span> | <span data-ttu-id="09c22-122">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="09c22-122">Any non-negative integer.</span></span> |
| <span data-ttu-id="09c22-123">**Démarrer**</span><span class="sxs-lookup"><span data-stu-id="09c22-123">**StartY**</span></span> | <span data-ttu-id="09c22-124">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="09c22-124">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="09c22-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="09c22-125">Required</span></span> | <span data-ttu-id="09c22-126">Valeur Y du point marquant le début de la ligne de base.</span><span class="sxs-lookup"><span data-stu-id="09c22-126">The Y value for the point marking the beginning of the baseline.</span></span> | <span data-ttu-id="09c22-127">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="09c22-127">Any non-negative integer.</span></span> |
| <span data-ttu-id="09c22-128">**EndX**</span><span class="sxs-lookup"><span data-stu-id="09c22-128">**EndX**</span></span>   | <span data-ttu-id="09c22-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="09c22-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="09c22-130">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="09c22-130">Required</span></span> | <span data-ttu-id="09c22-131">Valeur X du point marquant la fin de la ligne de base.</span><span class="sxs-lookup"><span data-stu-id="09c22-131">The X value for the point marking the end of the baseline.</span></span>       | <span data-ttu-id="09c22-132">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="09c22-132">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="09c22-133">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="09c22-133">Element Information</span></span>



|              |                                                               |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="09c22-134">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="09c22-134">Element type</span></span> | <span data-ttu-id="09c22-135">ComplexType [**BaselineType**](baselinetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="09c22-135">[**BaselineType**](baselinetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="09c22-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="09c22-136">Namespace</span></span>    | <span data-ttu-id="09c22-137">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="09c22-137">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="09c22-138">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="09c22-138">Schema name</span></span>  | <span data-ttu-id="09c22-139">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="09c22-139">Journal Reader</span></span>                                                |



 

 

 



