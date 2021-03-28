---
title: Méthode ID3DX11ThreadPump GetQueueStatus (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Obtient le nombre d’éléments dans chacune des trois files d’attente à l’intérieur de la pompe de thread.'
ms.assetid: 69e1c786-6c7d-4432-bf34-3bf7606a07f6
keywords:
- Méthode GetQueueStatus Direct3D 11
- Méthode GetQueueStatus Direct3D 11, interface ID3DX11ThreadPump
- Interface ID3DX11ThreadPump Direct3D 11, méthode GetQueueStatus
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetQueueStatus
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c945cb2978af15263d3f72d34a47c5e8ca8a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974531"
---
# <a name="id3dx11threadpumpgetqueuestatus-method"></a><span data-ttu-id="eb0ae-107">ID3DX11ThreadPump :: GetQueueStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="eb0ae-107">ID3DX11ThreadPump::GetQueueStatus method</span></span>

> [!Note]  
> <span data-ttu-id="eb0ae-108">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="eb0ae-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="eb0ae-109">Obtient le nombre d’éléments dans chacune des trois files d’attente à l’intérieur de la pompe de thread.</span><span class="sxs-lookup"><span data-stu-id="eb0ae-109">Gets the number of items in each of the three queues inside the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb0ae-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb0ae-110">Syntax</span></span>


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a><span data-ttu-id="eb0ae-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb0ae-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb0ae-112">*pIoQueue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb0ae-112">*pIoQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb0ae-113">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="eb0ae-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="eb0ae-114">Nombre d’éléments dans la file d’attente d’e/s.</span><span class="sxs-lookup"><span data-stu-id="eb0ae-114">Number of items in the I/O queue.</span></span>

</dd> <dt>

<span data-ttu-id="eb0ae-115">*pProcessQueue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb0ae-115">*pProcessQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb0ae-116">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="eb0ae-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="eb0ae-117">Nombre d’éléments dans la file d’attente de traitement.</span><span class="sxs-lookup"><span data-stu-id="eb0ae-117">Number of items in the process queue.</span></span>

</dd> <dt>

<span data-ttu-id="eb0ae-118">*pDeviceQueue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb0ae-118">*pDeviceQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb0ae-119">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="eb0ae-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="eb0ae-120">Nombre d’éléments dans la file d’attente de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="eb0ae-120">Number of items in the device queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb0ae-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb0ae-121">Return value</span></span>

<span data-ttu-id="eb0ae-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eb0ae-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eb0ae-123">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="eb0ae-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb0ae-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="eb0ae-124">Requirements</span></span>



| <span data-ttu-id="eb0ae-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb0ae-125">Requirement</span></span> | <span data-ttu-id="eb0ae-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb0ae-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb0ae-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb0ae-127">Header</span></span><br/>  | <dl> <span data-ttu-id="eb0ae-128"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb0ae-128"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="eb0ae-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb0ae-129">Library</span></span><br/> | <dl> <span data-ttu-id="eb0ae-130"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb0ae-130"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eb0ae-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb0ae-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb0ae-132">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="eb0ae-132">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="eb0ae-133">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="eb0ae-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

