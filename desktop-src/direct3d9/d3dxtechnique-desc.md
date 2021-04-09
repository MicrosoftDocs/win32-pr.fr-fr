---
description: Décrit une technique utilisée par un effet.
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: Structure D3DXTECHNIQUE_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTECHNIQUE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 35dd483a983f17371d6a77e6c020b3a45d9e9360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043094"
---
# <a name="d3dxtechnique_desc-structure"></a><span data-ttu-id="53eb2-103">D3DXTECHNIQUE \_ desc, structure</span><span class="sxs-lookup"><span data-stu-id="53eb2-103">D3DXTECHNIQUE\_DESC structure</span></span>

<span data-ttu-id="53eb2-104">Décrit une technique utilisée par un effet.</span><span class="sxs-lookup"><span data-stu-id="53eb2-104">Describes a technique used by an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="53eb2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53eb2-105">Syntax</span></span>


```C++
typedef struct D3DXTECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DXTECHNIQUE_DESC, *LPD3DXTECHNIQUE_DESC;
```



## <a name="members"></a><span data-ttu-id="53eb2-106">Membres</span><span class="sxs-lookup"><span data-stu-id="53eb2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="53eb2-107">**Nom**</span><span class="sxs-lookup"><span data-stu-id="53eb2-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="53eb2-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53eb2-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53eb2-109">Chaîne qui contient le nom de la technique.</span><span class="sxs-lookup"><span data-stu-id="53eb2-109">String that contains the technique name.</span></span>

</dd> <dt>

<span data-ttu-id="53eb2-110">**Mettent**</span><span class="sxs-lookup"><span data-stu-id="53eb2-110">**Passes**</span></span>
</dt> <dd>

<span data-ttu-id="53eb2-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53eb2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53eb2-112">Nombre de passes de rendu requises par la technique.</span><span class="sxs-lookup"><span data-stu-id="53eb2-112">Number of rendering passes the technique requires.</span></span> <span data-ttu-id="53eb2-113">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="53eb2-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="53eb2-114">**Annotations**</span><span class="sxs-lookup"><span data-stu-id="53eb2-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="53eb2-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53eb2-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53eb2-116">Nombre d’annotations.</span><span class="sxs-lookup"><span data-stu-id="53eb2-116">The number of annotations.</span></span> <span data-ttu-id="53eb2-117">Consultez [Ajouter des informations pour appliquer des paramètres avec des \_ Annotations](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="53eb2-117">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53eb2-118">Notes</span><span class="sxs-lookup"><span data-stu-id="53eb2-118">Remarks</span></span>

<span data-ttu-id="53eb2-119">Certaines cartes vidéo peuvent restituer deux textures en une seule passe.</span><span class="sxs-lookup"><span data-stu-id="53eb2-119">Some video cards can render two textures in a single pass.</span></span> <span data-ttu-id="53eb2-120">Toutefois, si une carte n’a pas cette fonctionnalité, il est souvent possible d’afficher le même effet en deux passes, en utilisant une texture pour chaque passe.</span><span class="sxs-lookup"><span data-stu-id="53eb2-120">However, if a card does not have this capability, it is often possible to render the same effect in two passes, using one texture for each pass.</span></span>

## <a name="requirements"></a><span data-ttu-id="53eb2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53eb2-121">Requirements</span></span>



| <span data-ttu-id="53eb2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53eb2-122">Requirement</span></span> | <span data-ttu-id="53eb2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="53eb2-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="53eb2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="53eb2-124">Header</span></span><br/> | <dl> <span data-ttu-id="53eb2-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="53eb2-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53eb2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53eb2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53eb2-127">Structures d’effet</span><span class="sxs-lookup"><span data-stu-id="53eb2-127">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
