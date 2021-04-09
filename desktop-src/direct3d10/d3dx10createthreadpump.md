---
description: Créer une pompe de thread.
ms.assetid: a7a016e2-784d-4d7a-8058-88895bf3c4e2
title: D3DX10CreateThreadPump, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateThreadPump
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a27f8df1f4eaa8e7f41e863d703063308f9c595
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953971"
---
# <a name="d3dx10createthreadpump-function"></a><span data-ttu-id="ef145-103">D3DX10CreateThreadPump fonction)</span><span class="sxs-lookup"><span data-stu-id="ef145-103">D3DX10CreateThreadPump function</span></span>

<span data-ttu-id="ef145-104">Créer une pompe de thread.</span><span class="sxs-lookup"><span data-stu-id="ef145-104">Create a thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef145-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef145-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX10ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a><span data-ttu-id="ef145-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef145-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef145-107">*cIoThreads* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef145-107">*cIoThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef145-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef145-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ef145-109">Nombre de threads d’e/s à créer.</span><span class="sxs-lookup"><span data-stu-id="ef145-109">The number of I/O threads to create.</span></span> <span data-ttu-id="ef145-110">Si la valeur 0 est spécifiée, Direct3D tente de calculer le nombre optimal de threads en fonction de la configuration matérielle.</span><span class="sxs-lookup"><span data-stu-id="ef145-110">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="ef145-111">*cProcThreads* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef145-111">*cProcThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef145-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef145-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ef145-113">Nombre de threads de processus à créer.</span><span class="sxs-lookup"><span data-stu-id="ef145-113">The number of process threads to create.</span></span> <span data-ttu-id="ef145-114">Si la valeur 0 est spécifiée, Direct3D tente de calculer le nombre optimal de threads en fonction de la configuration matérielle.</span><span class="sxs-lookup"><span data-stu-id="ef145-114">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="ef145-115">*ppThreadPump* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ef145-115">*ppThreadPump* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef145-116">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ef145-116">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***</span></span>

<span data-ttu-id="ef145-117">Pompe de thread créée.</span><span class="sxs-lookup"><span data-stu-id="ef145-117">The created thread pump.</span></span> <span data-ttu-id="ef145-118">Voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="ef145-118">See [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef145-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef145-119">Return value</span></span>

<span data-ttu-id="ef145-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef145-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef145-121">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ef145-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef145-122">Notes</span><span class="sxs-lookup"><span data-stu-id="ef145-122">Remarks</span></span>

<span data-ttu-id="ef145-123">Une pompe de thread est un objet très gourmand en ressources.</span><span class="sxs-lookup"><span data-stu-id="ef145-123">A thread pump is a very resource-intensive object.</span></span> <span data-ttu-id="ef145-124">Une seule pompe de threads doit être créée par application.</span><span class="sxs-lookup"><span data-stu-id="ef145-124">Only one thread pump should be created per application.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef145-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef145-125">Requirements</span></span>



| <span data-ttu-id="ef145-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef145-126">Requirement</span></span> | <span data-ttu-id="ef145-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef145-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef145-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef145-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ef145-129"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef145-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef145-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef145-130">Library</span></span><br/> | <dl> <span data-ttu-id="ef145-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef145-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef145-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef145-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef145-133">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="ef145-133">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
