---
title: Méthode ID3DX11EffectVariable GetAnnotationByName (D3dx11effect. h)
description: Obtient une annotation par nom. | Méthode ID3DX11EffectVariable GetAnnotationByName (D3dx11effect. h)
ms.assetid: 0ca3df07-c721-48c4-9422-f6af24acbaef
keywords:
- Méthode GetAnnotationByName Direct3D 11
- Méthode GetAnnotationByName Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37efcd773728e563a4112f61a7c6c965d05bad4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323025"
---
# <a name="id3dx11effectvariablegetannotationbyname-method"></a><span data-ttu-id="b7bf2-107">ID3DX11EffectVariable :: GetAnnotationByName, méthode</span><span class="sxs-lookup"><span data-stu-id="b7bf2-107">ID3DX11EffectVariable::GetAnnotationByName method</span></span>

<span data-ttu-id="b7bf2-108">Obtient une annotation par nom.</span><span class="sxs-lookup"><span data-stu-id="b7bf2-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7bf2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7bf2-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="b7bf2-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7bf2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7bf2-111">*Nom*</span><span class="sxs-lookup"><span data-stu-id="b7bf2-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="b7bf2-112">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b7bf2-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b7bf2-113">Nom de l’annotation.</span><span class="sxs-lookup"><span data-stu-id="b7bf2-113">The annotation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7bf2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7bf2-114">Return value</span></span>

<span data-ttu-id="b7bf2-115">Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="b7bf2-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="b7bf2-116">Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="b7bf2-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="b7bf2-117">Notez que si l’annotation est introuvable, le **ID3DX11EffectVariable** retourné est vide.</span><span class="sxs-lookup"><span data-stu-id="b7bf2-117">Note that if the annotation is not found the **ID3DX11EffectVariable** returned will be empty.</span></span> <span data-ttu-id="b7bf2-118">La méthode [**ID3DX11EffectVariable :: IsValid**](id3dx11effectvariable-isvalid.md) doit être appelée pour déterminer si l’annotation a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="b7bf2-118">The [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) method should be called to determine whether the annotation was found.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7bf2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b7bf2-119">Remarks</span></span>

<span data-ttu-id="b7bf2-120">Annonations peut être attaché à une technique, à une passe ou à une variable globale.</span><span class="sxs-lookup"><span data-stu-id="b7bf2-120">Annonations can be attached to a technique, a pass, or a global variable.</span></span>

> [!Note]  
> <span data-ttu-id="b7bf2-121">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="b7bf2-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b7bf2-122">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="b7bf2-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b7bf2-123">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b7bf2-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b7bf2-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b7bf2-124">Requirements</span></span>



| <span data-ttu-id="b7bf2-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7bf2-125">Requirement</span></span> | <span data-ttu-id="b7bf2-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7bf2-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7bf2-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7bf2-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b7bf2-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7bf2-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b7bf2-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b7bf2-129">Library</span></span><br/> | <dl> <span data-ttu-id="b7bf2-130"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="b7bf2-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7bf2-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7bf2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7bf2-132">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="b7bf2-132">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

