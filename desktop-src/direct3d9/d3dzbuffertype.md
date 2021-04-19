---
description: Définit des constantes qui décrivent des formats de mémoire tampon de profondeur.
ms.assetid: 5e5ce48b-8859-43e0-a9b4-5972cf6bf781
title: Énumération D3DZBUFFERTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DZBUFFERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 271a278f48c10a89fa6f552c3e1a7b4a83f274f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532454"
---
# <a name="d3dzbuffertype-enumeration"></a><span data-ttu-id="42707-103">Énumération D3DZBUFFERTYPE</span><span class="sxs-lookup"><span data-stu-id="42707-103">D3DZBUFFERTYPE enumeration</span></span>

<span data-ttu-id="42707-104">Définit des constantes qui décrivent des formats de mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="42707-104">Defines constants that describe depth-buffer formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="42707-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42707-105">Syntax</span></span>


```C++
typedef enum D3DZBUFFERTYPE { 
  D3DZB_FALSE        = 0,
  D3DZB_TRUE         = 1,
  D3DZB_USEW         = 2,
  D3DZB_FORCE_DWORD  = 0x7fffffff
} D3DZBUFFERTYPE, *LPD3DZBUFFERTYPE;
```



## <a name="constants"></a><span data-ttu-id="42707-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="42707-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="42707-107"><span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB \_ false**</span><span class="sxs-lookup"><span data-stu-id="42707-107"><span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB\_FALSE**</span></span>
</dt> <dd>

<span data-ttu-id="42707-108">Désactivez la mise en mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="42707-108">Disable depth buffering.</span></span>

</dd> <dt>

<span data-ttu-id="42707-109"><span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB \_ true**</span><span class="sxs-lookup"><span data-stu-id="42707-109"><span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB\_TRUE**</span></span>
</dt> <dd>

<span data-ttu-id="42707-110">Activez la mise en mémoire tampon z.</span><span class="sxs-lookup"><span data-stu-id="42707-110">Enable z-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="42707-111"><span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DZB \_ USEW**</span><span class="sxs-lookup"><span data-stu-id="42707-111"><span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DZB\_USEW**</span></span>
</dt> <dd>

<span data-ttu-id="42707-112">Activez la mise en mémoire tampon w.</span><span class="sxs-lookup"><span data-stu-id="42707-112">Enable w-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="42707-113"><span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="42707-113"><span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="42707-114">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="42707-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="42707-115">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="42707-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="42707-116">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="42707-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42707-117">Notes</span><span class="sxs-lookup"><span data-stu-id="42707-117">Remarks</span></span>

<span data-ttu-id="42707-118">Les membres de ce type énuméré sont utilisés avec l' \_ État de rendu D3DRS ZENABLE.</span><span class="sxs-lookup"><span data-stu-id="42707-118">Members of this enumerated type are used with the D3DRS\_ZENABLE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="42707-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42707-119">Requirements</span></span>



| <span data-ttu-id="42707-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42707-120">Requirement</span></span> | <span data-ttu-id="42707-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="42707-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42707-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="42707-122">Header</span></span><br/> | <dl> <span data-ttu-id="42707-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="42707-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42707-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42707-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42707-125">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="42707-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="42707-126">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="42707-126">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
