---
title: Méthode ID3DX11EffectType GetDesc (D3dx11effect. h)
description: Obtient une description de type d’effet.
ms.assetid: 08a8a1b6-fe2d-431b-a0e4-d628f0ceb1a0
keywords:
- Méthode GetDesc Direct3D 11
- Méthode GetDesc Direct3D 11, interface ID3DX11EffectType
- Interface ID3DX11EffectType Direct3D 11, méthode GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1ee52e4c6628c00b0155e5bd3081b6c4fd8c46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996240"
---
# <a name="id3dx11effecttypegetdesc-method"></a><span data-ttu-id="d7a91-106">ID3DX11EffectType :: GetDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="d7a91-106">ID3DX11EffectType::GetDesc method</span></span>

<span data-ttu-id="d7a91-107">Obtient une description de type d’effet.</span><span class="sxs-lookup"><span data-stu-id="d7a91-107">Get an effect-type description.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7a91-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7a91-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_TYPE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="d7a91-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7a91-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7a91-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="d7a91-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="d7a91-111">Type : type d' **[ **\_ effet D3DX11 \_ \_ desc**](d3dx11-effect-type-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7a91-111">Type: **[**D3DX11\_EFFECT\_TYPE\_DESC**](d3dx11-effect-type-desc.md)\***</span></span>

<span data-ttu-id="d7a91-112">Pointeur vers une description de type d’effet.</span><span class="sxs-lookup"><span data-stu-id="d7a91-112">A pointer to an effect-type description.</span></span> <span data-ttu-id="d7a91-113">Consultez [**la \_ \_ \_ Description du type d’effet D3DX11**](d3dx11-effect-type-desc.md).</span><span class="sxs-lookup"><span data-stu-id="d7a91-113">See [**D3DX11\_EFFECT\_TYPE\_DESC**](d3dx11-effect-type-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7a91-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7a91-114">Return value</span></span>

<span data-ttu-id="d7a91-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d7a91-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d7a91-116">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="d7a91-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d7a91-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d7a91-117">Remarks</span></span>

<span data-ttu-id="d7a91-118">La description de la variable Effect contient des données sur le nom, les annotations, la sémantique, les indicateurs et le décalage de la mémoire tampon du type d’effet.</span><span class="sxs-lookup"><span data-stu-id="d7a91-118">The effect-variable description contains data about the name, annotations, semantic, flags and buffer offset of the effect type.</span></span>

> [!Note]  
> <span data-ttu-id="d7a91-119">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="d7a91-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d7a91-120">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="d7a91-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d7a91-121">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d7a91-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d7a91-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d7a91-122">Requirements</span></span>



| <span data-ttu-id="d7a91-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7a91-123">Requirement</span></span> | <span data-ttu-id="d7a91-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7a91-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a91-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7a91-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d7a91-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7a91-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d7a91-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d7a91-127">Library</span></span><br/> | <dl> <span data-ttu-id="d7a91-128"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="d7a91-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7a91-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7a91-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7a91-130">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="d7a91-130">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

 





