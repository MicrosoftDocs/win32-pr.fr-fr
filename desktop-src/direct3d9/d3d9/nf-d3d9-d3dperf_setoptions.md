---
title: D3DPERF_SetOptions fonction)
description: Définissez les options du profileur spécifiées par le programme cible.
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
- D3DPERF_SetOptions
targetos: Windows
ms.openlocfilehash: 8bd877469864ccdaa833ce80d00eb06ae5fc18de
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104462754"
---
# <a name="d3dperf_setoptions-function"></a><span data-ttu-id="2c08a-103">D3DPERF_SetOptions fonction)</span><span class="sxs-lookup"><span data-stu-id="2c08a-103">D3DPERF_SetOptions function</span></span>

<span data-ttu-id="2c08a-104">Définissez les options du profileur spécifiées par le programme cible.</span><span class="sxs-lookup"><span data-stu-id="2c08a-104">Set profiler options specified by the target program.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c08a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c08a-105">Syntax</span></span>

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a><span data-ttu-id="2c08a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c08a-106">Parameters</span></span>

`dwOptions`

<span data-ttu-id="2c08a-107">Options utilisateur reconnaissables par PIX.</span><span class="sxs-lookup"><span data-stu-id="2c08a-107">User options recognizable by PIX.</span></span> <span data-ttu-id="2c08a-108">Affectez-lui la valeur 1 pour indiquer à PIX que le programme cible n’accorde pas l’autorisation d’être profilée.</span><span class="sxs-lookup"><span data-stu-id="2c08a-108">Set this to 1 to notify PIX that the target program does not give permission to be profiled.</span></span>

## <a name="return-value"></a><span data-ttu-id="2c08a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c08a-109">Return value</span></span>

<span data-ttu-id="2c08a-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2c08a-110">This function doesn't return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c08a-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c08a-111">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2c08a-112">**Plateforme cible**</span><span class="sxs-lookup"><span data-stu-id="2c08a-112">**Target Platform**</span></span> | <span data-ttu-id="2c08a-113">Windows</span><span class="sxs-lookup"><span data-stu-id="2c08a-113">Windows</span></span> |
| <span data-ttu-id="2c08a-114">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="2c08a-114">**Header**</span></span> | <span data-ttu-id="2c08a-115">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="2c08a-115">d3d9.h</span></span> |
| <span data-ttu-id="2c08a-116">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="2c08a-116">**Library**</span></span> | <span data-ttu-id="2c08a-117">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="2c08a-117">d3d9.lib</span></span> |
| <span data-ttu-id="2c08a-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="2c08a-118">**DLL**</span></span> | <span data-ttu-id="2c08a-119">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="2c08a-119">d3d9.dll</span></span> |