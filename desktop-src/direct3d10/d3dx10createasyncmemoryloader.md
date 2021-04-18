---
description: Créez un chargeur de mémoire asynchrone.
ms.assetid: 92177390-cb09-445e-9828-806a23ef91b5
title: D3DX10CreateAsyncMemoryLoader, fonction (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncMemoryLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 0219026eabfcff6dfcec0df4721716302f09f5e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522761"
---
# <a name="d3dx10createasyncmemoryloader-function"></a><span data-ttu-id="ed4bf-103">D3DX10CreateAsyncMemoryLoader fonction)</span><span class="sxs-lookup"><span data-stu-id="ed4bf-103">D3DX10CreateAsyncMemoryLoader function</span></span>

<span data-ttu-id="ed4bf-104">Créez un chargeur de mémoire asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ed4bf-104">Create an asynchronous-memory loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed4bf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed4bf-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="ed4bf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed4bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed4bf-107">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed4bf-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed4bf-108">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed4bf-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed4bf-109">Pointeur vers les données.</span><span class="sxs-lookup"><span data-stu-id="ed4bf-109">Pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="ed4bf-110">*cbData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed4bf-110">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed4bf-111">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed4bf-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed4bf-112">Taille des données.</span><span class="sxs-lookup"><span data-stu-id="ed4bf-112">Size of the data.</span></span>

</dd> <dt>

<span data-ttu-id="ed4bf-113">*ppDataLoader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ed4bf-113">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed4bf-114">Type : **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ed4bf-114">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="ed4bf-115">Adresse d’un pointeur vers le processeur de données asynchrones (voir [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="ed4bf-115">The address of a pointer to the asynchronous-data processor (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed4bf-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed4bf-116">Return value</span></span>

<span data-ttu-id="ed4bf-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed4bf-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed4bf-118">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ed4bf-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed4bf-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed4bf-119">Requirements</span></span>



| <span data-ttu-id="ed4bf-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed4bf-120">Requirement</span></span> | <span data-ttu-id="ed4bf-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed4bf-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed4bf-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ed4bf-122">Header</span></span><br/> | <dl> <span data-ttu-id="ed4bf-123"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed4bf-123"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed4bf-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed4bf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed4bf-125">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="ed4bf-125">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
