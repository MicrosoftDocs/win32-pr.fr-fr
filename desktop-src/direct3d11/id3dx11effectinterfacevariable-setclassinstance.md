---
title: Méthode ID3DX11EffectInterfaceVariable SetClassInstance (D3dx11effect. h)
description: Définit une instance de classe.
ms.assetid: fc71a0d2-054a-48ed-86a5-54cf0017062a
keywords:
- Méthode SetClassInstance Direct3D 11
- Méthode SetClassInstance Direct3D 11, interface ID3DX11EffectInterfaceVariable
- Interface ID3DX11EffectInterfaceVariable Direct3D 11, méthode SetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.SetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03d319d55b073393ff511b2e072aa07c244e5a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974559"
---
# <a name="id3dx11effectinterfacevariablesetclassinstance-method"></a><span data-ttu-id="54cf9-106">ID3DX11EffectInterfaceVariable :: SetClassInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="54cf9-106">ID3DX11EffectInterfaceVariable::SetClassInstance method</span></span>

<span data-ttu-id="54cf9-107">Définit une instance de classe.</span><span class="sxs-lookup"><span data-stu-id="54cf9-107">Sets a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="54cf9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54cf9-108">Syntax</span></span>


```C++
HRESULT SetClassInstance(
   ID3DX11EffectClassInstanceVariable *pEffectClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="54cf9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54cf9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54cf9-110">*pEffectClassInstance*</span><span class="sxs-lookup"><span data-stu-id="54cf9-110">*pEffectClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="54cf9-111">Type : **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="54cf9-111">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span></span>

<span data-ttu-id="54cf9-112">Pointeur vers une interface [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) .</span><span class="sxs-lookup"><span data-stu-id="54cf9-112">Pointer to an [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54cf9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54cf9-113">Return value</span></span>

<span data-ttu-id="54cf9-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54cf9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54cf9-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="54cf9-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="54cf9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="54cf9-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="54cf9-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="54cf9-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="54cf9-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="54cf9-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="54cf9-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="54cf9-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="54cf9-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="54cf9-120">Requirements</span></span>



| <span data-ttu-id="54cf9-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54cf9-121">Requirement</span></span> | <span data-ttu-id="54cf9-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="54cf9-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54cf9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="54cf9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="54cf9-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="54cf9-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="54cf9-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="54cf9-125">Library</span></span><br/> | <dl> <span data-ttu-id="54cf9-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="54cf9-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54cf9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54cf9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54cf9-128">ID3DX11EffectInterfaceVariable</span><span class="sxs-lookup"><span data-stu-id="54cf9-128">ID3DX11EffectInterfaceVariable</span></span>](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





