---
title: Fonction de type Rect (D2d1helper. h)
description: Crée une structure rectangle qui stocke ses coordonnées à l’aide du type de données spécifié.
ms.assetid: b152efaf-0779-4024-b998-82a347abba71
keywords:
- Fonction de type Rect Direct2D
topic_type:
- apiref
api_name:
- Rect Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ed16ecd5a79c73ecb7341b9aa7f3378854dd4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511160"
---
# <a name="recttype-function"></a><span data-ttu-id="a7291-104">Rect, <Type> fonction</span><span class="sxs-lookup"><span data-stu-id="a7291-104">Rect<Type> Function</span></span>

<span data-ttu-id="a7291-105">Crée une structure rectangle qui stocke ses coordonnées à l’aide du type de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="a7291-105">Creates a rectangle structure that stores its coordinates using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Rect Rect(
  Type left,
  Type top,
  Type right,
  Type bottom
);
```

## <a name="template-parameters"></a><span data-ttu-id="a7291-106">Paramètres de modèle</span><span class="sxs-lookup"><span data-stu-id="a7291-106">Template Parameters</span></span>



| <span data-ttu-id="a7291-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a7291-107">Parameter</span></span> | <span data-ttu-id="a7291-108">Description</span><span class="sxs-lookup"><span data-stu-id="a7291-108">Description</span></span>                                                                                                |
|-----------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7291-109">Type</span><span class="sxs-lookup"><span data-stu-id="a7291-109">Type</span></span>      | <span data-ttu-id="a7291-110">Type de données utilisé pour stocker les dimensions du rectangle.</span><span class="sxs-lookup"><span data-stu-id="a7291-110">The data type used to store the dimensions of the rectangle.</span></span> <span data-ttu-id="a7291-111">Les valeurs possibles sont **float** et **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="a7291-111">Possible values are **FLOAT** and **UINT32**.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="a7291-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7291-112">Parameters</span></span>



| <span data-ttu-id="a7291-113">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a7291-113">Parameter</span></span> | <span data-ttu-id="a7291-114">Description</span><span class="sxs-lookup"><span data-stu-id="a7291-114">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="a7291-115">gauche</span><span class="sxs-lookup"><span data-stu-id="a7291-115">left</span></span>      | <span data-ttu-id="a7291-116">Coordonnée x de l’angle supérieur gauche du rectangle.</span><span class="sxs-lookup"><span data-stu-id="a7291-116">The x-coordinate of the rectangle's upper-left corner.</span></span>  |
| <span data-ttu-id="a7291-117">top</span><span class="sxs-lookup"><span data-stu-id="a7291-117">top</span></span>       | <span data-ttu-id="a7291-118">Coordonnée y de l’angle supérieur gauche du rectangle.</span><span class="sxs-lookup"><span data-stu-id="a7291-118">The y-coordinate of the rectangle's upper-left corner.</span></span>  |
| <span data-ttu-id="a7291-119">droite</span><span class="sxs-lookup"><span data-stu-id="a7291-119">right</span></span>     | <span data-ttu-id="a7291-120">Coordonnée x du coin inférieur droit du rectangle.</span><span class="sxs-lookup"><span data-stu-id="a7291-120">The x-coordinate of the rectangle's lower-right corner.</span></span> |
| <span data-ttu-id="a7291-121">bottom</span><span class="sxs-lookup"><span data-stu-id="a7291-121">bottom</span></span>    | <span data-ttu-id="a7291-122">Coordonnée y du coin inférieur droit du rectangle.</span><span class="sxs-lookup"><span data-stu-id="a7291-122">The y-coordinate of the rectangle's lower-right corner.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="a7291-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a7291-123">Return Value</span></span>

<span data-ttu-id="a7291-124">Structure rectangle qui contient les coordonnées spécifiées.</span><span class="sxs-lookup"><span data-stu-id="a7291-124">A rectangle structure that contains the specified coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7291-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7291-125">Requirements</span></span>



| <span data-ttu-id="a7291-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7291-126">Requirement</span></span> | <span data-ttu-id="a7291-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7291-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7291-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7291-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a7291-129">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a7291-129">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="a7291-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7291-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a7291-131">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a7291-131">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a7291-132">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7291-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="a7291-133">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="a7291-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="a7291-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7291-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7291-135"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7291-135"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="a7291-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a7291-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="a7291-137"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7291-137"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="a7291-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a7291-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7291-139"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7291-139"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





