---
title: D3DPERF_BeginEvent fonction)
description: Marque le début d’un événement défini par l’utilisateur. PIX peut utiliser cet événement pour déclencher une action.
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
- D3DPERF_BeginEvent
targetos: Windows
ms.openlocfilehash: f6732d4ce969cbd26cdb32f4750654c7baacd324
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104381639"
---
# <a name="d3dperf_beginevent-function"></a><span data-ttu-id="da64b-104">D3DPERF_BeginEvent fonction)</span><span class="sxs-lookup"><span data-stu-id="da64b-104">D3DPERF_BeginEvent function</span></span>

<span data-ttu-id="da64b-105">Marque le début d’un événement défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="da64b-105">Marks the beginning of a user-defined event.</span></span> <span data-ttu-id="da64b-106">PIX peut utiliser cet événement pour déclencher une action.</span><span class="sxs-lookup"><span data-stu-id="da64b-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="da64b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da64b-107">Syntax</span></span>

```cpp
int WINAPI D3DPERF_BeginEvent(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="da64b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da64b-108">Parameters</span></span>

`col`

<span data-ttu-id="da64b-109">Couleur de l’événement.</span><span class="sxs-lookup"><span data-stu-id="da64b-109">Event color.</span></span> <span data-ttu-id="da64b-110">Il s’agit de la couleur permettant d’afficher l’événement dans l’affichage des événements.</span><span class="sxs-lookup"><span data-stu-id="da64b-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="da64b-111">Nom de l’événement.</span><span class="sxs-lookup"><span data-stu-id="da64b-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="da64b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da64b-112">Return value</span></span>

<span data-ttu-id="da64b-113">Niveau de base zéro de la hiérarchie à partir duquel cet événement commence.</span><span class="sxs-lookup"><span data-stu-id="da64b-113">The zero-based level of the hierarchy that this event is starting in.</span></span> <span data-ttu-id="da64b-114">Si une erreur se produit, la valeur de retour est négative.</span><span class="sxs-lookup"><span data-stu-id="da64b-114">If an error occurs, the return value will be negative.</span></span>

## <a name="remarks"></a><span data-ttu-id="da64b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="da64b-115">Remarks</span></span>

<span data-ttu-id="da64b-116">Les événements définis par l’utilisateur regroupent d’autres événements d’une manière significative pour le programme cible afin qu’ils puissent être mieux représentés dans les outils de profilage des performances.</span><span class="sxs-lookup"><span data-stu-id="da64b-116">User-defined events group together other events in a way that is meaningful to the target program so that they can be better represented in performance profiling tools.</span></span> <span data-ttu-id="da64b-117">Par exemple, un événement d' *espace de dessin* peut comporter un certain nombre d’appels Direct3D qui gèrent le dessin d’un espace dans un jeu.</span><span class="sxs-lookup"><span data-stu-id="da64b-117">For example, a *Draw Spaceship* event might bracket a number of Direct3D calls that handle drawing a spaceship in a game.</span></span> <span data-ttu-id="da64b-118">Les événements peuvent être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="da64b-118">Events can be nested.</span></span>

<span data-ttu-id="da64b-119">Chaque appel de **D3DPERF_BeginEvent** doit avoir un appel de **D3DPERF_EndEvent** correspondant.</span><span class="sxs-lookup"><span data-stu-id="da64b-119">Each **D3DPERF_BeginEvent** call should have a matching **D3DPERF_EndEvent** call.</span></span> <span data-ttu-id="da64b-120">Les événements instantanés (qui ne comportent pas d’autres événements) doivent être étiquetés à l’aide de **D3DPERF_SetMarker** plutôt que par **D3DPERF_BeginEvent** et **D3DPERF_EndEvent**.</span><span class="sxs-lookup"><span data-stu-id="da64b-120">Instantaneous events (which do not bracket other events) should be labeled by using **D3DPERF_SetMarker** rather than by **D3DPERF_BeginEvent** and **D3DPERF_EndEvent**.</span></span>

## <a name="requirements"></a><span data-ttu-id="da64b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da64b-121">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="da64b-122">**Plateforme cible**</span><span class="sxs-lookup"><span data-stu-id="da64b-122">**Target Platform**</span></span> | <span data-ttu-id="da64b-123">Windows</span><span class="sxs-lookup"><span data-stu-id="da64b-123">Windows</span></span> |
| <span data-ttu-id="da64b-124">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="da64b-124">**Header**</span></span> | <span data-ttu-id="da64b-125">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="da64b-125">d3d9.h</span></span> |
| <span data-ttu-id="da64b-126">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="da64b-126">**Library**</span></span> | <span data-ttu-id="da64b-127">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="da64b-127">d3d9.lib</span></span> |
| <span data-ttu-id="da64b-128">**DLL**</span><span class="sxs-lookup"><span data-stu-id="da64b-128">**DLL**</span></span> | <span data-ttu-id="da64b-129">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="da64b-129">d3d9.dll</span></span> |