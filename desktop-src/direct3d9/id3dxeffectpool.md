---
description: Les applications utilisent l’interface ID3DXEffectPool pour identifier les paramètres qui vont être partagés entre les effets. Consultez partage de paramètres dans le clonage et le partage (Direct3D 9). Cette interface n’a pas de méthode.
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: Interface ID3DXEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectPool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893116d7e99bd720f098a8b536f1ad4fd02563ab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394071"
---
# <a name="id3dxeffectpool-interface"></a><span data-ttu-id="c4e9a-105">Interface ID3DXEffectPool</span><span class="sxs-lookup"><span data-stu-id="c4e9a-105">ID3DXEffectPool interface</span></span>

<span data-ttu-id="c4e9a-106">Les applications utilisent l’interface **ID3DXEffectPool** pour identifier les paramètres qui vont être partagés entre les effets.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-106">Applications use the **ID3DXEffectPool** interface to identify parameters that are going to be shared across effects.</span></span> <span data-ttu-id="c4e9a-107">Consultez partage de paramètres dans le [clonage et le partage (Direct3D 9)](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="c4e9a-107">See parameter sharing in [Cloning and Sharing (Direct3D 9)](cloning-and-sharing.md).</span></span> <span data-ttu-id="c4e9a-108">Cette interface n’a pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-108">This interface has no methods.</span></span>

## <a name="members"></a><span data-ttu-id="c4e9a-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c4e9a-109">Members</span></span>

<span data-ttu-id="c4e9a-110">L’interface **ID3DXEffectPool** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-110">The **ID3DXEffectPool** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4e9a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c4e9a-111">Remarks</span></span>

<span data-ttu-id="c4e9a-112">L’interface ID3DXEffectPool est obtenue en appelant [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).</span><span class="sxs-lookup"><span data-stu-id="c4e9a-112">The ID3DXEffectPool interface is obtained by calling [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).</span></span>

<span data-ttu-id="c4e9a-113">Le type LPD3DXEFFECTPOOL est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-113">The LPD3DXEFFECTPOOL type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a><span data-ttu-id="c4e9a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4e9a-114">Requirements</span></span>



| <span data-ttu-id="c4e9a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4e9a-115">Requirement</span></span> | <span data-ttu-id="c4e9a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4e9a-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4e9a-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4e9a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c4e9a-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4e9a-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c4e9a-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c4e9a-119">Library</span></span><br/> | <dl> <span data-ttu-id="c4e9a-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4e9a-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c4e9a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4e9a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4e9a-122">Interfaces d’effet</span><span class="sxs-lookup"><span data-stu-id="c4e9a-122">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
