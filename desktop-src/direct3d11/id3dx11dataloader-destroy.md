---
title: ID3DX11DataLoader Destroy, méthode (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Détruit le chargeur après l’achèvement d’un élément de travail.'
ms.assetid: 5d86c4ad-3eb6-421f-bb77-c88e8f5b42bb
keywords:
- Méthode Destroy Direct3D 11
- Méthode Destroy Direct3D 11, interface ID3DX11DataLoader
- ID3DX11DataLoader interface Direct3D 11, Destroy, méthode
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Destroy
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c3a1c6511a00d66704c104b3b69150a8509e41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982610"
---
# <a name="id3dx11dataloaderdestroy-method"></a><span data-ttu-id="3442b-107">ID3DX11DataLoader ::D méthode estroy</span><span class="sxs-lookup"><span data-stu-id="3442b-107">ID3DX11DataLoader::Destroy method</span></span>

> [!Note]  
> <span data-ttu-id="3442b-108">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="3442b-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="3442b-109">Détruit le chargeur après l’achèvement d’un élément de travail.</span><span class="sxs-lookup"><span data-stu-id="3442b-109">Destroys the loader after a work item completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3442b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3442b-110">Syntax</span></span>


```C++
HRESULT Destroy();
```



## <a name="parameters"></a><span data-ttu-id="3442b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3442b-111">Parameters</span></span>

<span data-ttu-id="3442b-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3442b-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3442b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3442b-113">Return value</span></span>

<span data-ttu-id="3442b-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3442b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3442b-115">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3442b-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3442b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="3442b-116">Remarks</span></span>

<span data-ttu-id="3442b-117">Cette méthode est utilisée par une [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="3442b-117">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3442b-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3442b-118">Requirements</span></span>



| <span data-ttu-id="3442b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3442b-119">Requirement</span></span> | <span data-ttu-id="3442b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3442b-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3442b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3442b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3442b-122"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3442b-122"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="3442b-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3442b-123">Library</span></span><br/> | <dl> <span data-ttu-id="3442b-124"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3442b-124"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3442b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3442b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3442b-126">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="3442b-126">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="3442b-127">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="3442b-127">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





