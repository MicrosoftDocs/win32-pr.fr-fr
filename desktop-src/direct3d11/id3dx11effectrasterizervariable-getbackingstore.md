---
title: Méthode ID3DX11EffectRasterizerVariable GetBackingStore (D3dx11effect. h)
description: Obtient un pointeur vers une variable qui contient l’État rasteriser.
ms.assetid: aff62a6c-bdef-49ad-9492-5db0878f632e
keywords:
- Méthode GetBackingStore Direct3D 11
- Méthode GetBackingStore Direct3D 11, interface ID3DX11EffectRasterizerVariable
- Interface ID3DX11EffectRasterizerVariable Direct3D 11, méthode GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1941ba93b69f1d07eeebaa6c1f0c9323f5c0a49e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043160"
---
# <a name="id3dx11effectrasterizervariablegetbackingstore-method"></a><span data-ttu-id="fe35f-106">ID3DX11EffectRasterizerVariable :: GetBackingStore, méthode</span><span class="sxs-lookup"><span data-stu-id="fe35f-106">ID3DX11EffectRasterizerVariable::GetBackingStore method</span></span>

<span data-ttu-id="fe35f-107">Obtient un pointeur vers une variable qui contient l’État rasteriser.</span><span class="sxs-lookup"><span data-stu-id="fe35f-107">Get a pointer to a variable that contains rasteriser state.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe35f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe35f-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT                  Index,
   D3D11_RASTERIZER_DESC *pRasterizerDesc
);
```



## <a name="parameters"></a><span data-ttu-id="fe35f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe35f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe35f-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="fe35f-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="fe35f-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fe35f-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fe35f-112">Index dans un tableau de descriptions d’État rasteriser.</span><span class="sxs-lookup"><span data-stu-id="fe35f-112">Index into an array of rasteriser-state descriptions.</span></span> <span data-ttu-id="fe35f-113">S’il n’existe qu’une seule variable rasteriser dans l’effet, utilisez 0.</span><span class="sxs-lookup"><span data-stu-id="fe35f-113">If there is only one rasteriser variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="fe35f-114">*pRasterizerDesc*</span><span class="sxs-lookup"><span data-stu-id="fe35f-114">*pRasterizerDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="fe35f-115">Type : **[ **d3d11 \_ rastériseur \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***</span><span class="sxs-lookup"><span data-stu-id="fe35f-115">Type: **[**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***</span></span>

<span data-ttu-id="fe35f-116">Pointeur vers une description de l’État rasteriser (voir [**d3d11 \_ rastériseur \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)).</span><span class="sxs-lookup"><span data-stu-id="fe35f-116">A pointer to a rasteriser-state description (see [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe35f-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fe35f-117">Return value</span></span>

<span data-ttu-id="fe35f-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe35f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe35f-119">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="fe35f-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe35f-120">Notes</span><span class="sxs-lookup"><span data-stu-id="fe35f-120">Remarks</span></span>

<span data-ttu-id="fe35f-121">Les variables d’effet sont enregistrées en mémoire dans le magasin de stockage ; Quand une technique est appliquée, les valeurs du magasin de stockage sont copiées sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fe35f-121">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="fe35f-122">Les données du magasin de stockage peuvent être utilisées pour recréer la variable si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="fe35f-122">Backing store data can used to recreate the variable when necessary.</span></span>

> [!Note]  
> <span data-ttu-id="fe35f-123">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="fe35f-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fe35f-124">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="fe35f-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fe35f-125">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fe35f-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe35f-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fe35f-126">Requirements</span></span>



| <span data-ttu-id="fe35f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe35f-127">Requirement</span></span> | <span data-ttu-id="fe35f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe35f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe35f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe35f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="fe35f-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe35f-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fe35f-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fe35f-131">Library</span></span><br/> | <dl> <span data-ttu-id="fe35f-132"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="fe35f-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe35f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe35f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe35f-134">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="fe35f-134">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

