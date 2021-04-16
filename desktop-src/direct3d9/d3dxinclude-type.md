---
description: Décrit l’emplacement du fichier include.
ms.assetid: a15d363e-0d82-44a9-816b-edf2f60540b3
title: Énumération D3DXINCLUDE_TYPE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINCLUDE_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 51a4ed41203a9f78ee5fef747f088e9def9033c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530897"
---
# <a name="d3dxinclude_type-enumeration"></a><span data-ttu-id="b67d2-103">\_Énumération de type D3DXINCLUDE</span><span class="sxs-lookup"><span data-stu-id="b67d2-103">D3DXINCLUDE\_TYPE enumeration</span></span>

<span data-ttu-id="b67d2-104">Décrit l’emplacement du fichier include.</span><span class="sxs-lookup"><span data-stu-id="b67d2-104">Describes the location for the include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b67d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b67d2-105">Syntax</span></span>


```C++
typedef enum D3DXINCLUDE_TYPE { 
  D3DXINC_LOCAL        = 0,
  D3DXINC_SYSTEM       = 1,
  D3DXINC_FORCE_DWORD  = 0x7fffffff
} D3DXINCLUDE_TYPE, *LPD3DXINCLUDE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="b67d2-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b67d2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b67d2-107"><span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC \_ local**</span><span class="sxs-lookup"><span data-stu-id="b67d2-107"><span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC\_LOCAL**</span></span>
</dt> <dd>

<span data-ttu-id="b67d2-108">Recherchez le fichier include dans le projet local.</span><span class="sxs-lookup"><span data-stu-id="b67d2-108">Look in the local project for the include file.</span></span>

</dd> <dt>

<span data-ttu-id="b67d2-109"><span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**\_Système D3DXINC**</span><span class="sxs-lookup"><span data-stu-id="b67d2-109"><span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**D3DXINC\_SYSTEM**</span></span>
</dt> <dd>

<span data-ttu-id="b67d2-110">Recherchez le fichier include dans le chemin d’accès système.</span><span class="sxs-lookup"><span data-stu-id="b67d2-110">Look in the system path for the include file.</span></span>

</dd> <dt>

<span data-ttu-id="b67d2-111"><span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b67d2-111"><span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="b67d2-112">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="b67d2-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="b67d2-113">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b67d2-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="b67d2-114">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="b67d2-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b67d2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b67d2-115">Requirements</span></span>



| <span data-ttu-id="b67d2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b67d2-116">Requirement</span></span> | <span data-ttu-id="b67d2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b67d2-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b67d2-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b67d2-118">Header</span></span><br/> | <dl> <span data-ttu-id="b67d2-119"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b67d2-119"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b67d2-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b67d2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b67d2-121">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="b67d2-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




