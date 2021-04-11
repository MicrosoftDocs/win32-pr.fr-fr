---
title: MsimtfIsWindowFiltered fonction)
description: La fonction MsimtfIsWindowFiltered teste si la fenêtre donnée est filtrée par AIMM (gestionnaire de méthode d’entrée actif).
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- MsimtfIsWindowFiltered fonction Text Services Framework
topic_type:
- apiref
api_name:
- MsimtfIsWindowFiltered
api_location:
- msimtf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ad9bd9fb61c546ec3e2f1d96d5fc9cf932613a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105397"
---
# <a name="msimtfiswindowfiltered-function"></a><span data-ttu-id="7ec35-104">MsimtfIsWindowFiltered fonction)</span><span class="sxs-lookup"><span data-stu-id="7ec35-104">MsimtfIsWindowFiltered function</span></span>

<span data-ttu-id="7ec35-105">La fonction **MsimtfIsWindowFiltered** teste si la fenêtre donnée est filtrée par AIMM (gestionnaire de méthode d’entrée actif).</span><span class="sxs-lookup"><span data-stu-id="7ec35-105">The **MsimtfIsWindowFiltered** function tests if the given window is filtered by AIMM (Active Input Method Manager).</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec35-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ec35-106">Syntax</span></span>


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="7ec35-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ec35-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ec35-108">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ec35-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec35-109">Handle de fenêtre à tester.</span><span class="sxs-lookup"><span data-stu-id="7ec35-109">A window handle to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ec35-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ec35-110">Return value</span></span>



| <span data-ttu-id="7ec35-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7ec35-111">Return code</span></span>                                                                          | <span data-ttu-id="7ec35-112">Description</span><span class="sxs-lookup"><span data-stu-id="7ec35-112">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7ec35-113"><dt>**:**</dt></span><span class="sxs-lookup"><span data-stu-id="7ec35-113"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="7ec35-114">Si cette fenêtre est filtrée par le gestionnaire de méthode d’entrée actif.</span><span class="sxs-lookup"><span data-stu-id="7ec35-114">If this window is filtered by Active Input Method Manager.</span></span><br/>     |
| <dl> <span data-ttu-id="7ec35-115"><dt>**FAUSSES**</dt></span><span class="sxs-lookup"><span data-stu-id="7ec35-115"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="7ec35-116">Si cette fenêtre n’est pas filtrée par le gestionnaire de méthode d’entrée actif.</span><span class="sxs-lookup"><span data-stu-id="7ec35-116">If this window is not filtered by Active Input Method Manager.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ec35-117">Notes</span><span class="sxs-lookup"><span data-stu-id="7ec35-117">Remarks</span></span>

<span data-ttu-id="7ec35-118">Une fenêtre peut être filtrée par IActiveIMMApp :: FilterClientWindows.</span><span class="sxs-lookup"><span data-stu-id="7ec35-118">A window can be filtered by IActiveIMMApp::FilterClientWindows.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec35-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ec35-119">Requirements</span></span>



| <span data-ttu-id="7ec35-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ec35-120">Requirement</span></span> | <span data-ttu-id="7ec35-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ec35-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec35-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ec35-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7ec35-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ec35-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ec35-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ec35-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7ec35-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ec35-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ec35-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7ec35-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ec35-127"><dt>Msimtf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ec35-127"><dt>Msimtf.dll</dt></span></span> </dl> |



 

 





