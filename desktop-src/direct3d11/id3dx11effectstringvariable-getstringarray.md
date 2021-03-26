---
title: Méthode ID3DX11EffectStringVariable GetStringArray (D3dx11effect. h)
description: Obtient un tableau de chaînes.
ms.assetid: 2cc45b2f-1851-49d2-8844-3e249c48f327
keywords:
- Méthode GetStringArray Direct3D 11
- Méthode GetStringArray Direct3D 11, interface ID3DX11EffectStringVariable
- Interface ID3DX11EffectStringVariable Direct3D 11, méthode GetStringArray
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetStringArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2050ebd7c9ae3735385a379e6ef7bdff0e1cfd6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974470"
---
# <a name="id3dx11effectstringvariablegetstringarray-method"></a><span data-ttu-id="b6c4e-106">ID3DX11EffectStringVariable :: GetStringArray, méthode</span><span class="sxs-lookup"><span data-stu-id="b6c4e-106">ID3DX11EffectStringVariable::GetStringArray method</span></span>

<span data-ttu-id="b6c4e-107">Obtient un tableau de chaînes.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-107">Get an array of strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c4e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6c4e-108">Syntax</span></span>


```C++
HRESULT GetStringArray(
   LPCSTR *ppStrings,
   UINT   Offset,
   UINT   Count
);
```



## <a name="parameters"></a><span data-ttu-id="b6c4e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6c4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6c4e-110">*ppStrings*</span><span class="sxs-lookup"><span data-stu-id="b6c4e-110">*ppStrings*</span></span> 
</dt> <dd>

<span data-ttu-id="b6c4e-111">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="b6c4e-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="b6c4e-112">Pointeur vers la première chaîne dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-112">A pointer to the first string in the array.</span></span>

</dd> <dt>

<span data-ttu-id="b6c4e-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="b6c4e-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="b6c4e-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b6c4e-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b6c4e-115">Décalage (en nombre de chaînes) entre le début du tableau et la première chaîne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-115">The offset (in number of strings) between the start of the array and the first string to get.</span></span>

</dd> <dt>

<span data-ttu-id="b6c4e-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="b6c4e-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="b6c4e-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b6c4e-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b6c4e-118">Nombre de chaînes dans le tableau retourné.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-118">The number of strings in the returned array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6c4e-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6c4e-119">Return value</span></span>

<span data-ttu-id="b6c4e-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b6c4e-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b6c4e-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b6c4e-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b6c4e-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b6c4e-123">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b6c4e-124">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="b6c4e-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b6c4e-125">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b6c4e-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b6c4e-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b6c4e-126">Requirements</span></span>



| <span data-ttu-id="b6c4e-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6c4e-127">Requirement</span></span> | <span data-ttu-id="b6c4e-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6c4e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c4e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6c4e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b6c4e-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6c4e-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b6c4e-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b6c4e-131">Library</span></span><br/> | <dl> <span data-ttu-id="b6c4e-132"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="b6c4e-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6c4e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6c4e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c4e-134">ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="b6c4e-134">ID3DX11EffectStringVariable</span></span>](id3dx11effectstringvariable.md)
</dt> </dl>

 

