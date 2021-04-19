---
description: Types de données d’effet. Les données sont contenues dans le membre pValue de D3DXEFFECTDEFAULT.
ms.assetid: d698ad6e-2ce2-48d6-90be-49bc08f172a9
title: Énumération D3DXEFFECTDEFAULTTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULTTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: ffd31167d712a8270011c061cd6328aa9214352e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539878"
---
# <a name="d3dxeffectdefaulttype-enumeration"></a><span data-ttu-id="aaec7-104">Énumération D3DXEFFECTDEFAULTTYPE</span><span class="sxs-lookup"><span data-stu-id="aaec7-104">D3DXEFFECTDEFAULTTYPE enumeration</span></span>

<span data-ttu-id="aaec7-105">Types de données d’effet.</span><span class="sxs-lookup"><span data-stu-id="aaec7-105">Effect data types.</span></span> <span data-ttu-id="aaec7-106">Les données sont contenues dans le membre pValue de [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span><span class="sxs-lookup"><span data-stu-id="aaec7-106">The data is contained in the pValue member of [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aaec7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aaec7-107">Syntax</span></span>


```C++
typedef enum D3DXEFFECTDEFAULTTYPE { 
  D3DXEDT_STRING      = 1,
  D3DXEDT_FLOATS      = 2,
  D3DXEDT_DWORD       = 3,
  D3DXEDT_FORCEDWORD  = 0x7fffffff
} D3DXEFFECTDEFAULTTYPE, *LPD3DXEFFECTDEFAULTTYPE;
```



## <a name="constants"></a><span data-ttu-id="aaec7-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="aaec7-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="aaec7-109"><span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**\_Chaîne D3DXEDT**</span><span class="sxs-lookup"><span data-stu-id="aaec7-109"><span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**D3DXEDT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="aaec7-110">Le type de données est une chaîne de texte ASCII terminée par le caractère NULL.</span><span class="sxs-lookup"><span data-stu-id="aaec7-110">The data type is a NULL-terminated ASCII text string.</span></span>

</dd> <dt>

<span data-ttu-id="aaec7-111"><span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**D3DXEDT \_ Floats**</span><span class="sxs-lookup"><span data-stu-id="aaec7-111"><span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**D3DXEDT\_FLOATS**</span></span>
</dt> <dd>

<span data-ttu-id="aaec7-112">Le type de données est un tableau de type float.</span><span class="sxs-lookup"><span data-stu-id="aaec7-112">The data type is an array of type float.</span></span> <span data-ttu-id="aaec7-113">Le nombre de types float dans le tableau est spécifié par NumBytes dans [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span><span class="sxs-lookup"><span data-stu-id="aaec7-113">The number of float types in the array is specified by NumBytes in [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span></span>

</dd> <dt>

<span data-ttu-id="aaec7-114"><span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="aaec7-114"><span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="aaec7-115">Le type de données est un DWORD.</span><span class="sxs-lookup"><span data-stu-id="aaec7-115">The data type is a DWORD.</span></span>

</dd> <dt>

<span data-ttu-id="aaec7-116"><span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT \_ FORCEDWORD**</span><span class="sxs-lookup"><span data-stu-id="aaec7-116"><span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT\_FORCEDWORD**</span></span>
</dt> <dd>

<span data-ttu-id="aaec7-117">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="aaec7-117">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="aaec7-118">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="aaec7-118">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="aaec7-119">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="aaec7-119">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aaec7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aaec7-120">Requirements</span></span>



| <span data-ttu-id="aaec7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aaec7-121">Requirement</span></span> | <span data-ttu-id="aaec7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="aaec7-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaec7-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="aaec7-123">Header</span></span><br/> | <dl> <span data-ttu-id="aaec7-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaec7-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaec7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaec7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaec7-126">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="aaec7-126">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




