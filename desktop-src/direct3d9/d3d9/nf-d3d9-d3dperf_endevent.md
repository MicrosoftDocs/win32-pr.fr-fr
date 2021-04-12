---
title: D3DPERF_EndEvent fonction)
description: Marque la fin d’un événement défini par l’utilisateur. PIX peut utiliser cet événement pour déclencher une action.
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
- D3DPERF_EndEvent
targetos: Windows
ms.openlocfilehash: 91c2a6a19b926cd9f5549fae084ce8973432b0f2
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104381641"
---
# <a name="d3dperf_endevent-function"></a><span data-ttu-id="287d1-104">D3DPERF_EndEvent fonction)</span><span class="sxs-lookup"><span data-stu-id="287d1-104">D3DPERF_EndEvent function</span></span>

<span data-ttu-id="287d1-105">Marque la fin d’un événement défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="287d1-105">Marks the end of a user-defined event.</span></span> <span data-ttu-id="287d1-106">PIX peut utiliser cet événement pour déclencher une action.</span><span class="sxs-lookup"><span data-stu-id="287d1-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="287d1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="287d1-107">Syntax</span></span>

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a><span data-ttu-id="287d1-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="287d1-108">Return value</span></span>

<span data-ttu-id="287d1-109">Niveau de la hiérarchie dans laquelle l’événement se termine.</span><span class="sxs-lookup"><span data-stu-id="287d1-109">The level of the hierarchy in which the event is ending.</span></span> <span data-ttu-id="287d1-110">Si une erreur se produit, cette valeur est négative.</span><span class="sxs-lookup"><span data-stu-id="287d1-110">If an error occurs, this value is negative.</span></span>

## <a name="requirements"></a><span data-ttu-id="287d1-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="287d1-111">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="287d1-112">**Plateforme cible**</span><span class="sxs-lookup"><span data-stu-id="287d1-112">**Target Platform**</span></span> | <span data-ttu-id="287d1-113">Windows</span><span class="sxs-lookup"><span data-stu-id="287d1-113">Windows</span></span> |
| <span data-ttu-id="287d1-114">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="287d1-114">**Header**</span></span> | <span data-ttu-id="287d1-115">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="287d1-115">d3d9.h</span></span> |
| <span data-ttu-id="287d1-116">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="287d1-116">**Library**</span></span> | <span data-ttu-id="287d1-117">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="287d1-117">d3d9.lib</span></span> |
| <span data-ttu-id="287d1-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="287d1-118">**DLL**</span></span> | <span data-ttu-id="287d1-119">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="287d1-119">d3d9.dll</span></span> |