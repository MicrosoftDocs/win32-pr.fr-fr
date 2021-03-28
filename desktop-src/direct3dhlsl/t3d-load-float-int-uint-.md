---
title: 'Texture3D :: Load (int, int, uint), fonction'
description: 'Lit les données de texture et retourne l’état de l’opération. | Texture3D :: Load (int, int, uint), fonction'
ms.assetid: 3F562ADB-225F-462B-A7AC-40797BBB632A
keywords:
- Charger la fonction HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19522fe60567e55565265ce0c8b5051c7bf7ccdd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991885"
---
# <a name="texture3dloadintintuint-function"></a><span data-ttu-id="e50ad-105">Texture3D :: Load (int, int, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="e50ad-105">Texture3D::Load(int,int,uint) function</span></span>

<span data-ttu-id="e50ad-106">Lit les données de texture et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e50ad-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e50ad-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e50ad-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="e50ad-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e50ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e50ad-109">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e50ad-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e50ad-110">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="e50ad-110">Type: **int**</span></span>

<span data-ttu-id="e50ad-111">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="e50ad-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="e50ad-112">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e50ad-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e50ad-113">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="e50ad-113">Type: **int**</span></span>

<span data-ttu-id="e50ad-114">Décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="e50ad-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e50ad-115">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e50ad-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e50ad-116">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="e50ad-116">Type: **uint**</span></span>

<span data-ttu-id="e50ad-117">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e50ad-117">The status of the operation.</span></span> <span data-ttu-id="e50ad-118">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="e50ad-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e50ad-119">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="e50ad-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e50ad-120">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="e50ad-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e50ad-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e50ad-121">Return value</span></span>

<span data-ttu-id="e50ad-122">Tapez :</span><span class="sxs-lookup"><span data-stu-id="e50ad-122">Type:</span></span>

<span data-ttu-id="e50ad-123">Le type de retour correspond au type dans la déclaration pour l’objet [**Texture3D**](sm5-object-texture3d.md) .</span><span class="sxs-lookup"><span data-stu-id="e50ad-123">The return type matches the type in the declaration for the [**Texture3D**](sm5-object-texture3d.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="e50ad-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e50ad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e50ad-125">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="e50ad-125">Load methods</span></span>](texture3d-load.md)
</dt> <dt>

[<span data-ttu-id="e50ad-126">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="e50ad-126">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
