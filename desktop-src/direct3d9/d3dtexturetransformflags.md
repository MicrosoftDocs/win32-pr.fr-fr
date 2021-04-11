---
description: Définit les valeurs de transformation de la coordonnée de texture.
ms.assetid: a91f33ce-2db5-437a-ac29-402b26b0d4e1
title: Énumération D3DTEXTURETRANSFORMFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURETRANSFORMFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 63426c0d57dee02823ee2f37327ba7c66d421b24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211703"
---
# <a name="d3dtexturetransformflags-enumeration"></a><span data-ttu-id="3cecc-103">Énumération D3DTEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="3cecc-103">D3DTEXTURETRANSFORMFLAGS enumeration</span></span>

<span data-ttu-id="3cecc-104">Définit les valeurs de transformation de la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="3cecc-104">Defines texture coordinate transformation values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cecc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cecc-105">Syntax</span></span>


```C++
typedef enum D3DTEXTURETRANSFORMFLAGS { 
  D3DTTFF_DISABLE      = 0,
  D3DTTFF_COUNT1       = 1,
  D3DTTFF_COUNT2       = 2,
  D3DTTFF_COUNT3       = 3,
  D3DTTFF_COUNT4       = 4,
  D3DTTFF_PROJECTED    = 256,
  D3DTTFF_FORCE_DWORD  = 0x7fffffff
} D3DTEXTURETRANSFORMFLAGS, *LPD3DTEXTURETRANSFORMFLAGS;
```



## <a name="constants"></a><span data-ttu-id="3cecc-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="3cecc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3cecc-107"><span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**Désactivation de D3DTTFF \_**</span><span class="sxs-lookup"><span data-stu-id="3cecc-107"><span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**D3DTTFF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="3cecc-108">Les coordonnées de texture sont passées directement au rastériseur.</span><span class="sxs-lookup"><span data-stu-id="3cecc-108">Texture coordinates are passed directly to the rasterizer.</span></span>

</dd> <dt>

<span data-ttu-id="3cecc-109"><span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF \_ COUNT1**</span><span class="sxs-lookup"><span data-stu-id="3cecc-109"><span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF\_COUNT1**</span></span>
</dt> <dd>

<span data-ttu-id="3cecc-110">Le rastériseur doit s’attendre à des coordonnées de texture 1D.</span><span class="sxs-lookup"><span data-stu-id="3cecc-110">The rasterizer should expect 1D texture coordinates.</span></span> <span data-ttu-id="3cecc-111">Cette valeur est utilisée par le traitement du vertex de fonction fixe. elle doit être définie sur 0 lors de l’utilisation d’un nuanceur de sommet programmable.</span><span class="sxs-lookup"><span data-stu-id="3cecc-111">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="3cecc-112"><span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF \_ COUNT2**</span><span class="sxs-lookup"><span data-stu-id="3cecc-112"><span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF\_COUNT2**</span></span>
</dt> <dd>

<span data-ttu-id="3cecc-113">Le rastériseur doit s’attendre à des coordonnées de texture 2D.</span><span class="sxs-lookup"><span data-stu-id="3cecc-113">The rasterizer should expect 2D texture coordinates.</span></span> <span data-ttu-id="3cecc-114">Cette valeur est utilisée par le traitement du vertex de fonction fixe. elle doit être définie sur 0 lors de l’utilisation d’un nuanceur de sommet programmable.</span><span class="sxs-lookup"><span data-stu-id="3cecc-114">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="3cecc-115"><span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF \_ COUNT3**</span><span class="sxs-lookup"><span data-stu-id="3cecc-115"><span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF\_COUNT3**</span></span>
</dt> <dd>

<span data-ttu-id="3cecc-116">Le rastériseur doit s’attendre à des coordonnées de texture 3D.</span><span class="sxs-lookup"><span data-stu-id="3cecc-116">The rasterizer should expect 3D texture coordinates.</span></span> <span data-ttu-id="3cecc-117">Cette valeur est utilisée par le traitement du vertex de fonction fixe. elle doit être définie sur 0 lors de l’utilisation d’un nuanceur de sommet programmable.</span><span class="sxs-lookup"><span data-stu-id="3cecc-117">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="3cecc-118"><span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF \_ COUNT4**</span><span class="sxs-lookup"><span data-stu-id="3cecc-118"><span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF\_COUNT4**</span></span>
</dt> <dd>

<span data-ttu-id="3cecc-119">Le rastériseur doit s’attendre à des coordonnées de texture 4D.</span><span class="sxs-lookup"><span data-stu-id="3cecc-119">The rasterizer should expect 4D texture coordinates.</span></span> <span data-ttu-id="3cecc-120">Cette valeur est utilisée par le traitement du vertex de fonction fixe. elle doit être définie sur 0 lors de l’utilisation d’un nuanceur de sommet programmable.</span><span class="sxs-lookup"><span data-stu-id="3cecc-120">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="3cecc-121"><span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF \_ projetée**</span><span class="sxs-lookup"><span data-stu-id="3cecc-121"><span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF\_PROJECTED**</span></span>
</dt> <dd>

<span data-ttu-id="3cecc-122">Cet indicateur est respecté par le pipeline de pixels de fonction fixe, ainsi que le pipeline de pixel programmable dans les versions PS \_ 1 \_ 1 à PS \_ 1 \_ 3.</span><span class="sxs-lookup"><span data-stu-id="3cecc-122">This flag is honored by the fixed function pixel pipeline, as well as the programmable pixel pipeline in versions ps\_1\_1 to ps\_1\_3.</span></span> <span data-ttu-id="3cecc-123">Lorsque la projection de texture est activée pour une étape de texture, les quatre valeurs à virgule flottante doivent être écrites dans le registre de texture correspondant.</span><span class="sxs-lookup"><span data-stu-id="3cecc-123">When texture projection is enabled for a texture stage, all four floating point values must be written to the corresponding texture register.</span></span> <span data-ttu-id="3cecc-124">Chaque coordonnée de texture est divisée par le dernier élément avant d’être passée au rastériseur.</span><span class="sxs-lookup"><span data-stu-id="3cecc-124">Each texture coordinate is divided by the last element before being passed to the rasterizer.</span></span> <span data-ttu-id="3cecc-125">Par exemple, si cet indicateur est spécifié avec l' \_ indicateur D3DTTFF COUNT3, les première et deuxième coordonnées de texture sont divisées par la troisième coordonnée avant d’être passées au rastériseur.</span><span class="sxs-lookup"><span data-stu-id="3cecc-125">For example, if this flag is specified with the D3DTTFF\_COUNT3 flag, the first and second texture coordinates are divided by the third coordinate before being passed to the rasterizer.</span></span>

</dd> <dt>

<span data-ttu-id="3cecc-126"><span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3cecc-126"><span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="3cecc-127">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="3cecc-127">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="3cecc-128">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3cecc-128">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="3cecc-129">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="3cecc-129">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3cecc-130">Notes</span><span class="sxs-lookup"><span data-stu-id="3cecc-130">Remarks</span></span>

<span data-ttu-id="3cecc-131">Les coordonnées de texture peuvent être transformées à l’aide d’une matrice 4 x 4 avant que les résultats ne soient passés au rastériseur.</span><span class="sxs-lookup"><span data-stu-id="3cecc-131">Texture coordinates can be transformed using a 4 x 4 matrix before the results are passed to the rasterizer.</span></span> <span data-ttu-id="3cecc-132">Les transformations de coordonnées de texture sont définies en appelant [**IDirect3DDevice9 :: SetTextureStageState**](/windows/desktop/api)et en passant l’état de l' \_ étape de texture D3DTSS TEXTURETRANSFORMFLAGS et l’une des valeurs de **D3DTEXTURETRANSFORMFLAGS**.</span><span class="sxs-lookup"><span data-stu-id="3cecc-132">The texture coordinate transforms are set by calling [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api), and by passing in the D3DTSS\_TEXTURETRANSFORMFLAGS texture stage state and one of the values from **D3DTEXTURETRANSFORMFLAGS**.</span></span> <span data-ttu-id="3cecc-133">Pour plus d’informations sur les transformations de texture, consultez [transformations de coordonnées de texture (Direct3D 9)](texture-coordinate-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="3cecc-133">For more information about texture transforms, see [Texture Coordinate Transformations (Direct3D 9)](texture-coordinate-transformations.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3cecc-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cecc-134">Requirements</span></span>



| <span data-ttu-id="3cecc-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cecc-135">Requirement</span></span> | <span data-ttu-id="3cecc-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cecc-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cecc-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="3cecc-137">Header</span></span><br/> | <dl> <span data-ttu-id="3cecc-138"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cecc-138"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cecc-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cecc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cecc-140">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="3cecc-140">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="3cecc-141">**D3DTEXTURESTAGESTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="3cecc-141">**D3DTEXTURESTAGESTATETYPE**</span></span>](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
