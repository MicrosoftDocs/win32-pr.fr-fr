---
description: Cette fonction termine de force le programme appelant s’il est appelé à l’intérieur d’un appel de chargeur. Dans le cas contraire, elle n’a aucun effet.
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: LdrFastFailInLoaderCallout fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrFastFailInLoaderCallout
api_type:
- DllExport
api_location:
- NTDll.dll
ms.openlocfilehash: f74b9cdc0aec666242a8267fab8d6255c75dc94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528619"
---
# <a name="ldrfastfailinloadercallout-function"></a><span data-ttu-id="78e99-104">LdrFastFailInLoaderCallout fonction)</span><span class="sxs-lookup"><span data-stu-id="78e99-104">LdrFastFailInLoaderCallout function</span></span>

<span data-ttu-id="78e99-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="78e99-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="78e99-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="78e99-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="78e99-107">Cette fonction termine de force le programme appelant s’il est appelé à l’intérieur d’un appel de chargeur.</span><span class="sxs-lookup"><span data-stu-id="78e99-107">This function forcefully terminates the calling program if it is invoked inside a loader callout.</span></span> <span data-ttu-id="78e99-108">Dans le cas contraire, elle n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="78e99-108">Otherwise, it has no effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="78e99-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78e99-109">Syntax</span></span>


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a><span data-ttu-id="78e99-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78e99-110">Parameters</span></span>

<span data-ttu-id="78e99-111">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="78e99-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="78e99-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78e99-112">Return value</span></span>

<span data-ttu-id="78e99-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="78e99-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78e99-114">Notes</span><span class="sxs-lookup"><span data-stu-id="78e99-114">Remarks</span></span>

<span data-ttu-id="78e99-115">Cette routine n’intercepte pas tous les cas de blocage potentiels ; Il est possible pour un thread à l’intérieur d’une légende de chargeur d’acquérir un verrou tandis qu’un thread en dehors d’un appel de chargeur détient le même verrou et effectue un appel dans le chargeur.</span><span class="sxs-lookup"><span data-stu-id="78e99-115">This routine does not catch all potential deadlock cases; it is possible for a thread inside a loader callout to acquire a lock while some thread outside a loader callout holds the same lock and makes a call into the loader.</span></span> <span data-ttu-id="78e99-116">En d’autres termes, il peut y avoir une inversion d’ordre de verrou entre le verrou du chargeur et un verrou client.</span><span class="sxs-lookup"><span data-stu-id="78e99-116">In other words, there can be a lock order inversion between the loader lock and a client lock.</span></span>

## <a name="requirements"></a><span data-ttu-id="78e99-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78e99-117">Requirements</span></span>



| <span data-ttu-id="78e99-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78e99-118">Requirement</span></span> | <span data-ttu-id="78e99-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="78e99-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="78e99-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="78e99-120">Library</span></span><br/> | <dl> <span data-ttu-id="78e99-121"><dt>NTDll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78e99-121"><dt>NTDll.lib</dt></span></span> </dl> |
| <span data-ttu-id="78e99-122">DLL</span><span class="sxs-lookup"><span data-stu-id="78e99-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="78e99-123"><dt>NTDll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78e99-123"><dt>NTDll.dll</dt></span></span> </dl> |



 

 




