---
title: Fonction de type de taille (D2d1helper. h)
description: Crée une structure de taille qui stocke sa largeur et sa hauteur à l’aide du type de données spécifié.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Fonction de type de taille Direct2D
topic_type:
- apiref
api_name:
- Size Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a300ab0ce7da57440516733459f703379cf5a943
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465002"
---
# <a name="sizetype-function"></a><span data-ttu-id="d793c-104">Size, <Type> fonction</span><span class="sxs-lookup"><span data-stu-id="d793c-104">Size<Type> Function</span></span>

<span data-ttu-id="d793c-105">Crée une structure de taille qui stocke sa largeur et sa hauteur à l’aide du type de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="d793c-105">Creates a size structure that stores its width and height using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a><span data-ttu-id="d793c-106">Paramètres de modèle</span><span class="sxs-lookup"><span data-stu-id="d793c-106">Template Parameters</span></span>



| <span data-ttu-id="d793c-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d793c-107">Parameter</span></span> | <span data-ttu-id="d793c-108">Description</span><span class="sxs-lookup"><span data-stu-id="d793c-108">Description</span></span>                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d793c-109">Type</span><span class="sxs-lookup"><span data-stu-id="d793c-109">Type</span></span>      | <span data-ttu-id="d793c-110">Type de données utilisé pour stocker la largeur et la hauteur de la taille.</span><span class="sxs-lookup"><span data-stu-id="d793c-110">The data type used to store the width and height of the size.</span></span> <span data-ttu-id="d793c-111">Les valeurs possibles sont FLOAT et UINT32.</span><span class="sxs-lookup"><span data-stu-id="d793c-111">Possible values are FLOAT and UINT32.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="d793c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d793c-112">Parameters</span></span>



| <span data-ttu-id="d793c-113">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d793c-113">Parameter</span></span> | <span data-ttu-id="d793c-114">Description</span><span class="sxs-lookup"><span data-stu-id="d793c-114">Description</span></span>        |
|-----------|--------------------|
| <span data-ttu-id="d793c-115">width</span><span class="sxs-lookup"><span data-stu-id="d793c-115">width</span></span>     | <span data-ttu-id="d793c-116">Largeur de la taille.</span><span class="sxs-lookup"><span data-stu-id="d793c-116">The size's width.</span></span>  |
| <span data-ttu-id="d793c-117">height</span><span class="sxs-lookup"><span data-stu-id="d793c-117">height</span></span>    | <span data-ttu-id="d793c-118">Hauteur de la taille.</span><span class="sxs-lookup"><span data-stu-id="d793c-118">The size's height.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="d793c-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d793c-119">Return Value</span></span>

<span data-ttu-id="d793c-120">Taille qui contient la largeur et la hauteur spécifiées.</span><span class="sxs-lookup"><span data-stu-id="d793c-120">A size that contains the specified width and height.</span></span>

## <a name="requirements"></a><span data-ttu-id="d793c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d793c-121">Requirements</span></span>



| <span data-ttu-id="d793c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d793c-122">Requirement</span></span> | <span data-ttu-id="d793c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d793c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d793c-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d793c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d793c-125">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d793c-125">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="d793c-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d793c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d793c-127">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d793c-127">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d793c-128">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d793c-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="d793c-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="d793c-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="d793c-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="d793c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d793c-131"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="d793c-131"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="d793c-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d793c-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="d793c-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d793c-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="d793c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d793c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d793c-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d793c-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





