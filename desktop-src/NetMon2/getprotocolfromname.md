---
description: La fonction GetProtocolFromName retourne un handle vers un protocole d’un nom donné.
ms.assetid: 18f5a9a7-4245-479d-a0da-2ede362a60b8
title: GetProtocolFromName, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e104c066be2a5465083c7983aaefebd46f548b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750076"
---
# <a name="getprotocolfromname-function"></a><span data-ttu-id="dfeea-103">GetProtocolFromName fonction)</span><span class="sxs-lookup"><span data-stu-id="dfeea-103">GetProtocolFromName function</span></span>

<span data-ttu-id="dfeea-104">La fonction **GetProtocolFromName** retourne un handle vers un protocole d’un nom donné.</span><span class="sxs-lookup"><span data-stu-id="dfeea-104">The **GetProtocolFromName** function returns a handle to a protocol of a given name.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfeea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfeea-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI GetProtocolFromName(
  _In_ LPSTR ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="dfeea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfeea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfeea-107">*ProtocolName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfeea-107">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfeea-108">Nom du protocole (par exemple, IP).</span><span class="sxs-lookup"><span data-stu-id="dfeea-108">Protocol name (for example, IP).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfeea-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dfeea-109">Return value</span></span>

<span data-ttu-id="dfeea-110">Si la fonction réussit, la valeur de retour est un handle de protocole.</span><span class="sxs-lookup"><span data-stu-id="dfeea-110">If the function is successful, the return value is a protocol handle.</span></span>

<span data-ttu-id="dfeea-111">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="dfeea-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfeea-112">Notes</span><span class="sxs-lookup"><span data-stu-id="dfeea-112">Remarks</span></span>

<span data-ttu-id="dfeea-113">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetProtocolFromName** .</span><span class="sxs-lookup"><span data-stu-id="dfeea-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolFromName** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfeea-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfeea-114">Requirements</span></span>



| <span data-ttu-id="dfeea-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfeea-115">Requirement</span></span> | <span data-ttu-id="dfeea-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfeea-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dfeea-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfeea-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dfeea-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dfeea-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="dfeea-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfeea-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dfeea-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dfeea-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dfeea-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="dfeea-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfeea-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfeea-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="dfeea-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dfeea-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="dfeea-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfeea-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="dfeea-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dfeea-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfeea-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfeea-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




