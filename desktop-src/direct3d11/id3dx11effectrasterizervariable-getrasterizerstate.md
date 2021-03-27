---
title: Méthode ID3DX11EffectRasterizerVariable GetRasterizerState (D3dx11effect. h)
description: Obtient un pointeur vers une interface de rastérisation.
ms.assetid: 4b8515e0-b79a-4572-9142-07c50a8839b8
keywords:
- Méthode GetRasterizerState Direct3D 11
- Méthode GetRasterizerState Direct3D 11, interface ID3DX11EffectRasterizerVariable
- Interface ID3DX11EffectRasterizerVariable Direct3D 11, méthode GetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972140a8f74a3e5a6728429faddacc253aaa6c9d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982626"
---
# <a name="id3dx11effectrasterizervariablegetrasterizerstate-method"></a><span data-ttu-id="2e2c7-106">ID3DX11EffectRasterizerVariable :: GetRasterizerState, méthode</span><span class="sxs-lookup"><span data-stu-id="2e2c7-106">ID3DX11EffectRasterizerVariable::GetRasterizerState method</span></span>

<span data-ttu-id="2e2c7-107">Obtient un pointeur vers une interface de rastérisation.</span><span class="sxs-lookup"><span data-stu-id="2e2c7-107">Get a pointer to a rasterizer interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e2c7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e2c7-108">Syntax</span></span>


```C++
HRESULT GetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState **ppRasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="2e2c7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e2c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e2c7-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="2e2c7-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="2e2c7-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2e2c7-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2e2c7-112">Index dans un tableau d’interfaces de rastérisation.</span><span class="sxs-lookup"><span data-stu-id="2e2c7-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="2e2c7-113">S’il n’existe qu’une seule interface rastériseur, utilisez 0.</span><span class="sxs-lookup"><span data-stu-id="2e2c7-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="2e2c7-114">*ppRasterizerState*</span><span class="sxs-lookup"><span data-stu-id="2e2c7-114">*ppRasterizerState*</span></span> 
</dt> <dd>

<span data-ttu-id="2e2c7-115">Type : **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="2e2c7-115">Type: **[**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***</span></span>

<span data-ttu-id="2e2c7-116">Adresse d’un pointeur vers une interface de rastérisation (consultez [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)).</span><span class="sxs-lookup"><span data-stu-id="2e2c7-116">The address of a pointer to a rasterizer interface (see [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e2c7-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e2c7-117">Return value</span></span>

<span data-ttu-id="2e2c7-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2e2c7-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2e2c7-119">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="2e2c7-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2e2c7-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2e2c7-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2e2c7-121">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="2e2c7-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2e2c7-122">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="2e2c7-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2e2c7-123">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2e2c7-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e2c7-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2e2c7-124">Requirements</span></span>



| <span data-ttu-id="2e2c7-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e2c7-125">Requirement</span></span> | <span data-ttu-id="2e2c7-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e2c7-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2c7-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e2c7-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2e2c7-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e2c7-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2e2c7-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2e2c7-129">Library</span></span><br/> | <dl> <span data-ttu-id="2e2c7-130"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="2e2c7-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e2c7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e2c7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e2c7-132">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="2e2c7-132">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

