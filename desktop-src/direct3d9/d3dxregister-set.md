---
description: Type de données du Registre.
ms.assetid: b54530d3-4267-4b41-9a16-59d400ef3e18
title: Énumération D3DXREGISTER_SET (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXREGISTER_SET
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 683b13d0b386fcdbc162293455e2beb11bc1ee85
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523181"
---
# <a name="d3dxregister_set-enumeration"></a><span data-ttu-id="c9545-103">D3DXREGISTER \_ Set, énumération</span><span class="sxs-lookup"><span data-stu-id="c9545-103">D3DXREGISTER\_SET enumeration</span></span>

<span data-ttu-id="c9545-104">Type de données du Registre.</span><span class="sxs-lookup"><span data-stu-id="c9545-104">Data type of the register.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9545-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9545-105">Syntax</span></span>


```C++
typedef enum _D3DXREGISTER_SET { 
  D3DXRS_BOOL,
  D3DXRS_INT4,
  D3DXRS_FLOAT4,
  D3DXRS_SAMPLER,
  D3DXRS_FORCE_DWORD  = 0x7fffffff
} D3DXREGISTER_SET, *LPD3DXREGISTER_SET;
```



## <a name="constants"></a><span data-ttu-id="c9545-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c9545-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c9545-107"><span id="D3DXRS_BOOL"></span><span id="d3dxrs_bool"></span>**D3DXRS \_ bool**</span><span class="sxs-lookup"><span data-stu-id="c9545-107"><span id="D3DXRS_BOOL"></span><span id="d3dxrs_bool"></span>**D3DXRS\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="c9545-108">Valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="c9545-108">Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="c9545-109"><span id="D3DXRS_INT4"></span><span id="d3dxrs_int4"></span>**D3DXRS \_ INT4**</span><span class="sxs-lookup"><span data-stu-id="c9545-109"><span id="D3DXRS_INT4"></span><span id="d3dxrs_int4"></span>**D3DXRS\_INT4**</span></span>
</dt> <dd>

<span data-ttu-id="c9545-110">nombre entier 4D.</span><span class="sxs-lookup"><span data-stu-id="c9545-110">4D integer number.</span></span>

</dd> <dt>

<span data-ttu-id="c9545-111"><span id="D3DXRS_FLOAT4"></span><span id="d3dxrs_float4"></span>**D3DXRS \_ float4**</span><span class="sxs-lookup"><span data-stu-id="c9545-111"><span id="D3DXRS_FLOAT4"></span><span id="d3dxrs_float4"></span>**D3DXRS\_FLOAT4**</span></span>
</dt> <dd>

<span data-ttu-id="c9545-112">nombre à virgule flottante 4D.</span><span class="sxs-lookup"><span data-stu-id="c9545-112">4D floating-point number.</span></span>

</dd> <dt>

<span data-ttu-id="c9545-113"><span id="D3DXRS_SAMPLER"></span><span id="d3dxrs_sampler"></span>**\_Échantillonneur D3DXRS**</span><span class="sxs-lookup"><span data-stu-id="c9545-113"><span id="D3DXRS_SAMPLER"></span><span id="d3dxrs_sampler"></span>**D3DXRS\_SAMPLER**</span></span>
</dt> <dd>

<span data-ttu-id="c9545-114">Le registre contient des données d’échantillonneur 4D.</span><span class="sxs-lookup"><span data-stu-id="c9545-114">The register contains 4D sampler data.</span></span>

</dd> <dt>

<span data-ttu-id="c9545-115"><span id="D3DXRS_FORCE_DWORD"></span><span id="d3dxrs_force_dword"></span>**D3DXRS \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c9545-115"><span id="D3DXRS_FORCE_DWORD"></span><span id="d3dxrs_force_dword"></span>**D3DXRS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c9545-116">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="c9545-116">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="c9545-117">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c9545-117">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="c9545-118">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c9545-118">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9545-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9545-119">Requirements</span></span>



| <span data-ttu-id="c9545-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9545-120">Requirement</span></span> | <span data-ttu-id="c9545-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9545-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9545-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9545-122">Header</span></span><br/> | <dl> <span data-ttu-id="c9545-123"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9545-123"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9545-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9545-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9545-125">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="c9545-125">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="c9545-126">**D3DXSHADER \_ CONSTANTINFO**</span><span class="sxs-lookup"><span data-stu-id="c9545-126">**D3DXSHADER\_CONSTANTINFO**</span></span>](d3dxshader-constantinfo.md)
</dt> <dt>

[<span data-ttu-id="c9545-127">**D3DXCONSTANT \_ desc**</span><span class="sxs-lookup"><span data-stu-id="c9545-127">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




