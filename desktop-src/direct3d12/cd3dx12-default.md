---
title: Structure CD3DX12_DEFAULT (D3dx12. h)
description: Passe D3D12 \_ par défaut dans un constructeur pour chaque structure d’assistance. Cette structure est simplement utilisée comme un mécanisme pour définir des paramètres par défaut sur les autres structures d’assistance.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- Structure CD3DX12_DEFAULT
topic_type:
- apiref
api_name:
- CD3DX12_DEFAULT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b010e8f0fdce67f16750d0f66d1cf272c8ddb849
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538741"
---
# <a name="cd3dx12_default-structure"></a><span data-ttu-id="1b0f3-105">CD3DX12, \_ structure par défaut</span><span class="sxs-lookup"><span data-stu-id="1b0f3-105">CD3DX12\_DEFAULT structure</span></span>

<span data-ttu-id="1b0f3-106">Passe D3D12 \_ par défaut dans un constructeur pour chaque structure d’assistance.</span><span class="sxs-lookup"><span data-stu-id="1b0f3-106">Passes D3D12\_DEFAULT into a constructor for each helper structure.</span></span> <span data-ttu-id="1b0f3-107">Cette structure est simplement utilisée comme un mécanisme pour définir des paramètres par défaut sur les autres structures d’assistance.</span><span class="sxs-lookup"><span data-stu-id="1b0f3-107">This structure is simply used as a mechanism to set default parameters on the other helper structures.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b0f3-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1b0f3-108">Remarks</span></span>

<span data-ttu-id="1b0f3-109">Ce struct est déclaré comme suit :</span><span class="sxs-lookup"><span data-stu-id="1b0f3-109">This struct is declared as follows:</span></span>

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

<span data-ttu-id="1b0f3-110">Passe D3D12 \_ par défaut dans un constructeur pour chaque struct d’assistance.</span><span class="sxs-lookup"><span data-stu-id="1b0f3-110">Passes D3D12\_DEFAULT into a constructor for each helper struct.</span></span> <span data-ttu-id="1b0f3-111">Par exemple, le constructeur suivant est déclaré dans d3dx12. h :</span><span class="sxs-lookup"><span data-stu-id="1b0f3-111">For example, the following constructor is declared in d3dx12.h:</span></span>

<span data-ttu-id="1b0f3-112">\_ \_ Handle de descripteur de processeur CD3DX12 \_ ( \_ valeur par défaut CD3DX12) {PTR = 0 ;}</span><span class="sxs-lookup"><span data-stu-id="1b0f3-112">CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT) { ptr = 0; }</span></span>

## <a name="requirements"></a><span data-ttu-id="1b0f3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b0f3-113">Requirements</span></span>



| <span data-ttu-id="1b0f3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b0f3-114">Requirement</span></span> | <span data-ttu-id="1b0f3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b0f3-115">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1b0f3-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b0f3-116">Header</span></span><br/> | <dl> <span data-ttu-id="1b0f3-117"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b0f3-117"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b0f3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b0f3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b0f3-119">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="1b0f3-119">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





