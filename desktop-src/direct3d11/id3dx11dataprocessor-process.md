---
title: Méthode de processus ID3DX11DataProcessor (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Traite les données.'
ms.assetid: be20b231-9c2e-4b4a-bdb1-cdc75552bf9d
keywords:
- Méthode de traitement Direct3D 11
- Méthode de traitement Direct3D 11, interface ID3DX11DataProcessor
- Interface ID3DX11DataProcessor Direct3D 11, méthode Process
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Process
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6127d62398d212c94669fadaaa2ecb09819d0171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530951"
---
# <a name="id3dx11dataprocessorprocess-method"></a><span data-ttu-id="0d026-107">ID3DX11DataProcessor ::P méthode tionnaire</span><span class="sxs-lookup"><span data-stu-id="0d026-107">ID3DX11DataProcessor::Process method</span></span>

> [!Note]  
> <span data-ttu-id="0d026-108">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="0d026-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="0d026-109">Traite les données.</span><span class="sxs-lookup"><span data-stu-id="0d026-109">Processes data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d026-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d026-110">Syntax</span></span>


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="0d026-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d026-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d026-112">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d026-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d026-113">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="0d026-113">Type: **void\***</span></span>

<span data-ttu-id="0d026-114">Pointeur vers les données à traiter.</span><span class="sxs-lookup"><span data-stu-id="0d026-114">Pointer to the data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="0d026-115">*cBytes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d026-115">*cBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d026-116">Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0d026-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0d026-117">Taille des données à traiter.</span><span class="sxs-lookup"><span data-stu-id="0d026-117">Size of the data to be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d026-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d026-118">Return value</span></span>

<span data-ttu-id="0d026-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0d026-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0d026-120">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0d026-120">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0d026-121">Notes</span><span class="sxs-lookup"><span data-stu-id="0d026-121">Remarks</span></span>

<span data-ttu-id="0d026-122">Cette méthode est utilisée par une [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="0d026-122">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d026-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0d026-123">Requirements</span></span>



| <span data-ttu-id="0d026-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d026-124">Requirement</span></span> | <span data-ttu-id="0d026-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d026-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d026-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d026-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0d026-127"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d026-127"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="0d026-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0d026-128">Library</span></span><br/> | <dl> <span data-ttu-id="0d026-129"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d026-129"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0d026-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d026-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d026-131">ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="0d026-131">ID3DX11DataProcessor</span></span>](id3dx11dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="0d026-132">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="0d026-132">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

