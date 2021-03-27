---
title: Méthode ID3DX11EffectVectorVariable SetFloatVector (D3dx11effect. h)
description: Définissez un vecteur à quatre composants qui contient des données à virgule flottante.
ms.assetid: fb646df6-b9f9-4d71-93c3-38833076b781
keywords:
- Méthode SetFloatVector Direct3D 11
- Méthode SetFloatVector Direct3D 11, interface ID3DX11EffectVectorVariable
- Interface ID3DX11EffectVectorVariable Direct3D 11, méthode SetFloatVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetFloatVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5541f2773e992c4c52bf748bceb832d67b28825
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394200"
---
# <a name="id3dx11effectvectorvariablesetfloatvector-method"></a><span data-ttu-id="0ef8c-106">ID3DX11EffectVectorVariable :: SetFloatVector, méthode</span><span class="sxs-lookup"><span data-stu-id="0ef8c-106">ID3DX11EffectVectorVariable::SetFloatVector method</span></span>

<span data-ttu-id="0ef8c-107">Définissez un vecteur à quatre composants qui contient des données à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="0ef8c-107">Set a four-component vector that contains floating-point data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef8c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ef8c-108">Syntax</span></span>


```C++
HRESULT SetFloatVector(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="0ef8c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ef8c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ef8c-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="0ef8c-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="0ef8c-111">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="0ef8c-111">Type: **float\***</span></span>

<span data-ttu-id="0ef8c-112">Pointeur vers le premier composant.</span><span class="sxs-lookup"><span data-stu-id="0ef8c-112">A pointer to the first component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ef8c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ef8c-113">Return value</span></span>

<span data-ttu-id="0ef8c-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ef8c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ef8c-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="0ef8c-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ef8c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0ef8c-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0ef8c-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="0ef8c-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0ef8c-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="0ef8c-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0ef8c-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0ef8c-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0ef8c-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0ef8c-120">Requirements</span></span>



| <span data-ttu-id="0ef8c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ef8c-121">Requirement</span></span> | <span data-ttu-id="0ef8c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ef8c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef8c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ef8c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0ef8c-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ef8c-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0ef8c-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0ef8c-125">Library</span></span><br/> | <dl> <span data-ttu-id="0ef8c-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="0ef8c-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ef8c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ef8c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef8c-128">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="0ef8c-128">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

 





