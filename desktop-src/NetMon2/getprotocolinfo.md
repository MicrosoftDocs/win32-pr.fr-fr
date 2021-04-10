---
description: La fonction GetProtocolInfo retourne un pointeur vers une valeur d’informations de protocole.
ms.assetid: 1ba47889-b2ed-47ba-94f9-1b781af6d01f
title: GetProtocolInfo, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2ec9fb58957c2e0fd64bc1c5878892fe6542af8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950956"
---
# <a name="getprotocolinfo-function"></a><span data-ttu-id="d7a4d-103">GetProtocolInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="d7a4d-103">GetProtocolInfo function</span></span>

<span data-ttu-id="d7a4d-104">La fonction **GetProtocolInfo** retourne un pointeur vers une valeur d’informations de protocole.</span><span class="sxs-lookup"><span data-stu-id="d7a4d-104">The **GetProtocolInfo** function returns a pointer to a protocol information value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7a4d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7a4d-105">Syntax</span></span>


```C++
LPPROTOCOLINFO WINAPI GetProtocolInfo(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="d7a4d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7a4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7a4d-107">*hProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d7a4d-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7a4d-108">Handle d’un protocole.</span><span class="sxs-lookup"><span data-stu-id="d7a4d-108">Handle to a protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7a4d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7a4d-109">Return value</span></span>

<span data-ttu-id="d7a4d-110">Si la fonction réussit, la valeur de retour est un pointeur vers la valeur des informations de protocole.</span><span class="sxs-lookup"><span data-stu-id="d7a4d-110">If the function is successful, the return value is a pointer to the protocol information value.</span></span>

<span data-ttu-id="d7a4d-111">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="d7a4d-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7a4d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d7a4d-112">Remarks</span></span>

<span data-ttu-id="d7a4d-113">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetProtocolInfo** .</span><span class="sxs-lookup"><span data-stu-id="d7a4d-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolInfo** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7a4d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7a4d-114">Requirements</span></span>



| <span data-ttu-id="d7a4d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7a4d-115">Requirement</span></span> | <span data-ttu-id="d7a4d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7a4d-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a4d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7a4d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a4d-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7a4d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d7a4d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7a4d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a4d-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7a4d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d7a4d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7a4d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7a4d-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7a4d-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d7a4d-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d7a4d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7a4d-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7a4d-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d7a4d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d7a4d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7a4d-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7a4d-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




