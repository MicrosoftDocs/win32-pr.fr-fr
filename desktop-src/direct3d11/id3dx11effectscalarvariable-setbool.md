---
title: Méthode ID3DX11EffectScalarVariable SetBool (D3dx11effect. h)
description: Définissez une variable booléenne.
ms.assetid: b5385ed3-6e65-4d65-bb8e-835967e6f610
keywords:
- Méthode SetBool Direct3D 11
- Méthode SetBool Direct3D 11, interface ID3DX11EffectScalarVariable
- Interface ID3DX11EffectScalarVariable Direct3D 11, méthode SetBool
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e1d3670b3a41f47bf1b5ec7ac3d2fb93441e72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974651"
---
# <a name="id3dx11effectscalarvariablesetbool-method"></a><span data-ttu-id="b970b-106">ID3DX11EffectScalarVariable :: SetBool, méthode</span><span class="sxs-lookup"><span data-stu-id="b970b-106">ID3DX11EffectScalarVariable::SetBool method</span></span>

<span data-ttu-id="b970b-107">Définissez une variable booléenne.</span><span class="sxs-lookup"><span data-stu-id="b970b-107">Set a boolean variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b970b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b970b-108">Syntax</span></span>


```C++
HRESULT SetBool(
   BOOL Value
);
```



## <a name="parameters"></a><span data-ttu-id="b970b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b970b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b970b-110">*Valeur*</span><span class="sxs-lookup"><span data-stu-id="b970b-110">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="b970b-111">Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b970b-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b970b-112">Pointeur vers la variable.</span><span class="sxs-lookup"><span data-stu-id="b970b-112">A pointer to the variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b970b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b970b-113">Return value</span></span>

<span data-ttu-id="b970b-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b970b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b970b-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="b970b-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b970b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b970b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b970b-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="b970b-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b970b-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="b970b-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b970b-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b970b-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b970b-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b970b-120">Requirements</span></span>



| <span data-ttu-id="b970b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b970b-121">Requirement</span></span> | <span data-ttu-id="b970b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b970b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b970b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b970b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b970b-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b970b-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b970b-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b970b-125">Library</span></span><br/> | <dl> <span data-ttu-id="b970b-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="b970b-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b970b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b970b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b970b-128">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="b970b-128">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

