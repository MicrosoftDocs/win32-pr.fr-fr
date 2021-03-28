---
title: Méthode ID3DX11ThreadPump WaitForAllItems (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Attend la fin de l’exécution de tous les éléments de travail de la pompe de thread.'
ms.assetid: 6dfdaee8-e563-4c37-a2c1-4b115e29c434
keywords:
- Méthode WaitForAllItems Direct3D 11
- Méthode WaitForAllItems Direct3D 11, interface ID3DX11ThreadPump
- Interface ID3DX11ThreadPump Direct3D 11, méthode WaitForAllItems
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.WaitForAllItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40abbab67d6743be2190d5e81c733f63b52b32f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992229"
---
# <a name="id3dx11threadpumpwaitforallitems-method"></a><span data-ttu-id="170d8-107">ID3DX11ThreadPump :: WaitForAllItems, méthode</span><span class="sxs-lookup"><span data-stu-id="170d8-107">ID3DX11ThreadPump::WaitForAllItems method</span></span>

> [!Note]  
> <span data-ttu-id="170d8-108">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="170d8-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="170d8-109">Attend la fin de l’exécution de tous les éléments de travail de la pompe de thread.</span><span class="sxs-lookup"><span data-stu-id="170d8-109">Waits for all work items in the thread pump to finish.</span></span>

## <a name="syntax"></a><span data-ttu-id="170d8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="170d8-110">Syntax</span></span>


```C++
HRESULT WaitForAllItems();
```



## <a name="parameters"></a><span data-ttu-id="170d8-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="170d8-111">Parameters</span></span>

<span data-ttu-id="170d8-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="170d8-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="170d8-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="170d8-113">Return value</span></span>

<span data-ttu-id="170d8-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="170d8-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="170d8-115">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="170d8-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="170d8-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="170d8-116">Requirements</span></span>



| <span data-ttu-id="170d8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="170d8-117">Requirement</span></span> | <span data-ttu-id="170d8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="170d8-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="170d8-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="170d8-119">Header</span></span><br/>  | <dl> <span data-ttu-id="170d8-120"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="170d8-120"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="170d8-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="170d8-121">Library</span></span><br/> | <dl> <span data-ttu-id="170d8-122"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="170d8-122"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="170d8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="170d8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="170d8-124">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="170d8-124">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="170d8-125">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="170d8-125">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





