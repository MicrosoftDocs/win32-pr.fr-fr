---
description: Identifie les données de mémoire.
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: Structure D3DXF_FILELOADMEMORY (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADMEMORY
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: a7ad988d9906101db57af6f8f5042766c3e32ccc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953852"
---
# <a name="d3dxf_fileloadmemory-structure"></a><span data-ttu-id="1d964-103">D3DXF \_ FILELOADMEMORY, structure</span><span class="sxs-lookup"><span data-stu-id="1d964-103">D3DXF\_FILELOADMEMORY structure</span></span>

<span data-ttu-id="1d964-104">Identifie les données de mémoire.</span><span class="sxs-lookup"><span data-stu-id="1d964-104">Identifies memory data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d964-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d964-105">Syntax</span></span>


```C++
typedef struct D3DXF_FILELOADMEMORY {
  LPCVOID lpMemory;
  SIZE_T  dSize;
} D3DXF_FILELOADMEMORY, *LPD3DXF_FILELOADMEMORY;
```



## <a name="members"></a><span data-ttu-id="1d964-106">Membres</span><span class="sxs-lookup"><span data-stu-id="1d964-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1d964-107">**lpMemory**</span><span class="sxs-lookup"><span data-stu-id="1d964-107">**lpMemory**</span></span>
</dt> <dd>

<span data-ttu-id="1d964-108">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d964-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1d964-109">Pointeur vers un bloc de mémoire à charger.</span><span class="sxs-lookup"><span data-stu-id="1d964-109">Pointer to a block of memory to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="1d964-110">**dSize**</span><span class="sxs-lookup"><span data-stu-id="1d964-110">**dSize**</span></span>
</dt> <dd>

<span data-ttu-id="1d964-111">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d964-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1d964-112">Taille du bloc de mémoire à charger, en octets.</span><span class="sxs-lookup"><span data-stu-id="1d964-112">Size of the block of memory to be loaded, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d964-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1d964-113">Remarks</span></span>

<span data-ttu-id="1d964-114">Cette structure identifie les données à charger à partir de la mémoire lorsqu’une application utilise la méthode [**CreateEnumObject**](id3dxfile--createenumobject.md) et spécifie l' \_ \_ indicateur FROMMEMORY FILELOAD D3DXF.</span><span class="sxs-lookup"><span data-stu-id="1d964-114">This structure identifies data to be loaded from memory when an application uses the [**CreateEnumObject**](id3dxfile--createenumobject.md) method and specifies the D3DXF\_FILELOAD\_FROMMEMORY flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d964-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d964-115">Requirements</span></span>



| <span data-ttu-id="1d964-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d964-116">Requirement</span></span> | <span data-ttu-id="1d964-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d964-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d964-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d964-118">Header</span></span><br/> | <dl> <span data-ttu-id="1d964-119"><dt>D3dx9xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d964-119"><dt>D3dx9xof.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d964-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d964-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d964-121">Structures de fichiers D3DX X</span><span class="sxs-lookup"><span data-stu-id="1d964-121">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
