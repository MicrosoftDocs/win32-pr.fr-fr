---
description: Paramètres par défaut de l’effet.
ms.assetid: a8a24cf2-0ecd-4429-97d3-086ff49540a1
title: D3DXEFFECTDEFAULT, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: fee415cbd7d8ec28daa079dd2f224949402a813b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538513"
---
# <a name="d3dxeffectdefault-structure"></a><span data-ttu-id="e1270-103">D3DXEFFECTDEFAULT, structure</span><span class="sxs-lookup"><span data-stu-id="e1270-103">D3DXEFFECTDEFAULT structure</span></span>

<span data-ttu-id="e1270-104">Paramètres par défaut de l’effet.</span><span class="sxs-lookup"><span data-stu-id="e1270-104">Effect default parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1270-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1270-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECTDEFAULT {
  LPSTR                 pParamName;
  D3DXEFFECTDEFAULTTYPE Type;
  DWORD                 NumBytes;
  LPVOID                pValue;
} D3DXEFFECTDEFAULT, *LPD3DXEFFECTDEFAULT;
```



## <a name="members"></a><span data-ttu-id="e1270-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e1270-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e1270-107">**pParamName**</span><span class="sxs-lookup"><span data-stu-id="e1270-107">**pParamName**</span></span>
</dt> <dd>

<span data-ttu-id="e1270-108">Type : **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="e1270-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="e1270-109">Nom du paramètre.</span><span class="sxs-lookup"><span data-stu-id="e1270-109">Parameter name.</span></span>

</dd> <dt>

<span data-ttu-id="e1270-110">**Type**</span><span class="sxs-lookup"><span data-stu-id="e1270-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="e1270-111">Type : **[ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**</span><span class="sxs-lookup"><span data-stu-id="e1270-111">Type: **[**D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e1270-112">Type de données dans pValue.</span><span class="sxs-lookup"><span data-stu-id="e1270-112">Data type in pValue.</span></span> <span data-ttu-id="e1270-113">Pour plus d’informations, consultez [ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)</span><span class="sxs-lookup"><span data-stu-id="e1270-113">For more information, see [**D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)</span></span>

</dd> <dt>

<span data-ttu-id="e1270-114">**NumBytes**</span><span class="sxs-lookup"><span data-stu-id="e1270-114">**NumBytes**</span></span>
</dt> <dd>

<span data-ttu-id="e1270-115">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1270-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e1270-116">Taille, en octets, des données vers lesquelles pointe pValue.</span><span class="sxs-lookup"><span data-stu-id="e1270-116">Size, in bytes, of the data pointed to by pValue.</span></span>

</dd> <dt>

<span data-ttu-id="e1270-117">**pValue**</span><span class="sxs-lookup"><span data-stu-id="e1270-117">**pValue**</span></span>
</dt> <dd>

<span data-ttu-id="e1270-118">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1270-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e1270-119">Pointeur vers l’emplacement de mémoire qui contient les données.</span><span class="sxs-lookup"><span data-stu-id="e1270-119">Pointer to the memory location that contains the data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1270-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1270-120">Requirements</span></span>



| <span data-ttu-id="e1270-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1270-121">Requirement</span></span> | <span data-ttu-id="e1270-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1270-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1270-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1270-123">Header</span></span><br/> | <dl> <span data-ttu-id="e1270-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1270-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1270-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1270-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1270-126">Structures d’effet</span><span class="sxs-lookup"><span data-stu-id="e1270-126">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
