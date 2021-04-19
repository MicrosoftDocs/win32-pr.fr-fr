---
description: Identifie les données de mémoire. Action déconseillée.
ms.assetid: fe791e13-d5de-425f-b68f-80db8b332cc6
title: DXFILELOADMEMORY, structure (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADMEMORY
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 02424abd354811a6522b58dd0011ecdddce24564
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535827"
---
# <a name="dxfileloadmemory-structure"></a><span data-ttu-id="98859-104">DXFILELOADMEMORY, structure</span><span class="sxs-lookup"><span data-stu-id="98859-104">DXFILELOADMEMORY structure</span></span>

<span data-ttu-id="98859-105">Identifie les données de mémoire.</span><span class="sxs-lookup"><span data-stu-id="98859-105">Identifies memory data.</span></span> <span data-ttu-id="98859-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="98859-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="98859-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98859-107">Syntax</span></span>


```C++
typedef struct DXFILELOADMEMORY {
  LPVOID lpMemory;
  DWORD  dSize;
} DXFILELOADMEMORY, *LPDXFILELOADMEMORY;
```



## <a name="members"></a><span data-ttu-id="98859-108">Membres</span><span class="sxs-lookup"><span data-stu-id="98859-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="98859-109">**lpMemory**</span><span class="sxs-lookup"><span data-stu-id="98859-109">**lpMemory**</span></span>
</dt> <dd>

<span data-ttu-id="98859-110">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98859-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="98859-111">Pointeur vers un bloc de mémoire à charger.</span><span class="sxs-lookup"><span data-stu-id="98859-111">Pointer to a block of memory to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="98859-112">**dSize**</span><span class="sxs-lookup"><span data-stu-id="98859-112">**dSize**</span></span>
</dt> <dd>

<span data-ttu-id="98859-113">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98859-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="98859-114">Taille du bloc de mémoire à charger, en octets.</span><span class="sxs-lookup"><span data-stu-id="98859-114">Size of the block of memory to be loaded, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98859-115">Notes</span><span class="sxs-lookup"><span data-stu-id="98859-115">Remarks</span></span>

<span data-ttu-id="98859-116">Cette structure identifie une ressource à charger lorsqu’une application utilise la méthode [**CreateEnumObject**](idirectxfile--createenumobject.md) et spécifie DXFILELOAD \_ FROMMEMORY.</span><span class="sxs-lookup"><span data-stu-id="98859-116">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](idirectxfile--createenumobject.md) method and specifies DXFILELOAD\_FROMMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="98859-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98859-117">Requirements</span></span>



| <span data-ttu-id="98859-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98859-118">Requirement</span></span> | <span data-ttu-id="98859-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="98859-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="98859-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="98859-120">Header</span></span><br/> | <dl> <span data-ttu-id="98859-121"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="98859-121"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98859-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98859-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98859-123">Structures de fichiers X</span><span class="sxs-lookup"><span data-stu-id="98859-123">X File Structures</span></span>](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="98859-124">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="98859-124">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="98859-125">Constantes DXFILE</span><span class="sxs-lookup"><span data-stu-id="98859-125">DXFILE Constants</span></span>](dxfile.md)
</dt> </dl>

 

 
