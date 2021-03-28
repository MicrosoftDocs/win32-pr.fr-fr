---
title: Méthode ID3DX11EffectClassInstanceVariable GetClassInstance (D3dx11effect. h)
description: Obtient une instance de classe.
ms.assetid: dec00a6b-0587-40cf-abae-dd110a639fe0
keywords:
- Méthode GetClassInstance Direct3D 11
- Méthode GetClassInstance Direct3D 11, interface ID3DX11EffectClassInstanceVariable
- Interface ID3DX11EffectClassInstanceVariable Direct3D 11, méthode GetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dae96d42a0088adc683ca93d7e3215c12912a87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323393"
---
# <a name="id3dx11effectclassinstancevariablegetclassinstance-method"></a><span data-ttu-id="ccde2-106">ID3DX11EffectClassInstanceVariable :: GetClassInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="ccde2-106">ID3DX11EffectClassInstanceVariable::GetClassInstance method</span></span>

<span data-ttu-id="ccde2-107">Obtient une instance de classe.</span><span class="sxs-lookup"><span data-stu-id="ccde2-107">Gets a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccde2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ccde2-108">Syntax</span></span>


```C++
HRESULT GetClassInstance(
   ID3D11ClassInstance **ppClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="ccde2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ccde2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccde2-110">*ppClassInstance*</span><span class="sxs-lookup"><span data-stu-id="ccde2-110">*ppClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="ccde2-111">Type : **[ **ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***</span><span class="sxs-lookup"><span data-stu-id="ccde2-111">Type: **[**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***</span></span>

<span data-ttu-id="ccde2-112">Pointeur vers un pointeur [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) qui sera défini sur l’instance de classe.</span><span class="sxs-lookup"><span data-stu-id="ccde2-112">Pointer to an [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) pointer that will be set to class instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccde2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ccde2-113">Return value</span></span>

<span data-ttu-id="ccde2-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ccde2-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ccde2-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="ccde2-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ccde2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ccde2-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ccde2-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="ccde2-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ccde2-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="ccde2-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ccde2-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ccde2-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ccde2-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ccde2-120">Requirements</span></span>



| <span data-ttu-id="ccde2-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ccde2-121">Requirement</span></span> | <span data-ttu-id="ccde2-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccde2-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccde2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ccde2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ccde2-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccde2-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ccde2-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ccde2-125">Library</span></span><br/> | <dl> <span data-ttu-id="ccde2-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="ccde2-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccde2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccde2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccde2-128">ID3DX11EffectClassInstanceVariable</span><span class="sxs-lookup"><span data-stu-id="ccde2-128">ID3DX11EffectClassInstanceVariable</span></span>](id3dx11effectclassinstancevariable.md)
</dt> </dl>

 

 





