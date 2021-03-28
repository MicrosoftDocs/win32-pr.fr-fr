---
title: ID3DX11EffectVariable IsValid, méthode (D3dx11effect. h)
description: Comparez le type de données avec les données stockées.
ms.assetid: 3384afa3-6ae5-4c7c-b95d-4fe3c87cc2fe
keywords:
- Méthode IsValid Direct3D 11
- Méthode IsValid Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5136005e675a6f5e54cc3863ef2d80ffadfb7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996136"
---
# <a name="id3dx11effectvariableisvalid-method"></a><span data-ttu-id="9a954-106">ID3DX11EffectVariable :: IsValid, méthode</span><span class="sxs-lookup"><span data-stu-id="9a954-106">ID3DX11EffectVariable::IsValid method</span></span>

<span data-ttu-id="9a954-107">Comparez le type de données avec les données stockées.</span><span class="sxs-lookup"><span data-stu-id="9a954-107">Compare the data type with the data stored.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a954-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a954-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="9a954-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a954-109">Parameters</span></span>

<span data-ttu-id="9a954-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9a954-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a954-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9a954-111">Return value</span></span>

<span data-ttu-id="9a954-112">Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9a954-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9a954-113">**True** si la syntaxe est valide ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="9a954-113">**TRUE** if the syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a954-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9a954-114">Remarks</span></span>

<span data-ttu-id="9a954-115">Cette méthode vérifie que le type de données correspond aux données stockées après le cast d’une interface en une autre (à l’aide de l’une des méthodes As).</span><span class="sxs-lookup"><span data-stu-id="9a954-115">This method checks that the data type matches the data stored after casting one interface to another (using any of the As methods).</span></span>

> [!Note]  
> <span data-ttu-id="9a954-116">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="9a954-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9a954-117">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="9a954-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9a954-118">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9a954-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a954-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9a954-119">Requirements</span></span>



| <span data-ttu-id="9a954-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a954-120">Requirement</span></span> | <span data-ttu-id="9a954-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a954-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a954-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a954-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9a954-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a954-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9a954-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9a954-124">Library</span></span><br/> | <dl> <span data-ttu-id="9a954-125"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="9a954-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a954-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a954-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a954-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="9a954-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

