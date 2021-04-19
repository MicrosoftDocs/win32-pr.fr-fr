---
description: Ajoutez un élément de travail à la pompe de thread.
ms.assetid: f07789dc-a3d5-4bad-9768-527e701271b8
title: 'ID3DX10ThreadPump :: AddWorkItem, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.AddWorkItem
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aaf5286ca6cf7b61b0027b176d9a9261bd0beaa8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524885"
---
# <a name="id3dx10threadpumpaddworkitem-method"></a><span data-ttu-id="2e9c0-103">ID3DX10ThreadPump :: AddWorkItem, méthode</span><span class="sxs-lookup"><span data-stu-id="2e9c0-103">ID3DX10ThreadPump::AddWorkItem method</span></span>

<span data-ttu-id="2e9c0-104">Ajoutez un élément de travail à la pompe de thread.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-104">Add a work item to the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e9c0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e9c0-105">Syntax</span></span>


```C++
HRESULT AddWorkItem(
  [in]  ID3DX10DataLoader    *pDataLoader,
  [in]  ID3DX10DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a><span data-ttu-id="2e9c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e9c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e9c0-107">*pDataLoader* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e9c0-107">*pDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9c0-108">Type : **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e9c0-108">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\***</span></span>

<span data-ttu-id="2e9c0-109">Chargeur que la pompe de threads utilisera lorsqu’un élément de travail nécessite le chargement de données.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-109">The loader that the thread pump will use when a work item requires data to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="2e9c0-110">*pDataProcessor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e9c0-110">*pDataProcessor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9c0-111">Type : **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e9c0-111">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***</span></span>

<span data-ttu-id="2e9c0-112">Processeur que la pompe de threads utilisera lorsqu’un élément de travail nécessitera un traitement des données.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-112">The processor that the thread pump will use when a work item requires data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="2e9c0-113">*pHResult* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e9c0-113">*pHResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9c0-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="2e9c0-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="2e9c0-115">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-115">A pointer to the return value.</span></span> <span data-ttu-id="2e9c0-116">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-116">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2e9c0-117">*ppDeviceObject* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2e9c0-117">*ppDeviceObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9c0-118">Type : **void \* \***</span><span class="sxs-lookup"><span data-stu-id="2e9c0-118">Type: **void\*\***</span></span>

<span data-ttu-id="2e9c0-119">Périphérique qui utilise l’objet.</span><span class="sxs-lookup"><span data-stu-id="2e9c0-119">The device that uses the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e9c0-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e9c0-120">Return value</span></span>

<span data-ttu-id="2e9c0-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2e9c0-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2e9c0-122">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2e9c0-122">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e9c0-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e9c0-123">Requirements</span></span>



| <span data-ttu-id="2e9c0-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e9c0-124">Requirement</span></span> | <span data-ttu-id="2e9c0-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e9c0-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e9c0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e9c0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2e9c0-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e9c0-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2e9c0-128">Library</span></span><br/> | <dl> <span data-ttu-id="2e9c0-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e9c0-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e9c0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e9c0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e9c0-131">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="2e9c0-131">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="2e9c0-132">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="2e9c0-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




