---
description: Définit les jetons du moniteur de débogage.
ms.assetid: c0df4c9f-a232-45cf-b543-e95ee84a4a8d
title: Énumération D3DDEBUGMONITORTOKENS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEBUGMONITORTOKENS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 82c3ecfa7d197e1ab912dbafe0d26fcb2281e605
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953814"
---
# <a name="d3ddebugmonitortokens-enumeration"></a><span data-ttu-id="ffb71-103">Énumération D3DDEBUGMONITORTOKENS</span><span class="sxs-lookup"><span data-stu-id="ffb71-103">D3DDEBUGMONITORTOKENS enumeration</span></span>

<span data-ttu-id="ffb71-104">Définit les jetons du moniteur de débogage.</span><span class="sxs-lookup"><span data-stu-id="ffb71-104">Defines the debug monitor tokens.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffb71-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffb71-105">Syntax</span></span>


```C++
typedef enum D3DDEBUGMONITORTOKENS { 
  D3DDMT_ENABLE       = 0,
  D3DDMT_DISABLE      = 1,
  D3DDMT_FORCE_DWORD  = 0x7fffffff
} D3DDEBUGMONITORTOKENS, *LPD3DDEBUGMONITORTOKENS;
```



## <a name="constants"></a><span data-ttu-id="ffb71-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ffb71-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ffb71-107"><span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**D3DDMT \_ activer**</span><span class="sxs-lookup"><span data-stu-id="ffb71-107"><span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**D3DDMT\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="ffb71-108">Activez le moniteur de débogage.</span><span class="sxs-lookup"><span data-stu-id="ffb71-108">Enable the debug monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ffb71-109"><span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**Désactivation de D3DDMT \_**</span><span class="sxs-lookup"><span data-stu-id="ffb71-109"><span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**D3DDMT\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="ffb71-110">Désactivez le moniteur de débogage.</span><span class="sxs-lookup"><span data-stu-id="ffb71-110">Disable the debug monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ffb71-111"><span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ffb71-111"><span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="ffb71-112">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="ffb71-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="ffb71-113">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ffb71-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="ffb71-114">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ffb71-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffb71-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ffb71-115">Remarks</span></span>

<span data-ttu-id="ffb71-116">Les valeurs de ce type énuméré sont utilisées par l’état de \_ rendu D3DRS DEBUGMONITORTOKEN et ne sont pertinentes que pour les versions Debug.</span><span class="sxs-lookup"><span data-stu-id="ffb71-116">The values in this enumerated type are used by the D3DRS\_DEBUGMONITORTOKEN render state and are only relevant for debug builds.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffb71-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffb71-117">Requirements</span></span>



| <span data-ttu-id="ffb71-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffb71-118">Requirement</span></span> | <span data-ttu-id="ffb71-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffb71-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffb71-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffb71-120">Header</span></span><br/> | <dl> <span data-ttu-id="ffb71-121"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffb71-121"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffb71-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffb71-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffb71-123">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="ffb71-123">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="ffb71-124">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="ffb71-124">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
