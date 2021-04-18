---
description: Décrit une fonction utilisée par un effet.
ms.assetid: 5d9deb82-7fe5-4408-8a6a-b34ecd97e8ba
title: Structure D3DXFUNCTION_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFUNCTION_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: ec53cae4689ebc1795937012259b2e219630568b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106536245"
---
# <a name="d3dxfunction_desc-structure"></a><span data-ttu-id="c3134-103">D3DXFUNCTION \_ desc, structure</span><span class="sxs-lookup"><span data-stu-id="c3134-103">D3DXFUNCTION\_DESC structure</span></span>

<span data-ttu-id="c3134-104">Décrit une fonction utilisée par un effet.</span><span class="sxs-lookup"><span data-stu-id="c3134-104">Describes a function used by an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3134-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3134-105">Syntax</span></span>


```C++
typedef struct D3DXFUNCTION_DESC {
  LPCSTR Name;
  UINT   Annotations;
} D3DXFUNCTION_DESC, *LPD3DXFUNCTION_DESC;
```



## <a name="members"></a><span data-ttu-id="c3134-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c3134-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3134-107">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c3134-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="c3134-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3134-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c3134-109">Le nom de la fonction</span><span class="sxs-lookup"><span data-stu-id="c3134-109">Function name.</span></span>

</dd> <dt>

<span data-ttu-id="c3134-110">**Annotations**</span><span class="sxs-lookup"><span data-stu-id="c3134-110">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="c3134-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3134-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c3134-112">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="c3134-112">Unused.</span></span> <span data-ttu-id="c3134-113">Ce membre sera toujours défini sur zéro par [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md).</span><span class="sxs-lookup"><span data-stu-id="c3134-113">This member will always be set to zero by [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3134-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3134-114">Requirements</span></span>



| <span data-ttu-id="c3134-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3134-115">Requirement</span></span> | <span data-ttu-id="c3134-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3134-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3134-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3134-117">Header</span></span><br/> | <dl> <span data-ttu-id="c3134-118"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3134-118"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3134-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3134-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3134-120">Structures d’effet</span><span class="sxs-lookup"><span data-stu-id="c3134-120">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
