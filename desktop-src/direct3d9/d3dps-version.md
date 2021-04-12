---
description: Créez un jeton de version de nuanceur de pixels.
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: Macro D3DPS_VERSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3f30d673145ec9dfe38bd8e2a636ac04c9a195a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322997"
---
# <a name="d3dps_version-macro"></a><span data-ttu-id="5e8af-103">D3DPS la \_ macro de version</span><span class="sxs-lookup"><span data-stu-id="5e8af-103">D3DPS\_VERSION macro</span></span>

<span data-ttu-id="5e8af-104">Créez un jeton de version de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="5e8af-104">Create a pixel shader version token.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e8af-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e8af-105">Syntax</span></span>


```C++
DWORD D3DPS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a><span data-ttu-id="5e8af-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e8af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e8af-107">*\_Majeure*</span><span class="sxs-lookup"><span data-stu-id="5e8af-107">*\_Major*</span></span> 
</dt> <dd>

<span data-ttu-id="5e8af-108">Version du nuanceur de pixels principal.</span><span class="sxs-lookup"><span data-stu-id="5e8af-108">The major pixel shader version.</span></span>

</dd> <dt>

<span data-ttu-id="5e8af-109">*\_Secondaire*</span><span class="sxs-lookup"><span data-stu-id="5e8af-109">*\_Minor*</span></span> 
</dt> <dd>

<span data-ttu-id="5e8af-110">Version mineure du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="5e8af-110">The minor pixel shader version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e8af-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e8af-111">Return value</span></span>

<span data-ttu-id="5e8af-112">Retourne une valeur DWORD qui est une version de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="5e8af-112">Returns a DWORD value that is a pixel shader version.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e8af-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5e8af-113">Remarks</span></span>

<span data-ttu-id="5e8af-114">Numéros de versions</span><span class="sxs-lookup"><span data-stu-id="5e8af-114">Version Numbers</span></span>

<span data-ttu-id="5e8af-115">Le numéro de version est une combinaison de la version principale et des numéros de version de nuanceur de vertex secondaires.</span><span class="sxs-lookup"><span data-stu-id="5e8af-115">The version number is a combination of the major version and the minor vertex shader version numbers.</span></span> <span data-ttu-id="5e8af-116">Les nombres valides sont indiqués dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="5e8af-116">Valid numbers are shown in the table.</span></span>



| <span data-ttu-id="5e8af-117">Majeure</span><span class="sxs-lookup"><span data-stu-id="5e8af-117">Major</span></span> | <span data-ttu-id="5e8af-118">Secondaire</span><span class="sxs-lookup"><span data-stu-id="5e8af-118">Minor</span></span> | <span data-ttu-id="5e8af-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="5e8af-119">Example</span></span>             |
|-------|-------|---------------------|
| <span data-ttu-id="5e8af-120">1</span><span class="sxs-lookup"><span data-stu-id="5e8af-120">1</span></span>     | <span data-ttu-id="5e8af-121">1</span><span class="sxs-lookup"><span data-stu-id="5e8af-121">1</span></span>     | <span data-ttu-id="5e8af-122">\_Version de D3DPS (1, 1)</span><span class="sxs-lookup"><span data-stu-id="5e8af-122">D3DPS\_VERSION(1,1)</span></span> |
| <span data-ttu-id="5e8af-123">1</span><span class="sxs-lookup"><span data-stu-id="5e8af-123">1</span></span>     | <span data-ttu-id="5e8af-124">2</span><span class="sxs-lookup"><span data-stu-id="5e8af-124">2</span></span>     | <span data-ttu-id="5e8af-125">\_Version de D3DPS (1, 2)</span><span class="sxs-lookup"><span data-stu-id="5e8af-125">D3DPS\_VERSION(1,2)</span></span> |
| <span data-ttu-id="5e8af-126">1</span><span class="sxs-lookup"><span data-stu-id="5e8af-126">1</span></span>     | <span data-ttu-id="5e8af-127">3</span><span class="sxs-lookup"><span data-stu-id="5e8af-127">3</span></span>     | <span data-ttu-id="5e8af-128">\_Version de D3DPS (1, 3)</span><span class="sxs-lookup"><span data-stu-id="5e8af-128">D3DPS\_VERSION(1,3)</span></span> |
| <span data-ttu-id="5e8af-129">1</span><span class="sxs-lookup"><span data-stu-id="5e8af-129">1</span></span>     | <span data-ttu-id="5e8af-130">4</span><span class="sxs-lookup"><span data-stu-id="5e8af-130">4</span></span>     | <span data-ttu-id="5e8af-131">\_Version de D3DPS (1,4)</span><span class="sxs-lookup"><span data-stu-id="5e8af-131">D3DPS\_VERSION(1,4)</span></span> |
| <span data-ttu-id="5e8af-132">2</span><span class="sxs-lookup"><span data-stu-id="5e8af-132">2</span></span>     | <span data-ttu-id="5e8af-133">0</span><span class="sxs-lookup"><span data-stu-id="5e8af-133">0</span></span>     | <span data-ttu-id="5e8af-134">\_Version de D3DPS (2, 0)</span><span class="sxs-lookup"><span data-stu-id="5e8af-134">D3DPS\_VERSION(2,0)</span></span> |
| <span data-ttu-id="5e8af-135">3</span><span class="sxs-lookup"><span data-stu-id="5e8af-135">3</span></span>     | <span data-ttu-id="5e8af-136">0</span><span class="sxs-lookup"><span data-stu-id="5e8af-136">0</span></span>     | <span data-ttu-id="5e8af-137">\_Version de D3DPS (3, 0)</span><span class="sxs-lookup"><span data-stu-id="5e8af-137">D3DPS\_VERSION(3,0)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="5e8af-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e8af-138">Requirements</span></span>



| <span data-ttu-id="5e8af-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e8af-139">Requirement</span></span> | <span data-ttu-id="5e8af-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e8af-140">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e8af-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e8af-141">Header</span></span><br/> | <dl> <span data-ttu-id="5e8af-142"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e8af-142"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e8af-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e8af-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e8af-144">Macros</span><span class="sxs-lookup"><span data-stu-id="5e8af-144">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="5e8af-145">D3DCAPS9</span><span class="sxs-lookup"><span data-stu-id="5e8af-145">D3DCAPS9</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




