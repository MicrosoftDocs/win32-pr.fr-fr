---
title: D3DPERF_GetStatus fonction)
description: Déterminez l’état actuel du profileur à partir du programme cible.
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
- D3DPERF_GetStatus
targetos: Windows
ms.openlocfilehash: 626d56dd449b0a0aa92e85c82dabda119900680d
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104314467"
---
# <a name="d3dperf_getstatus-function"></a><span data-ttu-id="11c60-103">D3DPERF_GetStatus fonction)</span><span class="sxs-lookup"><span data-stu-id="11c60-103">D3DPERF_GetStatus function</span></span>

<span data-ttu-id="11c60-104">Déterminez l’état actuel du profileur à partir du programme cible.</span><span class="sxs-lookup"><span data-stu-id="11c60-104">Determine the current state of the profiler from the target program.</span></span>

## <a name="syntax"></a><span data-ttu-id="11c60-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11c60-105">Syntax</span></span>

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a><span data-ttu-id="11c60-106">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="11c60-106">Return value</span></span>

<span data-ttu-id="11c60-107">Valeur différente de zéro quand PIX Profile le programme cible ; Sinon, zéro.</span><span class="sxs-lookup"><span data-stu-id="11c60-107">A non-zero value when PIX is profiling the target program; otherwise, zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="11c60-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11c60-108">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="11c60-109">**Plateforme cible**</span><span class="sxs-lookup"><span data-stu-id="11c60-109">**Target Platform**</span></span> | <span data-ttu-id="11c60-110">Windows</span><span class="sxs-lookup"><span data-stu-id="11c60-110">Windows</span></span> |
| <span data-ttu-id="11c60-111">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="11c60-111">**Header**</span></span> | <span data-ttu-id="11c60-112">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="11c60-112">d3d9.h</span></span> |
| <span data-ttu-id="11c60-113">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="11c60-113">**Library**</span></span> | <span data-ttu-id="11c60-114">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="11c60-114">d3d9.lib</span></span> |
| <span data-ttu-id="11c60-115">**DLL**</span><span class="sxs-lookup"><span data-stu-id="11c60-115">**DLL**</span></span> | <span data-ttu-id="11c60-116">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="11c60-116">d3d9.dll</span></span> |