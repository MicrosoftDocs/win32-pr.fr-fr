---
title: Méthode ID3DX11EffectPass ComputeStateBlockMask (D3dx11effect. h)
description: Générez un masque pour autoriser ou empêcher les modifications d’État.
ms.assetid: 584be931-0e22-43e6-b852-f0d2ab050bdd
keywords:
- Méthode ComputeStateBlockMask Direct3D 11
- Méthode ComputeStateBlockMask Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, méthode ComputeStateBlockMask
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc5cb32ce9e9644d7d5b62868bfa99f150cc94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974619"
---
# <a name="id3dx11effectpasscomputestateblockmask-method"></a><span data-ttu-id="61cc3-106">ID3DX11EffectPass :: ComputeStateBlockMask, méthode</span><span class="sxs-lookup"><span data-stu-id="61cc3-106">ID3DX11EffectPass::ComputeStateBlockMask method</span></span>

<span data-ttu-id="61cc3-107">Générez un masque pour autoriser ou empêcher les modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="61cc3-107">Generate a mask for allowing/preventing state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="61cc3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61cc3-108">Syntax</span></span>


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a><span data-ttu-id="61cc3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61cc3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61cc3-110">*pStateBlockMask*</span><span class="sxs-lookup"><span data-stu-id="61cc3-110">*pStateBlockMask*</span></span> 
</dt> <dd>

<span data-ttu-id="61cc3-111">Type : **[ **\_ masque de \_ bloc \_ d’État D3DX11**](d3dx11-state-block-mask.md)\***</span><span class="sxs-lookup"><span data-stu-id="61cc3-111">Type: **[**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)\***</span></span>

<span data-ttu-id="61cc3-112">Pointeur vers un masque de bloc d’État (voir [**\_ masque de \_ bloc \_ d’État D3DX11**](d3dx11-state-block-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="61cc3-112">A pointer to a state-block mask (see [**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61cc3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61cc3-113">Return value</span></span>

<span data-ttu-id="61cc3-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="61cc3-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="61cc3-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="61cc3-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="61cc3-116">Notes</span><span class="sxs-lookup"><span data-stu-id="61cc3-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="61cc3-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="61cc3-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="61cc3-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="61cc3-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="61cc3-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="61cc3-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="61cc3-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="61cc3-120">Requirements</span></span>



| <span data-ttu-id="61cc3-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61cc3-121">Requirement</span></span> | <span data-ttu-id="61cc3-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="61cc3-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61cc3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="61cc3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="61cc3-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="61cc3-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="61cc3-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="61cc3-125">Library</span></span><br/> | <dl> <span data-ttu-id="61cc3-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="61cc3-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61cc3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61cc3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61cc3-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="61cc3-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





