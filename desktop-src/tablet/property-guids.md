---
description: Les Microsoft Recognizers utilisent les GUID suivants.
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: GUID de propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2eb089a9b3b5c7863f2d57d9a635b9ab042ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115911"
---
# <a name="property-guids"></a><span data-ttu-id="05304-103">GUID de propriété</span><span class="sxs-lookup"><span data-stu-id="05304-103">Property GUIDs</span></span>

<span data-ttu-id="05304-104">Les Microsoft Recognizers utilisent les GUID suivants.</span><span class="sxs-lookup"><span data-stu-id="05304-104">The Microsoft recognizers use the following GUIDs.</span></span> <span data-ttu-id="05304-105">Chaque fois que cela est possible, les applications doivent utiliser ces GUID.</span><span class="sxs-lookup"><span data-stu-id="05304-105">Whenever possible, applications should use these GUIDs.</span></span> <span data-ttu-id="05304-106">Toutefois, il est prévu et encouragé par d’autres programmeurs à utiliser des GUID supplémentaires pour les propriétés qui ne sont pas prises en charge par les Microsoft Recognizers.</span><span class="sxs-lookup"><span data-stu-id="05304-106">However, it is expected and encouraged that other recognizers will use additional GUIDs for properties that are not supported by the Microsoft recognizers.</span></span>

<span data-ttu-id="05304-107">Toutes les fonctions de propriété ont été développées en sachant que la liste des GUID peut être étendue par d’autres module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="05304-107">All property functions have been developed with the understanding that the list of GUIDs may be extended by other recognizers.</span></span> <span data-ttu-id="05304-108">Ces fonctions de propriété sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="05304-108">These property functions include:</span></span>

-   [<span data-ttu-id="05304-109">**GetContextPropertyList fonction)**</span><span class="sxs-lookup"><span data-stu-id="05304-109">**GetContextPropertyList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [<span data-ttu-id="05304-110">**GetContextPropertyValue fonction)**</span><span class="sxs-lookup"><span data-stu-id="05304-110">**GetContextPropertyValue Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [<span data-ttu-id="05304-111">**GetResultPropertyList fonction)**</span><span class="sxs-lookup"><span data-stu-id="05304-111">**GetResultPropertyList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [<span data-ttu-id="05304-112">**SetContextPropertyValue fonction)**</span><span class="sxs-lookup"><span data-stu-id="05304-112">**SetContextPropertyValue Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

<span data-ttu-id="05304-113">Le tableau suivant répertorie les GUID des propriétés des Tablet PC définis dans msinkaut. h (installés dans c : \\ Program Files \\ Microsoft Tablet PC Platform SDK \\ include par défaut).</span><span class="sxs-lookup"><span data-stu-id="05304-113">The following table lists Tablet PC property GUIDs defined in msinkaut.h (installed in c:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include by default).</span></span>



| <span data-ttu-id="05304-114">GUID</span><span class="sxs-lookup"><span data-stu-id="05304-114">GUID</span></span>                                                  | <span data-ttu-id="05304-115">Définition</span><span class="sxs-lookup"><span data-stu-id="05304-115">Definition</span></span>                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="05304-116">INKRECOGNITIONPROPERTY \_ BOXNUMBER</span><span class="sxs-lookup"><span data-stu-id="05304-116">INKRECOGNITIONPROPERTY\_BOXNUMBER</span></span><br/>          | <span data-ttu-id="05304-117">Index de la boîte alternative du module de reconnaissance en mode zone</span><span class="sxs-lookup"><span data-stu-id="05304-117">The recognizer alternate box index in box mode</span></span><br/>                                    |
| <span data-ttu-id="05304-118">INKRECOGNITIONPROPERTY \_ LINENUMBER</span><span class="sxs-lookup"><span data-stu-id="05304-118">INKRECOGNITIONPROPERTY\_LINENUMBER</span></span><br/>         | <span data-ttu-id="05304-119">Numéro de ligne</span><span class="sxs-lookup"><span data-stu-id="05304-119">The line number</span></span><br/>                                                                   |
| <span data-ttu-id="05304-120">\_segmentation INKRECOGNITIONPROPERTY</span><span class="sxs-lookup"><span data-stu-id="05304-120">INKRECOGNITIONPROPERTY\_SEGMENTATION</span></span><br/>       | <span data-ttu-id="05304-121">Comment le module de reconnaissance segmente les mots et les caractères</span><span class="sxs-lookup"><span data-stu-id="05304-121">How the recognizer segments words and characters</span></span><br/>                                  |
| <span data-ttu-id="05304-122">INKRECOGNITIONPROPERTY \_ HOTPOINT</span><span class="sxs-lookup"><span data-stu-id="05304-122">INKRECOGNITIONPROPERTY\_HOTPOINT</span></span><br/>           | <span data-ttu-id="05304-123">Point réactif du geste</span><span class="sxs-lookup"><span data-stu-id="05304-123">The gesture hot point</span></span><br/>                                                             |
| <span data-ttu-id="05304-124">INKRECOGNITIONPROPERTY \_ MAXIMUMSTROKECOUNT</span><span class="sxs-lookup"><span data-stu-id="05304-124">INKRECOGNITIONPROPERTY\_MAXIMUMSTROKECOUNT</span></span><br/> | <span data-ttu-id="05304-125">Nombre maximal de traits pour un segment</span><span class="sxs-lookup"><span data-stu-id="05304-125">Maximum number of strokes for a segment</span></span><br/>                                           |
| <span data-ttu-id="05304-126">INKRECOGNITIONPROPERTY \_ POINTSPERINCH</span><span class="sxs-lookup"><span data-stu-id="05304-126">INKRECOGNITIONPROPERTY\_POINTSPERINCH</span></span><br/>      | <span data-ttu-id="05304-127">Métrique point par pouce</span><span class="sxs-lookup"><span data-stu-id="05304-127">The points-per-inch metric</span></span><br/>                                                        |
| <span data-ttu-id="05304-128">INKRECOGNITIONPROPERTY \_ CONFIDENCELEVEL</span><span class="sxs-lookup"><span data-stu-id="05304-128">INKRECOGNITIONPROPERTY\_CONFIDENCELEVEL</span></span><br/>    | <span data-ttu-id="05304-129">[**Confiance \_**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) Énumération de niveau</span><span class="sxs-lookup"><span data-stu-id="05304-129">[**CONFIDENCE\_LEVEL**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) enumeration</span></span><br/>                         |
| <span data-ttu-id="05304-130">INKRECOGNITIONPROPERTY \_ LINEMETRICS</span><span class="sxs-lookup"><span data-stu-id="05304-130">INKRECOGNITIONPROPERTY\_LINEMETRICS</span></span><br/>        | <span data-ttu-id="05304-131">Informations pour le calcul de la ligne de base, de la ligne médiane ou des deux, utilisée dans le treillis</span><span class="sxs-lookup"><span data-stu-id="05304-131">Information for computing baseline, midline, or both, that is used in the lattice</span></span><br/> |



 

 

 




