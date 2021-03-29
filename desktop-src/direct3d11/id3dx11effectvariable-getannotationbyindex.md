---
title: Méthode ID3DX11EffectVariable GetAnnotationByIndex (D3dx11effect. h)
description: Obtient une annotation par index. | Méthode ID3DX11EffectVariable GetAnnotationByIndex (D3dx11effect. h)
ms.assetid: fc130098-0269-4c78-bc45-284aa0b77865
keywords:
- Méthode GetAnnotationByIndex Direct3D 11
- Méthode GetAnnotationByIndex Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e13cfcb27e94c64af132e5eec600941d0b41cd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116178"
---
# <a name="id3dx11effectvariablegetannotationbyindex-method"></a><span data-ttu-id="4b29f-107">ID3DX11EffectVariable :: GetAnnotationByIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="4b29f-107">ID3DX11EffectVariable::GetAnnotationByIndex method</span></span>

<span data-ttu-id="4b29f-108">Obtient une annotation par index.</span><span class="sxs-lookup"><span data-stu-id="4b29f-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b29f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b29f-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="4b29f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b29f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b29f-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="4b29f-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="4b29f-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4b29f-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4b29f-113">Index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="4b29f-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b29f-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b29f-114">Return value</span></span>

<span data-ttu-id="4b29f-115">Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="4b29f-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="4b29f-116">Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="4b29f-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4b29f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4b29f-117">Remarks</span></span>

<span data-ttu-id="4b29f-118">Annonations peut être attaché à une technique, à une passe ou à une variable globale.</span><span class="sxs-lookup"><span data-stu-id="4b29f-118">Annonations can be attached to a technique, a pass, or a global variable.</span></span>

> [!Note]  
> <span data-ttu-id="4b29f-119">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="4b29f-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4b29f-120">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="4b29f-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4b29f-121">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4b29f-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4b29f-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4b29f-122">Requirements</span></span>



| <span data-ttu-id="4b29f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b29f-123">Requirement</span></span> | <span data-ttu-id="4b29f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b29f-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b29f-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="4b29f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4b29f-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b29f-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4b29f-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4b29f-127">Library</span></span><br/> | <dl> <span data-ttu-id="4b29f-128"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="4b29f-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b29f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b29f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b29f-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="4b29f-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

