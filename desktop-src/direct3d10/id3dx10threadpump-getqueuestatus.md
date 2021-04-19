---
description: Obtient le nombre d’éléments dans chacune des trois files d’attente à l’intérieur de la pompe de thread.
ms.assetid: b5b829a5-5ef7-4ef5-afb4-efe1bb22ae70
title: 'ID3DX10ThreadPump :: GetQueueStatus, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.GetQueueStatus
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4cf3b5879da0346cefbb5b8835d6922dd736cfd3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545315"
---
# <a name="id3dx10threadpumpgetqueuestatus-method"></a><span data-ttu-id="c6357-103">ID3DX10ThreadPump :: GetQueueStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="c6357-103">ID3DX10ThreadPump::GetQueueStatus method</span></span>

<span data-ttu-id="c6357-104">Obtient le nombre d’éléments dans chacune des trois files d’attente à l’intérieur de la pompe de thread.</span><span class="sxs-lookup"><span data-stu-id="c6357-104">Get the number of items in each of the three queues inside the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6357-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6357-105">Syntax</span></span>


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a><span data-ttu-id="c6357-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6357-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6357-107">*pIoQueue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6357-107">*pIoQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6357-108">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c6357-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c6357-109">Nombre d’éléments dans la file d’attente d’e/s.</span><span class="sxs-lookup"><span data-stu-id="c6357-109">Number of items in the I/O queue.</span></span>

</dd> <dt>

<span data-ttu-id="c6357-110">*pProcessQueue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6357-110">*pProcessQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6357-111">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c6357-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c6357-112">Nombre d’éléments dans la file d’attente de traitement.</span><span class="sxs-lookup"><span data-stu-id="c6357-112">Number of items in the process queue.</span></span>

</dd> <dt>

<span data-ttu-id="c6357-113">*pDeviceQueue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6357-113">*pDeviceQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6357-114">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c6357-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c6357-115">Nombre d’éléments dans la file d’attente de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c6357-115">Number of items in the device queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6357-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c6357-116">Return value</span></span>

<span data-ttu-id="c6357-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c6357-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c6357-118">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c6357-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6357-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6357-119">Requirements</span></span>



| <span data-ttu-id="c6357-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6357-120">Requirement</span></span> | <span data-ttu-id="c6357-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6357-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6357-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6357-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c6357-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6357-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6357-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c6357-124">Library</span></span><br/> | <dl> <span data-ttu-id="c6357-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6357-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6357-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6357-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6357-127">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="c6357-127">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="c6357-128">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="c6357-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
