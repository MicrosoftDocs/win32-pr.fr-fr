---
description: Contient le niveau de confiance retourné par l’analyseur d’encre journal pour le InkWord.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Élément confidence
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cef4869776a6cafc4e6ef4758649b918e0b5988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112015"
---
# <a name="confidence-element"></a><span data-ttu-id="a748c-103">Élément confidence</span><span class="sxs-lookup"><span data-stu-id="a748c-103">Confidence Element</span></span>

<span data-ttu-id="a748c-104">Contient le niveau de confiance retourné par l’analyseur d’encre journal pour le [**InkWord**](inkword-element.md).</span><span class="sxs-lookup"><span data-stu-id="a748c-104">Contains the confidence rating returned by the Journal ink analyzer for the [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="a748c-105">Définition</span><span class="sxs-lookup"><span data-stu-id="a748c-105">Definition</span></span>

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="a748c-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a748c-106">Parent Elements</span></span>

[<span data-ttu-id="a748c-107">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="a748c-107">**InkWord**</span></span>](inkword-element.md)

## <a name="values"></a><span data-ttu-id="a748c-108">Valeurs</span><span class="sxs-lookup"><span data-stu-id="a748c-108">Values</span></span>

<span data-ttu-id="a748c-109">Les valeurs valides pour ce champ sont « 0 », « 1 » et « 2 ».</span><span class="sxs-lookup"><span data-stu-id="a748c-109">Valid values for this field include "0", "1", and "2".</span></span> <span data-ttu-id="a748c-110">0 indique une confiance forte, 1 indique une confiance intermédiaire et 2 indique une confiance médiocre.</span><span class="sxs-lookup"><span data-stu-id="a748c-110">0 indicates Strong confidence, 1 indicates Intermediate confidence, and 2 indicates Poor confidence.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a748c-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a748c-111">Child Elements</span></span>

<span data-ttu-id="a748c-112">Aucun</span><span class="sxs-lookup"><span data-stu-id="a748c-112">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="a748c-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="a748c-113">Attributes</span></span>

<span data-ttu-id="a748c-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="a748c-114">None.</span></span>

## <a name="element-information"></a><span data-ttu-id="a748c-115">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a748c-115">Element Information</span></span>



|              |                                            |
|--------------|--------------------------------------------|
| <span data-ttu-id="a748c-116">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="a748c-116">Element type</span></span> | <span data-ttu-id="a748c-117">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="a748c-117">**xs:string**</span></span>                              |
| <span data-ttu-id="a748c-118">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a748c-118">Namespace</span></span>    | <span data-ttu-id="a748c-119">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="a748c-119">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="a748c-120">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="a748c-120">Schema name</span></span>  | <span data-ttu-id="a748c-121">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="a748c-121">Journal Reader</span></span>                             |



 

 

 



