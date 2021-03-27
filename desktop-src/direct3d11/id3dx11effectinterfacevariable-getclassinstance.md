---
title: Méthode ID3DX11EffectInterfaceVariable GetClassInstance (D3dx11effect. h)
description: Obtient une instance de classe.
ms.assetid: a965f4e7-1761-45f1-a72e-7ad0ed1ad671
keywords:
- Méthode GetClassInstance Direct3D 11
- Méthode GetClassInstance Direct3D 11, interface ID3DX11EffectInterfaceVariable
- Interface ID3DX11EffectInterfaceVariable Direct3D 11, méthode GetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f729da6ee84d76dd37a40a7946438e367c1a4cbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953915"
---
# <a name="id3dx11effectinterfacevariablegetclassinstance-method"></a><span data-ttu-id="681b9-106">ID3DX11EffectInterfaceVariable :: GetClassInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="681b9-106">ID3DX11EffectInterfaceVariable::GetClassInstance method</span></span>

<span data-ttu-id="681b9-107">Obtient une instance de classe.</span><span class="sxs-lookup"><span data-stu-id="681b9-107">Get a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="681b9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="681b9-108">Syntax</span></span>


```C++
HRESULT GetClassInstance(
   ID3DX11EffectClassInstanceVariable **ppEffectClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="681b9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="681b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="681b9-110">*ppEffectClassInstance*</span><span class="sxs-lookup"><span data-stu-id="681b9-110">*ppEffectClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="681b9-111">Type : **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="681b9-111">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***</span></span>

<span data-ttu-id="681b9-112">Pointeur vers un pointeur [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) qui sera défini sur l’instance de classe.</span><span class="sxs-lookup"><span data-stu-id="681b9-112">Pointer to an [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) pointer that will be set to the class instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="681b9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="681b9-113">Return value</span></span>

<span data-ttu-id="681b9-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="681b9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="681b9-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="681b9-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="681b9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="681b9-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="681b9-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="681b9-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="681b9-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="681b9-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="681b9-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="681b9-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="681b9-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="681b9-120">Requirements</span></span>



| <span data-ttu-id="681b9-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="681b9-121">Requirement</span></span> | <span data-ttu-id="681b9-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="681b9-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="681b9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="681b9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="681b9-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="681b9-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="681b9-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="681b9-125">Library</span></span><br/> | <dl> <span data-ttu-id="681b9-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="681b9-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="681b9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="681b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="681b9-128">ID3DX11EffectInterfaceVariable</span><span class="sxs-lookup"><span data-stu-id="681b9-128">ID3DX11EffectInterfaceVariable</span></span>](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





