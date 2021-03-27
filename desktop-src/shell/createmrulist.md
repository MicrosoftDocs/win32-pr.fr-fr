---
description: Crée une nouvelle liste des derniers fichiers utilisés (MRU).
title: CreateMRUListW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMRUListW
- CreateMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: b2d9e3c7-8151-45ef-9658-bd33a87b4c9c
ms.openlocfilehash: 572e52f1461e3d48ab9eba1aa903c7fb690636d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750245"
---
# <a name="createmrulistw-function"></a><span data-ttu-id="3d407-103">CreateMRUListW fonction)</span><span class="sxs-lookup"><span data-stu-id="3d407-103">CreateMRUListW function</span></span>

<span data-ttu-id="3d407-104">Crée une nouvelle liste des derniers fichiers utilisés (MRU).</span><span class="sxs-lookup"><span data-stu-id="3d407-104">Creates a new most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d407-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d407-105">Syntax</span></span>


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a><span data-ttu-id="3d407-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d407-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d407-107">*lpmi* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3d407-107">*lpmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d407-108">Type : **LPMRUINFO**</span><span class="sxs-lookup"><span data-stu-id="3d407-108">Type: **LPMRUINFO**</span></span>

<span data-ttu-id="3d407-109">Pointeur vers une structure [**MRUINFO**](mruinfo.md) définissant la liste MRU.</span><span class="sxs-lookup"><span data-stu-id="3d407-109">A pointer to an [**MRUINFO**](mruinfo.md) structure defining the MRU list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d407-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3d407-110">Return value</span></span>

<span data-ttu-id="3d407-111">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="3d407-111">Type: **int**</span></span>

<span data-ttu-id="3d407-112">Retourne un handle vers la nouvelle liste MRU, ou 0 en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3d407-112">Returns a handle to the new MRU list, or 0 in case of an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d407-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3d407-113">Remarks</span></span>

<span data-ttu-id="3d407-114">Cette fonction n’est pas incluse dans un en-tête public ou une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3d407-114">This function is not included in a public header or library.</span></span> <span data-ttu-id="3d407-115">Il est accessible par le biais de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extrait de comctl32.dll par son ordinal, qui est 400 pour **CreateMRUListW**.</span><span class="sxs-lookup"><span data-stu-id="3d407-115">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 400 for **CreateMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d407-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3d407-116">Requirements</span></span>



| <span data-ttu-id="3d407-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d407-117">Requirement</span></span> | <span data-ttu-id="3d407-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d407-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d407-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d407-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3d407-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d407-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3d407-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d407-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3d407-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d407-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3d407-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3d407-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d407-124"><dt>Comctl32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="3d407-124"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="3d407-125">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="3d407-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3d407-126">**CreateMRUListW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="3d407-126">**CreateMRUListW** (Unicode)</span></span><br/>                                                                        |



 

 
