---
description: Définit des constantes qui décrivent le type de mémoire tampon d’arrière-plan.
ms.assetid: f099656b-4957-40a7-a92e-2c17e5fa8df9
title: Énumération D3DBACKBUFFER_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBACKBUFFER_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1641b37242339173fc5f591280d8e2beeff6a9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953817"
---
# <a name="d3dbackbuffer_type-enumeration"></a><span data-ttu-id="3e8f8-103">\_Énumération de type D3DBACKBUFFER</span><span class="sxs-lookup"><span data-stu-id="3e8f8-103">D3DBACKBUFFER\_TYPE enumeration</span></span>

<span data-ttu-id="3e8f8-104">Définit des constantes qui décrivent le type de mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="3e8f8-104">Defines constants that describe the type of back buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e8f8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e8f8-105">Syntax</span></span>


```C++
typedef enum D3DBACKBUFFER_TYPE { 
  D3DBACKBUFFER_TYPE_MONO         = 0,
  D3DBACKBUFFER_TYPE_LEFT         = 1,
  D3DBACKBUFFER_TYPE_RIGHT        = 2,
  D3DBACKBUFFER_TYPE_FORCE_DWORD  = 0x7fffffff
} D3DBACKBUFFER_TYPE, *LPD3DBACKBUFFER_TYPE;
```



## <a name="constants"></a><span data-ttu-id="3e8f8-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="3e8f8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3e8f8-107"><span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**TYPE de D3DBACKBUFFER \_ \_ mono**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-107"><span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**D3DBACKBUFFER\_TYPE\_MONO**</span></span>
</dt> <dd>

<span data-ttu-id="3e8f8-108">Spécifie une chaîne d’échange stéréo.</span><span class="sxs-lookup"><span data-stu-id="3e8f8-108">Specifies a nonstereo swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="3e8f8-109"><span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**D3DBACKBUFFER \_ type \_ gauche**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-109"><span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**D3DBACKBUFFER\_TYPE\_LEFT**</span></span>
</dt> <dd>

<span data-ttu-id="3e8f8-110">Spécifie le côté gauche d’une paire stéréo dans une chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="3e8f8-110">Specifies the left side of a stereo pair in a swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="3e8f8-111"><span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**D3DBACKBUFFER \_ type \_ droit**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-111"><span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**D3DBACKBUFFER\_TYPE\_RIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="3e8f8-112">Spécifie le côté droit d’une paire stéréo dans une chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="3e8f8-112">Specifies the right side of a stereo pair in a swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="3e8f8-113"><span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER \_ type \_ force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-113"><span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER\_TYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="3e8f8-114">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="3e8f8-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="3e8f8-115">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3e8f8-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="3e8f8-116">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="3e8f8-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e8f8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3e8f8-117">Remarks</span></span>

<span data-ttu-id="3e8f8-118">Direct3D 9 ne prend pas en charge la vue stéréo, donc Direct3D n’utilise pas les \_ \_ valeurs de type D3DBACKBUFFER Left et D3DBACKBUFFER \_ type \_ Right de ce type énuméré.</span><span class="sxs-lookup"><span data-stu-id="3e8f8-118">Direct3D 9 does not support stereo view, so Direct3D does not use the D3DBACKBUFFER\_TYPE\_LEFT and D3DBACKBUFFER\_TYPE\_RIGHT values of this enumerated type.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e8f8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e8f8-119">Requirements</span></span>



| <span data-ttu-id="3e8f8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e8f8-120">Requirement</span></span> | <span data-ttu-id="3e8f8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e8f8-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e8f8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e8f8-122">Header</span></span><br/> | <dl> <span data-ttu-id="3e8f8-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e8f8-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e8f8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e8f8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e8f8-125">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="3e8f8-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="3e8f8-126">**IDirect3DDevice9::GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-126">**IDirect3DDevice9::GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
</dt> <dt>

[<span data-ttu-id="3e8f8-127">**IDirect3DSwapChain9::GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-127">**IDirect3DSwapChain9::GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer)
</dt> </dl>

 

 
