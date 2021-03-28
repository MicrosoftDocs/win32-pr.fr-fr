---
title: Méthode ID3DX11Effect GetDesc (D3dx11effect. h)
description: Obtient une description de l’effet.
ms.assetid: ca684786-c813-48d1-acad-e78aafd1c0db
keywords:
- Méthode GetDesc Direct3D 11
- Méthode GetDesc Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetDesc
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587cde43ec2d9136bab5884691c99321d1492835
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996125"
---
# <a name="id3dx11effectgetdesc-method"></a><span data-ttu-id="3df5d-106">ID3DX11Effect :: GetDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="3df5d-106">ID3DX11Effect::GetDesc method</span></span>

<span data-ttu-id="3df5d-107">Obtient une description de l’effet.</span><span class="sxs-lookup"><span data-stu-id="3df5d-107">Get an effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3df5d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3df5d-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="3df5d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3df5d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3df5d-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="3df5d-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="3df5d-111">Type : **[ **D3DX11 \_ effet \_ desc**](d3dx11-effect-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="3df5d-111">Type: **[**D3DX11\_EFFECT\_DESC**](d3dx11-effect-desc.md)\***</span></span>

<span data-ttu-id="3df5d-112">Pointeur vers une description d’effet (consultez [**D3DX11 \_ Effect \_ desc**](d3dx11-effect-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="3df5d-112">A pointer to an effect description (see [**D3DX11\_EFFECT\_DESC**](d3dx11-effect-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3df5d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3df5d-113">Return value</span></span>

<span data-ttu-id="3df5d-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3df5d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3df5d-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="3df5d-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3df5d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="3df5d-116">Remarks</span></span>

<span data-ttu-id="3df5d-117">Une description d’effet contient des informations de base sur un effet tel que les techniques qu’il contient et les ressources de mémoire tampon constantes dont il a besoin.</span><span class="sxs-lookup"><span data-stu-id="3df5d-117">An effect description contains basic information about an effect such as the techniques it contains and the constant buffer resources it requires.</span></span>

> [!Note]  
> <span data-ttu-id="3df5d-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="3df5d-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3df5d-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="3df5d-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3df5d-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3df5d-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3df5d-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3df5d-121">Requirements</span></span>



| <span data-ttu-id="3df5d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3df5d-122">Requirement</span></span> | <span data-ttu-id="3df5d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3df5d-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3df5d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3df5d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3df5d-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3df5d-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3df5d-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3df5d-126">Library</span></span><br/> | <dl> <span data-ttu-id="3df5d-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="3df5d-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3df5d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3df5d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df5d-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="3df5d-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





