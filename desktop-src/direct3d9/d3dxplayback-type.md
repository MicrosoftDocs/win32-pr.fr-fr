---
description: Définit le type de mode de bouclage défini par l’animation utilisé pour la lecture.
ms.assetid: 2ce26bf0-2b33-4193-a58f-03493a051351
title: Énumération D3DXPLAYBACK_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLAYBACK_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ce95b4765ec678c43c8e0ed92008deeb9927298
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870098"
---
# <a name="d3dxplayback_type-enumeration"></a><span data-ttu-id="b5974-103">\_Énumération de type D3DXPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="b5974-103">D3DXPLAYBACK\_TYPE enumeration</span></span>

<span data-ttu-id="b5974-104">Définit le type de mode de bouclage défini par l’animation utilisé pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="b5974-104">Defines the type of animation set looping modes used for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5974-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5974-105">Syntax</span></span>


```C++
typedef enum D3DXPLAYBACK_TYPE { 
  D3DXPLAY_LOOP         = 0,
  D3DXPLAY_ONCE         = 1,
  D3DXPLAY_PINGPONG     = 2,
  D3DXPLAY_FORCE_DWORD  = 0x7fffffff
} D3DXPLAYBACK_TYPE, *LPD3DXPLAYBACK_TYPE;
```



## <a name="constants"></a><span data-ttu-id="b5974-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b5974-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b5974-107"><span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**\_Boucle D3DXPLAY**</span><span class="sxs-lookup"><span data-stu-id="b5974-107"><span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**D3DXPLAY\_LOOP**</span></span>
</dt> <dd>

<span data-ttu-id="b5974-108">L’animation se répète indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="b5974-108">The animation repeats endlessly.</span></span>

</dd> <dt>

<span data-ttu-id="b5974-109"><span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY \_ une fois**</span><span class="sxs-lookup"><span data-stu-id="b5974-109"><span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY\_ONCE**</span></span>
</dt> <dd>

<span data-ttu-id="b5974-110">L’animation est lue une fois, puis s’arrête sur la dernière image.</span><span class="sxs-lookup"><span data-stu-id="b5974-110">The animation plays once, and then it stops on the last frame.</span></span>

</dd> <dt>

<span data-ttu-id="b5974-111"><span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY \_ essai pingpong**</span><span class="sxs-lookup"><span data-stu-id="b5974-111"><span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY\_PINGPONG**</span></span>
</dt> <dd>

<span data-ttu-id="b5974-112">L’animation alterne de façon infinie entre la progression et la diffusion vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="b5974-112">The animation alternates endlessly between playing forward and playing backward.</span></span>

</dd> <dt>

<span data-ttu-id="b5974-113"><span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b5974-113"><span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="b5974-114">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="b5974-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="b5974-115">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b5974-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="b5974-116">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="b5974-116">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5974-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5974-117">Requirements</span></span>



| <span data-ttu-id="b5974-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5974-118">Requirement</span></span> | <span data-ttu-id="b5974-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5974-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5974-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5974-120">Header</span></span><br/> | <dl> <span data-ttu-id="b5974-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5974-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5974-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5974-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5974-123">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="b5974-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




