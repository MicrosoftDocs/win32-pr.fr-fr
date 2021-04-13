---
title: 'Texture2DMS :: Load (int, int, int, uint), fonction'
description: 'Lit les données de texture et retourne l’état de l’opération. | Texture2DMS :: Load (int, int, int, uint), fonction'
ms.assetid: 4230962C-2968-4030-9770-8318F1760AEB
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
ms.openlocfilehash: e967d69929c0b20317ffb74fc97c4e60e36c2854
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321805"
---
# <a name="texture2dmsloadintintintuint-function"></a><span data-ttu-id="18293-105">Texture2DMS :: Load (int, int, int, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="18293-105">Texture2DMS::Load(int,int,int,uint) function</span></span>

<span data-ttu-id="18293-106">Lit les données de texture et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="18293-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="18293-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18293-107">Syntax</span></span>


``` syntax
 Load(
  in  int2 Location,
  in  int  sampleindex,
  in  int2 Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="18293-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18293-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18293-109">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18293-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18293-110">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="18293-110">Type: **int2**</span></span>

<span data-ttu-id="18293-111">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="18293-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="18293-112">*sampleindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18293-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18293-113">Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="18293-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="18293-114">Exemple d’index.</span><span class="sxs-lookup"><span data-stu-id="18293-114">The sample index.</span></span>

</dd> <dt>

<span data-ttu-id="18293-115">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18293-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18293-116">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="18293-116">Type: **int2**</span></span>

<span data-ttu-id="18293-117">Décalage appliqué aux coordonnées de texture avant le chargement.</span><span class="sxs-lookup"><span data-stu-id="18293-117">An offset applied to the texture coordinates before loading.</span></span>

</dd> <dt>

<span data-ttu-id="18293-118">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="18293-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18293-119">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="18293-119">Type: **uint**</span></span>

<span data-ttu-id="18293-120">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="18293-120">The status of the operation.</span></span> <span data-ttu-id="18293-121">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="18293-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="18293-122">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="18293-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="18293-123">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="18293-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18293-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18293-124">Return value</span></span>

<span data-ttu-id="18293-125">Tapez :</span><span class="sxs-lookup"><span data-stu-id="18293-125">Type:</span></span>

<span data-ttu-id="18293-126">Le type de retour correspond au type dans la déclaration pour l’objet [**Texture2DMS**](sm5-object-texture2dms.md) .</span><span class="sxs-lookup"><span data-stu-id="18293-126">The return type matches the type in the declaration for the [**Texture2DMS**](sm5-object-texture2dms.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="18293-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18293-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18293-128">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="18293-128">Load methods</span></span>](texture2dms-load.md)
</dt> <dt>

[<span data-ttu-id="18293-129">**Texture2DMS**</span><span class="sxs-lookup"><span data-stu-id="18293-129">**Texture2DMS**</span></span>](sm5-object-texture2dms.md)
</dt> </dl>

 

 
