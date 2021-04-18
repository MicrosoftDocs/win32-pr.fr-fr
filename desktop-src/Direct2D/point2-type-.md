---
title: Fonction de type point2 (D2d1helper. h)
description: Crée un point qui stocke ses coordonnées à l’aide du type de données spécifié.
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Fonction de type point2 Direct2D
topic_type:
- apiref
api_name:
- Point2 Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f614f49077ed198c5e85d17b9ee3c84a5e300670
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512591"
---
# <a name="point2type-function"></a><span data-ttu-id="c70d1-104">Point2, <Type> fonction</span><span class="sxs-lookup"><span data-stu-id="c70d1-104">Point2<Type> Function</span></span>

<span data-ttu-id="c70d1-105">Crée un point qui stocke ses coordonnées à l’aide du type de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="c70d1-105">Creates a point that stores its coordinates using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Point Point2(
  Type x,
  Type y
);
```

## <a name="template-parameters"></a><span data-ttu-id="c70d1-106">Paramètres de modèle</span><span class="sxs-lookup"><span data-stu-id="c70d1-106">Template Parameters</span></span>



| <span data-ttu-id="c70d1-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c70d1-107">Parameter</span></span> | <span data-ttu-id="c70d1-108">Description</span><span class="sxs-lookup"><span data-stu-id="c70d1-108">Description</span></span>                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c70d1-109">Type</span><span class="sxs-lookup"><span data-stu-id="c70d1-109">Type</span></span>      | <span data-ttu-id="c70d1-110">Type de données utilisé pour stocker les coordonnées x et y du point.</span><span class="sxs-lookup"><span data-stu-id="c70d1-110">The data type used to store the x-coordinate and y-coordinate of the point.</span></span> <span data-ttu-id="c70d1-111">Les valeurs possibles sont FLOAT et UINT32.</span><span class="sxs-lookup"><span data-stu-id="c70d1-111">Possible values are FLOAT and UINT32.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="c70d1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c70d1-112">Parameters</span></span>



| <span data-ttu-id="c70d1-113">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c70d1-113">Parameter</span></span> | <span data-ttu-id="c70d1-114">Description</span><span class="sxs-lookup"><span data-stu-id="c70d1-114">Description</span></span>                    |
|-----------|--------------------------------|
| <span data-ttu-id="c70d1-115">x</span><span class="sxs-lookup"><span data-stu-id="c70d1-115">x</span></span>         | <span data-ttu-id="c70d1-116">Coordonnée X du point.</span><span class="sxs-lookup"><span data-stu-id="c70d1-116">The x-coordinate of the point.</span></span> |
| <span data-ttu-id="c70d1-117">y</span><span class="sxs-lookup"><span data-stu-id="c70d1-117">y</span></span>         | <span data-ttu-id="c70d1-118">Coordonnée Y du point.</span><span class="sxs-lookup"><span data-stu-id="c70d1-118">The y-coordinate of the point.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="c70d1-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c70d1-119">Return Value</span></span>

<span data-ttu-id="c70d1-120">Point qui contient les coordonnées x et y spécifiées.</span><span class="sxs-lookup"><span data-stu-id="c70d1-120">A point that contains the specified x-coordinate and y-coordinate.</span></span>

## <a name="requirements"></a><span data-ttu-id="c70d1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c70d1-121">Requirements</span></span>



| <span data-ttu-id="c70d1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c70d1-122">Requirement</span></span> | <span data-ttu-id="c70d1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c70d1-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c70d1-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c70d1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c70d1-125">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c70d1-125">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="c70d1-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c70d1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c70d1-127">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c70d1-127">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="c70d1-128">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c70d1-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="c70d1-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="c70d1-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="c70d1-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="c70d1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c70d1-131"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="c70d1-131"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="c70d1-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c70d1-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="c70d1-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c70d1-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="c70d1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c70d1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c70d1-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c70d1-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





