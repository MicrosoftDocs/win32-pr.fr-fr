---
description: La fonction GetProtocolStartOffsetHandle retourne le décalage de frame d’un protocole donné.
ms.assetid: b1e3a03b-f211-4c2c-8810-9e220c40136b
title: GetProtocolStartOffsetHandle, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffsetHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: bac8a10e2a0d8be667f1448c523f208c0c3e1512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513176"
---
# <a name="getprotocolstartoffsethandle-function"></a><span data-ttu-id="84467-103">GetProtocolStartOffsetHandle fonction)</span><span class="sxs-lookup"><span data-stu-id="84467-103">GetProtocolStartOffsetHandle function</span></span>

<span data-ttu-id="84467-104">La fonction **GetProtocolStartOffsetHandle** retourne le décalage de frame d’un protocole donné.</span><span class="sxs-lookup"><span data-stu-id="84467-104">The **GetProtocolStartOffsetHandle** function returns the frame offset of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="84467-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84467-105">Syntax</span></span>


```C++
DWORD WINAPI GetProtocolStartOffsetHandle(
  _In_ HFRAME    hFrame,
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="84467-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84467-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84467-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84467-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84467-108">Handle vers un frame.</span><span class="sxs-lookup"><span data-stu-id="84467-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="84467-109">*hProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84467-109">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84467-110">Handle d’un protocole.</span><span class="sxs-lookup"><span data-stu-id="84467-110">Handle to a protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84467-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84467-111">Return value</span></span>

<span data-ttu-id="84467-112">Si la fonction réussit, la valeur de retour est le décalage de la trame mesurée en octets.</span><span class="sxs-lookup"><span data-stu-id="84467-112">If the function is successful, the return value is the offset of the frame   measured in bytes.</span></span>

<span data-ttu-id="84467-113">Si la fonction échoue, la valeur de retour est un (1).</span><span class="sxs-lookup"><span data-stu-id="84467-113">If the function is unsuccessful, the return value is one (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="84467-114">Notes</span><span class="sxs-lookup"><span data-stu-id="84467-114">Remarks</span></span>

<span data-ttu-id="84467-115">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetProtocolStartOffsetHandle** .</span><span class="sxs-lookup"><span data-stu-id="84467-115">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolStartOffsetHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="84467-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84467-116">Requirements</span></span>



| <span data-ttu-id="84467-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84467-117">Requirement</span></span> | <span data-ttu-id="84467-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="84467-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="84467-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84467-119">Minimum supported client</span></span><br/> | <span data-ttu-id="84467-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84467-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="84467-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84467-121">Minimum supported server</span></span><br/> | <span data-ttu-id="84467-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84467-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="84467-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="84467-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="84467-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="84467-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="84467-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="84467-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="84467-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84467-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="84467-127">DLL</span><span class="sxs-lookup"><span data-stu-id="84467-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84467-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84467-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




