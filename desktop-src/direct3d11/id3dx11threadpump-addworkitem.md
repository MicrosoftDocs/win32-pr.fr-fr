---
title: Méthode ID3DX11ThreadPump AddWorkItem (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Ajoute un élément de travail à la pompe de thread.'
ms.assetid: 2578506c-6175-457a-bf10-94929bb3c0c4
keywords:
- Méthode AddWorkItem Direct3D 11
- Méthode AddWorkItem Direct3D 11, interface ID3DX11ThreadPump
- Interface ID3DX11ThreadPump Direct3D 11, méthode AddWorkItem
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.AddWorkItem
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf249405bd71287f93444ae8d23dab694027360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322686"
---
# <a name="id3dx11threadpumpaddworkitem-method"></a><span data-ttu-id="792a3-107">ID3DX11ThreadPump :: AddWorkItem, méthode</span><span class="sxs-lookup"><span data-stu-id="792a3-107">ID3DX11ThreadPump::AddWorkItem method</span></span>

> [!Note]  
> <span data-ttu-id="792a3-108">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="792a3-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="792a3-109">Ajoute un élément de travail à la pompe de thread.</span><span class="sxs-lookup"><span data-stu-id="792a3-109">Adds a work item to the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="792a3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="792a3-110">Syntax</span></span>


```C++
HRESULT AddWorkItem(
  [in]  ID3DX11DataLoader    *pDataLoader,
  [in]  ID3DX11DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a><span data-ttu-id="792a3-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="792a3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="792a3-112">*pDataLoader* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="792a3-112">*pDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="792a3-113">Type : **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\***</span><span class="sxs-lookup"><span data-stu-id="792a3-113">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\***</span></span>

<span data-ttu-id="792a3-114">Chargeur que la pompe de threads utilisera lorsqu’un élément de travail nécessite le chargement de données.</span><span class="sxs-lookup"><span data-stu-id="792a3-114">The loader that the thread pump will use when a work item requires data to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="792a3-115">*pDataProcessor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="792a3-115">*pDataProcessor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="792a3-116">Type : **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***</span><span class="sxs-lookup"><span data-stu-id="792a3-116">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***</span></span>

<span data-ttu-id="792a3-117">Processeur que la pompe de threads utilisera lorsqu’un élément de travail nécessitera un traitement des données.</span><span class="sxs-lookup"><span data-stu-id="792a3-117">The processor that the thread pump will use when a work item requires data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="792a3-118">*pHResult* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="792a3-118">*pHResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="792a3-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="792a3-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="792a3-120">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="792a3-120">A pointer to the return value.</span></span> <span data-ttu-id="792a3-121">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="792a3-121">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="792a3-122">*ppDeviceObject* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="792a3-122">*ppDeviceObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="792a3-123">Type : **void \* \***</span><span class="sxs-lookup"><span data-stu-id="792a3-123">Type: **void\*\***</span></span>

<span data-ttu-id="792a3-124">Périphérique qui utilise l’objet.</span><span class="sxs-lookup"><span data-stu-id="792a3-124">The device that uses the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="792a3-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="792a3-125">Return value</span></span>

<span data-ttu-id="792a3-126">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="792a3-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="792a3-127">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="792a3-127">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="792a3-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="792a3-128">Requirements</span></span>



| <span data-ttu-id="792a3-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="792a3-129">Requirement</span></span> | <span data-ttu-id="792a3-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="792a3-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="792a3-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="792a3-131">Header</span></span><br/>  | <dl> <span data-ttu-id="792a3-132"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="792a3-132"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="792a3-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="792a3-133">Library</span></span><br/> | <dl> <span data-ttu-id="792a3-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="792a3-134"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="792a3-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="792a3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="792a3-136">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="792a3-136">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="792a3-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="792a3-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





