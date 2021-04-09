---
description: Indicateurs utilisés pour obtenir des informations de rappel.
ms.assetid: e8126ff0-db23-4da6-a999-0efb8c2647da
title: Énumération D3DXCALLBACK_SEARCH_FLAGS (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCALLBACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: d3302b79734557a5c1f2082ec2a4e95c03790f4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043120"
---
# <a name="d3dxcallback_search_flags-enumeration"></a><span data-ttu-id="e5c5d-103">\_Énumération d’indicateurs de recherche D3DXCALLBACK \_</span><span class="sxs-lookup"><span data-stu-id="e5c5d-103">D3DXCALLBACK\_SEARCH\_FLAGS enumeration</span></span>

<span data-ttu-id="e5c5d-104">Indicateurs utilisés pour obtenir des informations de rappel.</span><span class="sxs-lookup"><span data-stu-id="e5c5d-104">Flags used to obtain callback information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5c5d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5c5d-105">Syntax</span></span>


```C++
typedef enum D3DXCALLBACK_SEARCH_FLAGS { 
  D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION  = 1,
  D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION     = 2,
  D3DXCALLBACK_SEARCH_FORCE_DWORD                 = 0x7fffffff
} D3DXCALLBACK_SEARCH_FLAGS, *LPD3DXCALLBACK_SEARCH_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="e5c5d-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="e5c5d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e5c5d-107"><span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**D3DXCALLBACK la \_ recherche à \_ l’exception de la \_ \_ position initiale**</span><span class="sxs-lookup"><span data-stu-id="e5c5d-107"><span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**D3DXCALLBACK\_SEARCH\_EXCLUDING\_INITIAL\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="e5c5d-108">Exclut les rappels situés à la position initiale de la recherche.</span><span class="sxs-lookup"><span data-stu-id="e5c5d-108">Exclude callbacks located at the initial position from the search.</span></span>

</dd> <dt>

<span data-ttu-id="e5c5d-109"><span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**D3DXCALLBACK \_ recherche \_ derrière \_ la \_ position initiale**</span><span class="sxs-lookup"><span data-stu-id="e5c5d-109"><span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**D3DXCALLBACK\_SEARCH\_BEHIND\_INITIAL\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="e5c5d-110">Inversez le sens de la recherche de rappel.</span><span class="sxs-lookup"><span data-stu-id="e5c5d-110">Reverse the callback search direction.</span></span>

</dd> <dt>

<span data-ttu-id="e5c5d-111"><span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK de \_ force de recherche de \_ \_ mot de passe**</span><span class="sxs-lookup"><span data-stu-id="e5c5d-111"><span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK\_SEARCH\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="e5c5d-112">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="e5c5d-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="e5c5d-113">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e5c5d-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="e5c5d-114">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="e5c5d-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5c5d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5c5d-115">Requirements</span></span>



| <span data-ttu-id="e5c5d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5c5d-116">Requirement</span></span> | <span data-ttu-id="e5c5d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5c5d-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c5d-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5c5d-118">Header</span></span><br/> | <dl> <span data-ttu-id="e5c5d-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5c5d-119"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5c5d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5c5d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c5d-121">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="e5c5d-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




