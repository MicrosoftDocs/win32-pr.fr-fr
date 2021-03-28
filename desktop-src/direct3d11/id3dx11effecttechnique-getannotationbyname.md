---
title: Méthode ID3DX11EffectTechnique GetAnnotationByName (D3dx11effect. h)
description: Obtient une annotation par nom. | Méthode ID3DX11EffectTechnique GetAnnotationByName (D3dx11effect. h)
ms.assetid: 3a9e1fa7-4586-42d6-a723-3140f29a01b4
keywords:
- Méthode GetAnnotationByName Direct3D 11
- Méthode GetAnnotationByName Direct3D 11, interface ID3DX11EffectTechnique
- Interface ID3DX11EffectTechnique Direct3D 11, méthode GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae5a7c24d392bd034dfcd69fb67723c9492f982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323026"
---
# <a name="id3dx11effecttechniquegetannotationbyname-method"></a><span data-ttu-id="d4aac-107">ID3DX11EffectTechnique :: GetAnnotationByName, méthode</span><span class="sxs-lookup"><span data-stu-id="d4aac-107">ID3DX11EffectTechnique::GetAnnotationByName method</span></span>

<span data-ttu-id="d4aac-108">Obtient une annotation par nom.</span><span class="sxs-lookup"><span data-stu-id="d4aac-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4aac-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4aac-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="d4aac-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4aac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4aac-111">*Nom*</span><span class="sxs-lookup"><span data-stu-id="d4aac-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="d4aac-112">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4aac-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d4aac-113">Nom de l’annotation.</span><span class="sxs-lookup"><span data-stu-id="d4aac-113">Name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4aac-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4aac-114">Return value</span></span>

<span data-ttu-id="d4aac-115">Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4aac-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="d4aac-116">Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="d4aac-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4aac-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d4aac-117">Remarks</span></span>

<span data-ttu-id="d4aac-118">Utilisez une annotation pour attacher un élément de métadonnées à une technique.</span><span class="sxs-lookup"><span data-stu-id="d4aac-118">Use an annotation to attach a piece of metadata to a technique.</span></span>

> [!Note]  
> <span data-ttu-id="d4aac-119">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="d4aac-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d4aac-120">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="d4aac-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d4aac-121">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d4aac-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d4aac-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d4aac-122">Requirements</span></span>



| <span data-ttu-id="d4aac-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4aac-123">Requirement</span></span> | <span data-ttu-id="d4aac-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4aac-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aac-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4aac-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d4aac-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4aac-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d4aac-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4aac-127">Library</span></span><br/> | <dl> <span data-ttu-id="d4aac-128"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="d4aac-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4aac-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4aac-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4aac-130">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="d4aac-130">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

