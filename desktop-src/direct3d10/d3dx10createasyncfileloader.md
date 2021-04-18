---
description: Créez un chargeur de fichiers asynchrones.
ms.assetid: 1b79fba5-e7f0-4160-9cec-ffea94f84fde
title: D3DX10CreateAsyncFileLoader, fonction (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncFileLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e98bccf709fa4a6d921e266148b94fd8623429ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522582"
---
# <a name="d3dx10createasyncfileloader-function"></a><span data-ttu-id="534cd-103">D3DX10CreateAsyncFileLoader fonction)</span><span class="sxs-lookup"><span data-stu-id="534cd-103">D3DX10CreateAsyncFileLoader function</span></span>

<span data-ttu-id="534cd-104">Créez un chargeur de fichiers asynchrones.</span><span class="sxs-lookup"><span data-stu-id="534cd-104">Create an asynchronous-file loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="534cd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="534cd-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="534cd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="534cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="534cd-107">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="534cd-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="534cd-108">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="534cd-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="534cd-109">Nom du fichier à charger.</span><span class="sxs-lookup"><span data-stu-id="534cd-109">The name of the file to load.</span></span> <span data-ttu-id="534cd-110">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="534cd-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="534cd-111">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="534cd-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="534cd-112">*ppDataLoader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="534cd-112">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="534cd-113">Type : **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="534cd-113">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="534cd-114">Adresse d’un pointeur vers le chargeur de données asynchrones (voir [**interface ID3DX10DataLoader**](id3dx10dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="534cd-114">Address of a pointer to the asynchronous-data loader (see [**ID3DX10DataLoader Interface**](id3dx10dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="534cd-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="534cd-115">Return value</span></span>

<span data-ttu-id="534cd-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="534cd-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="534cd-117">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="534cd-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="534cd-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="534cd-118">Requirements</span></span>



| <span data-ttu-id="534cd-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="534cd-119">Requirement</span></span> | <span data-ttu-id="534cd-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="534cd-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="534cd-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="534cd-121">Header</span></span><br/> | <dl> <span data-ttu-id="534cd-122"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="534cd-122"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="534cd-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="534cd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="534cd-124">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="534cd-124">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
