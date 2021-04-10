---
description: La fonction GetFrameMacType retourne le type MAC du frame.
ms.assetid: 8d3da770-1392-4638-a267-32c2dae289b0
title: GetFrameMacType, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b85accc64a6e29424e3f65d070bafcf29bb3ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950965"
---
# <a name="getframemactype-function"></a><span data-ttu-id="f58bf-103">GetFrameMacType fonction)</span><span class="sxs-lookup"><span data-stu-id="f58bf-103">GetFrameMacType function</span></span>

<span data-ttu-id="f58bf-104">La fonction **GetFrameMacType** retourne le type Mac du frame.</span><span class="sxs-lookup"><span data-stu-id="f58bf-104">The **GetFrameMacType** function returns the MAC type of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f58bf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f58bf-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameMacType(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="f58bf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f58bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f58bf-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f58bf-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f58bf-108">Handle vers le frame.</span><span class="sxs-lookup"><span data-stu-id="f58bf-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f58bf-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f58bf-109">Return value</span></span>

<span data-ttu-id="f58bf-110">La fonction retourne le type MAC du frame, qui peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f58bf-110">The function returns the MAC type of the frame, which can have one of the following values.</span></span>

-   <span data-ttu-id="f58bf-111">\_type Mac \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="f58bf-111">MAC\_TYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="f58bf-112">MAC \_ type \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="f58bf-112">MAC\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="f58bf-113">\_type Mac \_ TOKENRING</span><span class="sxs-lookup"><span data-stu-id="f58bf-113">MAC\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="f58bf-114">\_type Mac \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="f58bf-114">MAC\_TYPE\_FDDI</span></span>

## <a name="remarks"></a><span data-ttu-id="f58bf-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f58bf-115">Remarks</span></span>

<span data-ttu-id="f58bf-116">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameMacType** .</span><span class="sxs-lookup"><span data-stu-id="f58bf-116">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameMacType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f58bf-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f58bf-117">Requirements</span></span>



| <span data-ttu-id="f58bf-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f58bf-118">Requirement</span></span> | <span data-ttu-id="f58bf-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f58bf-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f58bf-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f58bf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f58bf-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f58bf-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f58bf-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f58bf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f58bf-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f58bf-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f58bf-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f58bf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f58bf-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f58bf-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f58bf-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f58bf-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="f58bf-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f58bf-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f58bf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f58bf-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f58bf-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f58bf-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




