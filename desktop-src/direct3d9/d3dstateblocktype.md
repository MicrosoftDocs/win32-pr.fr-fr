---
description: Ensembles prédéfinis d’état de pipeline utilisés par les blocs d’État (consultez États de l’enregistrement et de la restauration des blocs d’État (Direct3D 9)).
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: Énumération D3DSTATEBLOCKTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTATEBLOCKTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 03b1834a2bd8e1b5f89922d908a558aa97e58f76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104550616"
---
# <a name="d3dstateblocktype-enumeration"></a><span data-ttu-id="95dba-103">Énumération D3DSTATEBLOCKTYPE</span><span class="sxs-lookup"><span data-stu-id="95dba-103">D3DSTATEBLOCKTYPE enumeration</span></span>

<span data-ttu-id="95dba-104">Ensembles prédéfinis d’état de pipeline utilisés par les blocs d’État (consultez États de l' [enregistrement et de la restauration des blocs d’État (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="95dba-104">Predefined sets of pipeline state used by state blocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="95dba-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95dba-105">Syntax</span></span>


```C++
typedef enum _D3DSTATEBLOCKTYPE { 
  D3DSBT_ALL          = 1,
  D3DSBT_PIXELSTATE   = 2,
  D3DSBT_VERTEXSTATE  = 3,
  D3DSBT_FORCE_DWORD  = 0x7fffffff
} D3DSTATEBLOCKTYPE;
```



## <a name="constants"></a><span data-ttu-id="95dba-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="95dba-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="95dba-107"><span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_ tout**</span><span class="sxs-lookup"><span data-stu-id="95dba-107"><span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="95dba-108">Capturer l’état actuel de l' [appareil](saving-all-device-states-with-a-stateblock.md).</span><span class="sxs-lookup"><span data-stu-id="95dba-108">Capture the current [device state](saving-all-device-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="95dba-109"><span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT \_ PIXELSTATE**</span><span class="sxs-lookup"><span data-stu-id="95dba-109"><span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT\_PIXELSTATE**</span></span>
</dt> <dd>

<span data-ttu-id="95dba-110">Capturer l’état actuel du [Pixel](saving-pixel-states-with-a-stateblock.md).</span><span class="sxs-lookup"><span data-stu-id="95dba-110">Capture the current [pixel state](saving-pixel-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="95dba-111"><span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT \_ VERTEXSTATE**</span><span class="sxs-lookup"><span data-stu-id="95dba-111"><span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT\_VERTEXSTATE**</span></span>
</dt> <dd>

<span data-ttu-id="95dba-112">Capture l’état actuel du [vertex](saving-vertex-states-with-a-stateblock.md).</span><span class="sxs-lookup"><span data-stu-id="95dba-112">Capture the current [vertex state](saving-vertex-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="95dba-113"><span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="95dba-113"><span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="95dba-114">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="95dba-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="95dba-115">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="95dba-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="95dba-116">N’utilisez pas cette valeur.</span><span class="sxs-lookup"><span data-stu-id="95dba-116">Do not use this value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95dba-117">Notes</span><span class="sxs-lookup"><span data-stu-id="95dba-117">Remarks</span></span>

<span data-ttu-id="95dba-118">Comme le montre le diagramme suivant, l’état des vertex et des pixels est à la fois des sous-ensembles de l’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="95dba-118">As the following diagram shows, vertex and pixel state are both subsets of device state.</span></span>

![diagramme de l’état de l’appareil, avec un état de vertex et un état de pixel comme sous-ensembles](images/statesets.png)

<span data-ttu-id="95dba-120">Il n’y a que quelques États qui sont considérés comme l’état des vertex et des pixels.</span><span class="sxs-lookup"><span data-stu-id="95dba-120">There are only a few states that are considered both vertex and pixel state.</span></span> <span data-ttu-id="95dba-121">Ces états sont :</span><span class="sxs-lookup"><span data-stu-id="95dba-121">These states are:</span></span>

-   <span data-ttu-id="95dba-122">État du rendu : D3DRS \_ FOGDENSITY</span><span class="sxs-lookup"><span data-stu-id="95dba-122">Render state: D3DRS\_FOGDENSITY</span></span>
-   <span data-ttu-id="95dba-123">État du rendu : D3DRS \_ FOGSTART</span><span class="sxs-lookup"><span data-stu-id="95dba-123">Render state: D3DRS\_FOGSTART</span></span>
-   <span data-ttu-id="95dba-124">État du rendu : D3DRS \_ FOGEND</span><span class="sxs-lookup"><span data-stu-id="95dba-124">Render state: D3DRS\_FOGEND</span></span>
-   <span data-ttu-id="95dba-125">État de la texture : D3DTSS \_ TEXCOORDINDEX</span><span class="sxs-lookup"><span data-stu-id="95dba-125">Texture state: D3DTSS\_TEXCOORDINDEX</span></span>
-   <span data-ttu-id="95dba-126">État de la texture : D3DTSS \_ TEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="95dba-126">Texture state: D3DTSS\_TEXTURETRANSFORMFLAGS</span></span>

## <a name="requirements"></a><span data-ttu-id="95dba-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95dba-127">Requirements</span></span>



| <span data-ttu-id="95dba-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95dba-128">Requirement</span></span> | <span data-ttu-id="95dba-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="95dba-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95dba-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="95dba-130">Header</span></span><br/> | <dl> <span data-ttu-id="95dba-131"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="95dba-131"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95dba-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95dba-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95dba-133">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="95dba-133">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="95dba-134">**IDirect3DDevice9::CreateStateBlock**</span><span class="sxs-lookup"><span data-stu-id="95dba-134">**IDirect3DDevice9::CreateStateBlock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

<span data-ttu-id="95dba-135">**IDirect3DDevice9::CreateStateBlock**</span><span class="sxs-lookup"><span data-stu-id="95dba-135">**IDirect3DDevice9::CreateStateBlock**</span></span>
</dt> </dl>

 

 
