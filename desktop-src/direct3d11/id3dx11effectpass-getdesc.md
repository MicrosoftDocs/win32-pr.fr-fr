---
title: Méthode ID3DX11EffectPass GetDesc (D3dx11effect. h)
description: Obtenir une description du passage.
ms.assetid: 423766be-96b2-4038-834e-34125789e8b1
keywords:
- Méthode GetDesc Direct3D 11
- Méthode GetDesc Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, méthode GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a85a8c08faa100ecb3987a1a1421613d9c448b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323074"
---
# <a name="id3dx11effectpassgetdesc-method"></a><span data-ttu-id="275bd-106">ID3DX11EffectPass :: GetDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="275bd-106">ID3DX11EffectPass::GetDesc method</span></span>

<span data-ttu-id="275bd-107">Obtenir une description du passage.</span><span class="sxs-lookup"><span data-stu-id="275bd-107">Get a pass description.</span></span>

## <a name="syntax"></a><span data-ttu-id="275bd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="275bd-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_PASS_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="275bd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="275bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="275bd-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="275bd-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="275bd-111">Type : **[ **D3DX11 \_ passe \_ desc**](d3dx11-pass-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="275bd-111">Type: **[**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md)\***</span></span>

<span data-ttu-id="275bd-112">Pointeur vers une description de la passe (consultez [**D3DX11 \_ Pass \_ desc**](d3dx11-pass-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="275bd-112">A pointer to a pass description (see [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="275bd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="275bd-113">Return value</span></span>

<span data-ttu-id="275bd-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="275bd-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="275bd-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="275bd-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="275bd-116">Notes</span><span class="sxs-lookup"><span data-stu-id="275bd-116">Remarks</span></span>

<span data-ttu-id="275bd-117">Une passe est un bloc de code qui définit l’état de rendu et les nuanceurs (qui, à son tour, définit les mémoires tampons constantes, les échantillonneurs et les textures).</span><span class="sxs-lookup"><span data-stu-id="275bd-117">A pass is a block of code that sets render state and shaders (which in turn sets constant buffers, samplers and textures).</span></span> <span data-ttu-id="275bd-118">Une technique d’effet contient une ou plusieurs passes.</span><span class="sxs-lookup"><span data-stu-id="275bd-118">An effect technique contains one or more passes.</span></span>

> [!Note]  
> <span data-ttu-id="275bd-119">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="275bd-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="275bd-120">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="275bd-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="275bd-121">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="275bd-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="275bd-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="275bd-122">Requirements</span></span>



| <span data-ttu-id="275bd-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="275bd-123">Requirement</span></span> | <span data-ttu-id="275bd-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="275bd-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="275bd-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="275bd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="275bd-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="275bd-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="275bd-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="275bd-127">Library</span></span><br/> | <dl> <span data-ttu-id="275bd-128"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="275bd-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="275bd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="275bd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="275bd-130">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="275bd-130">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





