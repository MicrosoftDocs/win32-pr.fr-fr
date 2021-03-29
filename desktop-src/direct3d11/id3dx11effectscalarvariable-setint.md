---
title: ID3DX11EffectScalarVariable setInt, méthode (D3dx11effect. h)
description: Définissez une variable de type entier.
ms.assetid: 614284be-8f70-4d7e-b797-b67e813615ab
keywords:
- SetInt, méthode Direct3D 11
- SetInt, méthode Direct3D 11, interface ID3DX11EffectScalarVariable
- Interface ID3DX11EffectScalarVariable Direct3D 11, méthode setInt
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetInt
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4e2f44a3b67db12bd84f5dd23426c033b99b57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211695"
---
# <a name="id3dx11effectscalarvariablesetint-method"></a><span data-ttu-id="b7136-106">ID3DX11EffectScalarVariable :: setInt, méthode</span><span class="sxs-lookup"><span data-stu-id="b7136-106">ID3DX11EffectScalarVariable::SetInt method</span></span>

<span data-ttu-id="b7136-107">Définissez une variable de type entier.</span><span class="sxs-lookup"><span data-stu-id="b7136-107">Set an integer variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7136-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7136-108">Syntax</span></span>


```C++
HRESULT SetInt(
   int Value
);
```



## <a name="parameters"></a><span data-ttu-id="b7136-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7136-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7136-110">*Valeur*</span><span class="sxs-lookup"><span data-stu-id="b7136-110">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="b7136-111">Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b7136-111">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b7136-112">Pointeur vers la variable.</span><span class="sxs-lookup"><span data-stu-id="b7136-112">A pointer to the variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7136-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7136-113">Return value</span></span>

<span data-ttu-id="b7136-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7136-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7136-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="b7136-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b7136-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b7136-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b7136-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="b7136-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b7136-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="b7136-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b7136-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b7136-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b7136-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b7136-120">Requirements</span></span>



| <span data-ttu-id="b7136-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7136-121">Requirement</span></span> | <span data-ttu-id="b7136-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7136-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7136-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7136-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b7136-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7136-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b7136-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b7136-125">Library</span></span><br/> | <dl> <span data-ttu-id="b7136-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="b7136-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7136-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7136-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7136-128">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="b7136-128">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

