---
title: 'Texture2DMSArray :: Load (int, int, int, uint), fonction'
description: 'Lit les données de texture et retourne l’état de l’opération. | Texture2DMSArray :: Load (int, int, int, uint), fonction'
ms.assetid: F5EA2FFF-7E43-4A34-9358-EA54382641DC
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
ms.openlocfilehash: 0065ee5e420c67876b87c67be1f5e5c8ff10e65b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991897"
---
# <a name="texture2dmsarrayloadintintintuint-function"></a><span data-ttu-id="c14ac-105">Texture2DMSArray :: Load (int, int, int, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="c14ac-105">Texture2DMSArray::Load(int,int,int,uint) function</span></span>

<span data-ttu-id="c14ac-106">Lit les données de texture et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c14ac-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c14ac-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c14ac-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  sampleindex,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="c14ac-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c14ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c14ac-109">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c14ac-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c14ac-110">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="c14ac-110">Type: **int**</span></span>

<span data-ttu-id="c14ac-111">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="c14ac-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="c14ac-112">*sampleindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c14ac-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c14ac-113">Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c14ac-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c14ac-114">Exemple d’index.</span><span class="sxs-lookup"><span data-stu-id="c14ac-114">The sample index.</span></span>

</dd> <dt>

<span data-ttu-id="c14ac-115">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c14ac-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c14ac-116">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="c14ac-116">Type: **int**</span></span>

<span data-ttu-id="c14ac-117">Décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="c14ac-117">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c14ac-118">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c14ac-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c14ac-119">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="c14ac-119">Type: **uint**</span></span>

<span data-ttu-id="c14ac-120">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c14ac-120">The status of the operation.</span></span> <span data-ttu-id="c14ac-121">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="c14ac-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c14ac-122">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="c14ac-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c14ac-123">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="c14ac-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c14ac-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c14ac-124">Return value</span></span>

<span data-ttu-id="c14ac-125">Tapez :</span><span class="sxs-lookup"><span data-stu-id="c14ac-125">Type:</span></span>

<span data-ttu-id="c14ac-126">Le type de retour correspond au type dans la déclaration pour l’objet [**Texture2DMSArray**](sm5-object-texture2dmsarray.md) .</span><span class="sxs-lookup"><span data-stu-id="c14ac-126">The return type matches the type in the declaration for the [**Texture2DMSArray**](sm5-object-texture2dmsarray.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="c14ac-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c14ac-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c14ac-128">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="c14ac-128">Load methods</span></span>](texture2dmsarray-load.md)
</dt> <dt>

[<span data-ttu-id="c14ac-129">**Texture2DMSArray**</span><span class="sxs-lookup"><span data-stu-id="c14ac-129">**Texture2DMSArray**</span></span>](sm5-object-texture2dmsarray.md)
</dt> </dl>

 

 
