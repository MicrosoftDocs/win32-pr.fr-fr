---
title: Méthode ID3DX11EffectGroup GetAnnotationByName (D3dx11effect. h)
description: Obtient une annotation par nom. | Méthode ID3DX11EffectGroup GetAnnotationByName (D3dx11effect. h)
ms.assetid: c526a249-fb56-47bb-a0c2-b829a1da88e8
keywords:
- Méthode GetAnnotationByName Direct3D 11
- Méthode GetAnnotationByName Direct3D 11, interface ID3DX11EffectGroup
- Interface ID3DX11EffectGroup Direct3D 11, méthode GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1880983785fcfea8a4cda4aa09c8baec2cfebf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992245"
---
# <a name="id3dx11effectgroupgetannotationbyname-method"></a><span data-ttu-id="26b96-107">ID3DX11EffectGroup :: GetAnnotationByName, méthode</span><span class="sxs-lookup"><span data-stu-id="26b96-107">ID3DX11EffectGroup::GetAnnotationByName method</span></span>

<span data-ttu-id="26b96-108">Obtient une annotation par nom.</span><span class="sxs-lookup"><span data-stu-id="26b96-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="26b96-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26b96-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="26b96-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26b96-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26b96-111">*Nom*</span><span class="sxs-lookup"><span data-stu-id="26b96-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="26b96-112">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="26b96-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="26b96-113">Nom de l’annotation.</span><span class="sxs-lookup"><span data-stu-id="26b96-113">The name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26b96-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26b96-114">Return value</span></span>

<span data-ttu-id="26b96-115">Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="26b96-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="26b96-116">Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="26b96-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="26b96-117">Notez que si l’annotation est introuvable, le **ID3DX11EffectVariable** retourné est vide.</span><span class="sxs-lookup"><span data-stu-id="26b96-117">Note that if the annotation is not found the **ID3DX11EffectVariable** returned will be empty.</span></span> <span data-ttu-id="26b96-118">La méthode [**ID3DX11EffectVariable :: IsValid**](id3dx11effectvariable-isvalid.md) doit être appelée pour déterminer si l’annotation a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="26b96-118">The [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) method should be called to determine whether the annotation was found.</span></span>

## <a name="remarks"></a><span data-ttu-id="26b96-119">Notes</span><span class="sxs-lookup"><span data-stu-id="26b96-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="26b96-120">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="26b96-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="26b96-121">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="26b96-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="26b96-122">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="26b96-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="26b96-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="26b96-123">Requirements</span></span>



| <span data-ttu-id="26b96-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26b96-124">Requirement</span></span> | <span data-ttu-id="26b96-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="26b96-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26b96-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="26b96-126">Header</span></span><br/>  | <dl> <span data-ttu-id="26b96-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="26b96-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="26b96-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="26b96-128">Library</span></span><br/> | <dl> <span data-ttu-id="26b96-129"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="26b96-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26b96-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26b96-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26b96-131">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="26b96-131">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

