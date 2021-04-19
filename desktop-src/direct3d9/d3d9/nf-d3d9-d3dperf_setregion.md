---
title: D3DPERF_SetRegion fonction)
description: Marquez une série de frames avec la couleur et le nom spécifiés dans le fichier PIXRun. Cette fonction n’est pas actuellement prise en charge par PIX.
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
- D3DPERF_SetRegion
targetos: Windows
ms.openlocfilehash: 650cc6063865da5ce30b97ed1468c1718ace5da6
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2020
ms.locfileid: "106511475"
---
# <a name="d3dperf_setregion-function"></a><span data-ttu-id="1fb3f-104">D3DPERF_SetRegion fonction)</span><span class="sxs-lookup"><span data-stu-id="1fb3f-104">D3DPERF_SetRegion function</span></span>

<span data-ttu-id="1fb3f-105">Marquez une série de frames avec la couleur et le nom spécifiés dans le fichier PIXRun.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-105">Mark a series of frames with the specified color and name in the PIXRun file.</span></span> <span data-ttu-id="1fb3f-106">Cette fonction n’est pas actuellement prise en charge par PIX.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-106">This function is not currently supported by PIX.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb3f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fb3f-107">Syntax</span></span>

```cpp
void WINAPI D3DPERF_SetRegion(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="1fb3f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fb3f-108">Parameters</span></span>

`col`

<span data-ttu-id="1fb3f-109">Couleur de l’événement.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-109">Event color.</span></span> <span data-ttu-id="1fb3f-110">Il s’agit de la couleur permettant d’afficher l’événement dans l’affichage des événements.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="1fb3f-111">Nom de l’événement.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="1fb3f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1fb3f-112">Return value</span></span>

<span data-ttu-id="1fb3f-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-113">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fb3f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1fb3f-114">Remarks</span></span>

<span data-ttu-id="1fb3f-115">Pour faciliter l’analyse, le programme cible peut utiliser la couleur pour marquer chaque niveau d’un programme cible.</span><span class="sxs-lookup"><span data-stu-id="1fb3f-115">To make analysis easier, the target program can use color to mark each level of a target program.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb3f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fb3f-116">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1fb3f-117">**Plateforme cible**</span><span class="sxs-lookup"><span data-stu-id="1fb3f-117">**Target Platform**</span></span> | <span data-ttu-id="1fb3f-118">Windows</span><span class="sxs-lookup"><span data-stu-id="1fb3f-118">Windows</span></span> |
| <span data-ttu-id="1fb3f-119">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="1fb3f-119">**Header**</span></span> | <span data-ttu-id="1fb3f-120">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="1fb3f-120">d3d9.h</span></span> |
| <span data-ttu-id="1fb3f-121">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="1fb3f-121">**Library**</span></span> | <span data-ttu-id="1fb3f-122">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="1fb3f-122">d3d9.lib</span></span> |
| <span data-ttu-id="1fb3f-123">**DLL**</span><span class="sxs-lookup"><span data-stu-id="1fb3f-123">**DLL**</span></span> | <span data-ttu-id="1fb3f-124">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="1fb3f-124">d3d9.dll</span></span> |