---
title: Méthode ID3DX11EffectTechnique GetPassByName (D3dx11effect. h)
description: Obtenir un passage par nom.
ms.assetid: 07c7502e-2af9-4898-8cd4-106d6814fb85
keywords:
- Méthode GetPassByName Direct3D 11
- Méthode GetPassByName Direct3D 11, interface ID3DX11EffectTechnique
- Interface ID3DX11EffectTechnique Direct3D 11, méthode GetPassByName
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84bbe9b954efff12e458ee6172665118a7b8ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992253"
---
# <a name="id3dx11effecttechniquegetpassbyname-method"></a><span data-ttu-id="01edb-106">ID3DX11EffectTechnique :: GetPassByName, méthode</span><span class="sxs-lookup"><span data-stu-id="01edb-106">ID3DX11EffectTechnique::GetPassByName method</span></span>

<span data-ttu-id="01edb-107">Obtenir un passage par nom.</span><span class="sxs-lookup"><span data-stu-id="01edb-107">Get a pass by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="01edb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01edb-108">Syntax</span></span>


```C++
ID3DX11EffectPass* GetPassByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="01edb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01edb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01edb-110">*Nom*</span><span class="sxs-lookup"><span data-stu-id="01edb-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="01edb-111">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="01edb-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="01edb-112">Nom de la passe.</span><span class="sxs-lookup"><span data-stu-id="01edb-112">The name of the pass.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01edb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01edb-113">Return value</span></span>

<span data-ttu-id="01edb-114">Type : **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***</span><span class="sxs-lookup"><span data-stu-id="01edb-114">Type: **[**ID3DX11EffectPass**](id3dx11effectpass.md)\***</span></span>

<span data-ttu-id="01edb-115">Pointeur vers un [**ID3DX11EffectPass**](id3dx11effectpass.md).</span><span class="sxs-lookup"><span data-stu-id="01edb-115">A pointer to an [**ID3DX11EffectPass**](id3dx11effectpass.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="01edb-116">Notes</span><span class="sxs-lookup"><span data-stu-id="01edb-116">Remarks</span></span>

<span data-ttu-id="01edb-117">Une technique contient une ou plusieurs passes ; obtenir une passe à l’aide d’un nom ou d’un index.</span><span class="sxs-lookup"><span data-stu-id="01edb-117">A technique contains one or more passes; get a pass using a name or an index.</span></span>

> [!Note]  
> <span data-ttu-id="01edb-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="01edb-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="01edb-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="01edb-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="01edb-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="01edb-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01edb-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="01edb-121">Requirements</span></span>



| <span data-ttu-id="01edb-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01edb-122">Requirement</span></span> | <span data-ttu-id="01edb-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="01edb-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01edb-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="01edb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="01edb-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="01edb-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="01edb-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="01edb-126">Library</span></span><br/> | <dl> <span data-ttu-id="01edb-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="01edb-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01edb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01edb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01edb-129">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="01edb-129">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

