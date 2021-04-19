---
description: L’analyse de la disposition opère sur une collection de traits et classe les traits en éléments d’écriture manuscrite et de dessin. L’objet diviseur fournit l’accès aux fonctionnalités d’analyse de la disposition du Tablet PC.
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: Analyse de la disposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0901e7c7df96bec5ea3972f643469033fbb22ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518320"
---
# <a name="layout-analysis"></a><span data-ttu-id="4c67d-104">Analyse de la disposition</span><span class="sxs-lookup"><span data-stu-id="4c67d-104">Layout Analysis</span></span>

<span data-ttu-id="4c67d-105">L’analyse de la disposition opère sur une collection de [**traits**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) et classe les traits en éléments d’écriture manuscrite et de dessin.</span><span class="sxs-lookup"><span data-stu-id="4c67d-105">Layout analysis operates on a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection and classifies the strokes into handwriting and drawing elements.</span></span> <span data-ttu-id="4c67d-106">L’objet [**diviseur**](inkdivider-class.md) fournit l’accès aux fonctionnalités d’analyse de la disposition du Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="4c67d-106">The [**Divider**](inkdivider-class.md) object provides access to the Tablet PC layout analysis features.</span></span>

<span data-ttu-id="4c67d-107">Le tableau suivant décrit les types d’éléments structurels de l’énumération [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) dans lesquels l’objet [**diviseur**](inkdivider-class.md) classifie les traits.</span><span class="sxs-lookup"><span data-stu-id="4c67d-107">The following table describes the structural element types of the [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) enumeration into which the [**Divider**](inkdivider-class.md) object classifies strokes.</span></span>



| <span data-ttu-id="4c67d-108">Type</span><span class="sxs-lookup"><span data-stu-id="4c67d-108">Type</span></span>          | <span data-ttu-id="4c67d-109">Description</span><span class="sxs-lookup"><span data-stu-id="4c67d-109">Description</span></span>                                                                      |
|---------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4c67d-110">**Segment**</span><span class="sxs-lookup"><span data-stu-id="4c67d-110">**Segment**</span></span>   | <span data-ttu-id="4c67d-111">Un segment de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="4c67d-111">A recognition segment.</span></span><br/>                                                |
| <span data-ttu-id="4c67d-112">**Ligne**</span><span class="sxs-lookup"><span data-stu-id="4c67d-112">**Line**</span></span>      | <span data-ttu-id="4c67d-113">Ligne d’écriture manuscrite qui contient un ou plusieurs segments de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="4c67d-113">A line of handwriting that contains one or more recognition segments.</span></span><br/> |
| <span data-ttu-id="4c67d-114">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="4c67d-114">**Paragraph**</span></span> | <span data-ttu-id="4c67d-115">Bloc de traits qui contient une ou plusieurs lignes d’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="4c67d-115">A block of strokes that contains one or more lines of handwriting.</span></span><br/>    |
| <span data-ttu-id="4c67d-116">**Schéma**</span><span class="sxs-lookup"><span data-stu-id="4c67d-116">**Drawing**</span></span>   | <span data-ttu-id="4c67d-117">Entrée manuscrite qui n’est pas une écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="4c67d-117">Ink that is not handwriting.</span></span><br/>                                          |



 

<span data-ttu-id="4c67d-118">L’objet [**diviseur**](inkdivider-class.md) possède une collection [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , que l’objet **diviseur** analyse dynamiquement chaque fois que vous ajoutez ou supprimez la collection.</span><span class="sxs-lookup"><span data-stu-id="4c67d-118">The [**Divider**](inkdivider-class.md) object has a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection, which the **Divider** object dynamically analyzes each time you add to or delete from the collection.</span></span> <span data-ttu-id="4c67d-119">L’objet de **séparateur** n’est pas sérialisable, et vous ne pouvez pas enregistrer son état d’analyse.</span><span class="sxs-lookup"><span data-stu-id="4c67d-119">The **Divider** object is not serializable, and you cannot save its analysis state.</span></span> <span data-ttu-id="4c67d-120">Par conséquent, l’objet **diviseur** est conçu pour les applications qui doivent faire la différence entre l’écriture de texte mixte et l’entrée de dessin, mais n’ont pas besoin de réanalyser de grandes quantités d’encre entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="4c67d-120">Thus the **Divider** object is designed for applications that must differentiate between mixed handwriting and drawing input, but do not need to reanalyze large amounts of ink between sessions.</span></span>

<span data-ttu-id="4c67d-121">Vous pouvez obtenir un instantané statique du résultat de l’analyse actuelle, qui est retourné dans un objet [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="4c67d-121">You can obtain a static snapshot of the current analysis result, which is returned in a [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span> <span data-ttu-id="4c67d-122">Vous pouvez obtenir des objets [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) , chacun représentant un élément structurel unique d’un objet **DivisionResult** .</span><span class="sxs-lookup"><span data-stu-id="4c67d-122">You can obtain [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) objects, each which represents a single structural element of a **DivisionResult** object.</span></span> <span data-ttu-id="4c67d-123">Les objets **DivisionResult** et **DivisionUnit** ne sont pas sérialisables.</span><span class="sxs-lookup"><span data-stu-id="4c67d-123">The **DivisionResult** and **DivisionUnit** objects are not serializable.</span></span> <span data-ttu-id="4c67d-124">Toutefois, les informations d’état de ces objets sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="4c67d-124">However, state information from these objects is available.</span></span>

<span data-ttu-id="4c67d-125">L’objet [**diviseur**](inkdivider-class.md) fonctionne uniquement avec l’écriture manuscrite de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="4c67d-125">The [**Divider**](inkdivider-class.md) object works only with left-to-right handwriting.</span></span> <span data-ttu-id="4c67d-126">Pour que l’objet **diviseur** analyse les langues verticales telles que le chinois correctement, les caractères doivent être dessinés de gauche à droite et de haut en bas.</span><span class="sxs-lookup"><span data-stu-id="4c67d-126">For the **Divider** object to analyze vertical languages such as Chinese correctly, the characters must be drawn left-to-right instead of top-to-bottom.</span></span>

 

