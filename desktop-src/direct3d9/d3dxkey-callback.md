---
description: Décrit une clé de rappel à utiliser dans l’animation d’image clé.
ms.assetid: aca034f5-6961-49f1-ba7c-addcf016af2b
title: Structure D3DXKEY_CALLBACK (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_CALLBACK
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5c2c4dc90cbb95218268bf673204867f5b5d6636
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527103"
---
# <a name="d3dxkey_callback-structure"></a><span data-ttu-id="0c291-103">\_Structure de rappel D3DXKEY</span><span class="sxs-lookup"><span data-stu-id="0c291-103">D3DXKEY\_CALLBACK structure</span></span>

<span data-ttu-id="0c291-104">Décrit une clé de rappel à utiliser dans l’animation d’image clé.</span><span class="sxs-lookup"><span data-stu-id="0c291-104">Describes a callback key for use in key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c291-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c291-105">Syntax</span></span>


```C++
typedef struct D3DXKEY_CALLBACK {
  FLOAT  Time;
  LPVOID pCallbackData;
} D3DXKEY_CALLBACK, *LPD3DXKEY_CALLBACK;
```



## <a name="members"></a><span data-ttu-id="0c291-106">Membres</span><span class="sxs-lookup"><span data-stu-id="0c291-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0c291-107">**Time**</span><span class="sxs-lookup"><span data-stu-id="0c291-107">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="0c291-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c291-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0c291-109">Horodatage de l’image clé.</span><span class="sxs-lookup"><span data-stu-id="0c291-109">Key frame time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="0c291-110">**pCallbackData**</span><span class="sxs-lookup"><span data-stu-id="0c291-110">**pCallbackData**</span></span>
</dt> <dd>

<span data-ttu-id="0c291-111">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c291-111">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0c291-112">Pointeur vers les données de rappel de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0c291-112">Pointer to user callback data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c291-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c291-113">Requirements</span></span>



| <span data-ttu-id="0c291-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c291-114">Requirement</span></span> | <span data-ttu-id="0c291-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c291-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c291-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c291-116">Header</span></span><br/> | <dl> <span data-ttu-id="0c291-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c291-117"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c291-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c291-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c291-119">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="0c291-119">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
