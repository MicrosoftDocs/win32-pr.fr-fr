---
title: ID3DX11DataLoader, méthode de chargement (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Charge des données à partir d’un disque.'
ms.assetid: 21dee078-af8f-4ca1-bb2e-d4ecc0471609
keywords:
- Charger la méthode Direct3D 11
- Charger la méthode Direct3D 11, interface ID3DX11DataLoader
- Interface ID3DX11DataLoader Direct3D 11, méthode Load
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Load
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0f720a5e6884bfdf1935c6d93f7a05decae5e8a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982615"
---
# <a name="id3dx11dataloaderload-method"></a><span data-ttu-id="4eaf2-107">ID3DX11DataLoader :: Load, méthode</span><span class="sxs-lookup"><span data-stu-id="4eaf2-107">ID3DX11DataLoader::Load method</span></span>

> [!Note]  
> <span data-ttu-id="4eaf2-108">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4eaf2-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="4eaf2-109">Charge des données à partir d’un disque.</span><span class="sxs-lookup"><span data-stu-id="4eaf2-109">Loads data from a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eaf2-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4eaf2-110">Syntax</span></span>


```C++
HRESULT Load();
```



## <a name="parameters"></a><span data-ttu-id="4eaf2-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4eaf2-111">Parameters</span></span>

<span data-ttu-id="4eaf2-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4eaf2-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4eaf2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4eaf2-113">Return value</span></span>

<span data-ttu-id="4eaf2-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4eaf2-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4eaf2-115">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4eaf2-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4eaf2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="4eaf2-116">Remarks</span></span>

<span data-ttu-id="4eaf2-117">Cette méthode est utilisée par une [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="4eaf2-117">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4eaf2-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4eaf2-118">Requirements</span></span>



| <span data-ttu-id="4eaf2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4eaf2-119">Requirement</span></span> | <span data-ttu-id="4eaf2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="4eaf2-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4eaf2-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="4eaf2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4eaf2-122"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eaf2-122"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="4eaf2-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4eaf2-123">Library</span></span><br/> | <dl> <span data-ttu-id="4eaf2-124"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4eaf2-124"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4eaf2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4eaf2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eaf2-126">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="4eaf2-126">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="4eaf2-127">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="4eaf2-127">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





