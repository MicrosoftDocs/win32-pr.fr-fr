---
title: D3DPERF_SetMarker fonction)
description: Marquez un événement instantané. PIX peut utiliser cet événement pour déclencher une action.
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
- D3DPERF_SetMarker
targetos: Windows
ms.openlocfilehash: 8eef59b9914ce30b95751641c16becf1963b19e0
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104381640"
---
# <a name="d3dperf_setmarker-function"></a><span data-ttu-id="7cf6e-104">D3DPERF_SetMarker fonction)</span><span class="sxs-lookup"><span data-stu-id="7cf6e-104">D3DPERF_SetMarker function</span></span>

<span data-ttu-id="7cf6e-105">Marquez un événement instantané.</span><span class="sxs-lookup"><span data-stu-id="7cf6e-105">Mark an instantaneous event.</span></span> <span data-ttu-id="7cf6e-106">PIX peut utiliser cet événement pour déclencher une action.</span><span class="sxs-lookup"><span data-stu-id="7cf6e-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf6e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cf6e-107">Syntax</span></span>

```cpp
void WINAPI D3DPERF_SetMarker(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="7cf6e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cf6e-108">Parameters</span></span>

`col`

<span data-ttu-id="7cf6e-109">Couleur de l’événement.</span><span class="sxs-lookup"><span data-stu-id="7cf6e-109">Event color.</span></span> <span data-ttu-id="7cf6e-110">Il s’agit de la couleur permettant d’afficher l’événement dans l’affichage des événements.</span><span class="sxs-lookup"><span data-stu-id="7cf6e-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="7cf6e-111">Nom de l’événement.</span><span class="sxs-lookup"><span data-stu-id="7cf6e-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="7cf6e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7cf6e-112">Return value</span></span>

<span data-ttu-id="7cf6e-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7cf6e-113">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cf6e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7cf6e-114">Remarks</span></span>

<span data-ttu-id="7cf6e-115">Les événements utilisateur instantanés ne dépassent pas ou ne regroupent pas d’autres événements.</span><span class="sxs-lookup"><span data-stu-id="7cf6e-115">Instantaneous user events do not bracket or group other events.</span></span> <span data-ttu-id="7cf6e-116">Par exemple, lorsque l’utilisateur lance une arme dans un jeu, un événement déclenché par une *capture* peut être créé par un appel de **D3DPERF_SetMarker** .</span><span class="sxs-lookup"><span data-stu-id="7cf6e-116">For example, when the user fires a weapon in a game, a *Shot Fired* event could be created by a **D3DPERF_SetMarker** call.</span></span> <span data-ttu-id="7cf6e-117">Pour regrouper plusieurs événements sous un seul nom défini par l’utilisateur, utilisez **D3DPERF_BeginEvent** et **D3DPERF_EndEvent** plutôt que **D3DPERF_SetMarker**.</span><span class="sxs-lookup"><span data-stu-id="7cf6e-117">To group together multiple events under a single, user-defined name, use **D3DPERF_BeginEvent** and **D3DPERF_EndEvent** rather than **D3DPERF_SetMarker**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cf6e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cf6e-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="7cf6e-119">**Plateforme cible**</span><span class="sxs-lookup"><span data-stu-id="7cf6e-119">**Target Platform**</span></span> | <span data-ttu-id="7cf6e-120">Windows</span><span class="sxs-lookup"><span data-stu-id="7cf6e-120">Windows</span></span> |
| <span data-ttu-id="7cf6e-121">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="7cf6e-121">**Header**</span></span> | <span data-ttu-id="7cf6e-122">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="7cf6e-122">d3d9.h</span></span> |
| <span data-ttu-id="7cf6e-123">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="7cf6e-123">**Library**</span></span> | <span data-ttu-id="7cf6e-124">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="7cf6e-124">d3d9.lib</span></span> |
| <span data-ttu-id="7cf6e-125">**DLL**</span><span class="sxs-lookup"><span data-stu-id="7cf6e-125">**DLL**</span></span> | <span data-ttu-id="7cf6e-126">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="7cf6e-126">d3d9.dll</span></span> |