---
description: Définit le degré des variables dans l’équation qui décrit une courbe.
ms.assetid: 52a9c57e-a48d-4d8a-a208-97a3d09e7abf
title: Énumération D3DDEGREETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEGREETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 773ef3a8dd8fc5f4657119c2021c5723e54a3bd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525871"
---
# <a name="d3ddegreetype-enumeration"></a><span data-ttu-id="5c7ec-103">Énumération D3DDEGREETYPE</span><span class="sxs-lookup"><span data-stu-id="5c7ec-103">D3DDEGREETYPE enumeration</span></span>

<span data-ttu-id="5c7ec-104">Définit le degré des variables dans l’équation qui décrit une courbe.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-104">Defines the degree of the variables in the equation that describes a curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c7ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c7ec-105">Syntax</span></span>


```C++
typedef enum D3DDEGREETYPE { 
  D3DDEGREE_LINEAR     = 1,
  D3DDEGREE_QUADRATIC  = 2,
  D3DDEGREE_CUBIC      = 3,
  D3DDEGREE_QUINTIC    = 5,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DDEGREETYPE, *LPD3DDEGREETYPE;
```



## <a name="constants"></a><span data-ttu-id="5c7ec-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="5c7ec-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5c7ec-107"><span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**D3DDEGREE \_ linéaire**</span><span class="sxs-lookup"><span data-stu-id="5c7ec-107"><span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**D3DDEGREE\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="5c7ec-108">La courbe est décrite par les variables du premier ordre.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-108">Curve is described by variables of first order.</span></span>

</dd> <dt>

<span data-ttu-id="5c7ec-109"><span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE \_ quadratique**</span><span class="sxs-lookup"><span data-stu-id="5c7ec-109"><span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE\_QUADRATIC**</span></span>
</dt> <dd>

<span data-ttu-id="5c7ec-110">La courbe est décrite par les variables de la deuxième commande.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-110">Curve is described by variables of second order.</span></span>

</dd> <dt>

<span data-ttu-id="5c7ec-111"><span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE \_ cubique**</span><span class="sxs-lookup"><span data-stu-id="5c7ec-111"><span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE\_CUBIC**</span></span>
</dt> <dd>

<span data-ttu-id="5c7ec-112">La courbe est décrite par les variables de troisième ordre.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-112">Curve is described by variables of third order.</span></span>

</dd> <dt>

<span data-ttu-id="5c7ec-113"><span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE \_ quintaux**</span><span class="sxs-lookup"><span data-stu-id="5c7ec-113"><span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE\_QUINTIC**</span></span>
</dt> <dd>

<span data-ttu-id="5c7ec-114">La courbe est décrite par les variables du quatrième ordre.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-114">Curve is described by variables of fourth order.</span></span>

</dd> <dt>

<span data-ttu-id="5c7ec-115"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5c7ec-115"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="5c7ec-116">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-116">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="5c7ec-117">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-117">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="5c7ec-118">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-118">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c7ec-119">Notes</span><span class="sxs-lookup"><span data-stu-id="5c7ec-119">Remarks</span></span>

<span data-ttu-id="5c7ec-120">Les valeurs de cette énumération sont utilisées pour décrire les courbes utilisées par les correctifs de rectangle et de triangle.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-120">The values in this enumeration are used to describe the curves used by rectangle and triangle patches.</span></span> <span data-ttu-id="5c7ec-121">Pour plus d’informations, consultez D3DRS \_ CULLMODE.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-121">For more information, see D3DRS\_CULLMODE.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c7ec-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c7ec-122">Requirements</span></span>



| <span data-ttu-id="5c7ec-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c7ec-123">Requirement</span></span> | <span data-ttu-id="5c7ec-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c7ec-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c7ec-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c7ec-125">Header</span></span><br/> | <dl> <span data-ttu-id="5c7ec-126"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c7ec-126"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c7ec-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c7ec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c7ec-128">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="5c7ec-128">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="5c7ec-129">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="5c7ec-129">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="5c7ec-130">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="5c7ec-130">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
