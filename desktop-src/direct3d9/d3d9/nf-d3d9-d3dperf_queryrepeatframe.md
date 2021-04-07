---
title: D3DPERF_QueryRepeatFrame fonction)
description: Déterminez si un profileur de performances demande que le frame actuel soit renvoyé à Direct3D pour l’analyse des performances. Cette fonction n’est pas actuellement prise en charge par PIX.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_QueryRepeatFrame
targetos: Windows
ms.openlocfilehash: c4054a0704fd0258483ee0d3d3d555cb5eabe7f9
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2020
ms.locfileid: "103723875"
---
# <a name="d3dperf_queryrepeatframe-function"></a><span data-ttu-id="8e5d4-104">D3DPERF_QueryRepeatFrame fonction)</span><span class="sxs-lookup"><span data-stu-id="8e5d4-104">D3DPERF_QueryRepeatFrame function</span></span>

<span data-ttu-id="8e5d4-105">Déterminez si un profileur de performances demande que le frame actuel soit renvoyé à Direct3D pour l’analyse des performances.</span><span class="sxs-lookup"><span data-stu-id="8e5d4-105">Determine whether a performance profiler is requesting that the current frame be resubmitted to Direct3D for performance analysis.</span></span> <span data-ttu-id="8e5d4-106">Cette fonction n’est pas actuellement prise en charge par PIX.</span><span class="sxs-lookup"><span data-stu-id="8e5d4-106">This function is not currently supported by PIX.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e5d4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e5d4-107">Syntax</span></span>

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a><span data-ttu-id="8e5d4-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8e5d4-108">Return value</span></span>

<span data-ttu-id="8e5d4-109">Si la valeur de retour est TRUE, l’appelant doit répéter la même séquence d’appels.</span><span class="sxs-lookup"><span data-stu-id="8e5d4-109">If the return value is TRUE, the caller should repeat the same sequence of calls.</span></span> <span data-ttu-id="8e5d4-110">Si la valeur est FALSe, l’appelant doit continuer.</span><span class="sxs-lookup"><span data-stu-id="8e5d4-110">If FALSE, the caller should continue.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e5d4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8e5d4-111">Remarks</span></span>

<span data-ttu-id="8e5d4-112">La fonction doit être appelée immédiatement après **IDirect3DDevice9 ::P renvoyé** est appelé.</span><span class="sxs-lookup"><span data-stu-id="8e5d4-112">The function should be called immediately after **IDirect3DDevice9::Present** is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e5d4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e5d4-113">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8e5d4-114">**Plateforme cible**</span><span class="sxs-lookup"><span data-stu-id="8e5d4-114">**Target Platform**</span></span> | <span data-ttu-id="8e5d4-115">Windows</span><span class="sxs-lookup"><span data-stu-id="8e5d4-115">Windows</span></span> |
| <span data-ttu-id="8e5d4-116">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="8e5d4-116">**Header**</span></span> | <span data-ttu-id="8e5d4-117">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="8e5d4-117">d3d9.h</span></span> |
| <span data-ttu-id="8e5d4-118">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="8e5d4-118">**Library**</span></span> | <span data-ttu-id="8e5d4-119">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="8e5d4-119">d3d9.lib</span></span> |
| <span data-ttu-id="8e5d4-120">**DLL**</span><span class="sxs-lookup"><span data-stu-id="8e5d4-120">**DLL**</span></span> | <span data-ttu-id="8e5d4-121">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="8e5d4-121">d3d9.dll</span></span> |