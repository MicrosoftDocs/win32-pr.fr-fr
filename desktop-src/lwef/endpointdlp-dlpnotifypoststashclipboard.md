---
description: Fournit au système des informations d’État après la fin d’une opération de presse-papiers.
title: DlpNotifyPostStashClipboard, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: e549593acab6d74edf838a0f82952d8f3034bfcc
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495475"
---
# <a name="dlpnotifypoststashclipboard-function"></a><span data-ttu-id="af5f8-103">DlpNotifyPostStashClipboard fonction)</span><span class="sxs-lookup"><span data-stu-id="af5f8-103">DlpNotifyPostStashClipboard function</span></span>

<span data-ttu-id="af5f8-104">Fournit au système des informations d’État après la fin d’une opération de presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="af5f8-104">Provides the system with status information after a stash clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="af5f8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af5f8-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="af5f8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af5f8-106">Parameters</span></span>


<dl> <dt>

<span data-ttu-id="af5f8-107">*OpStatus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af5f8-107">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af5f8-108">Pointeur vers une structure [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenant des informations d’État sur l’opération de dissimulation du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="af5f8-108">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the stash clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="af5f8-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="af5f8-109">Return value</span></span>

<span data-ttu-id="af5f8-110">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="af5f8-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="af5f8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="af5f8-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="af5f8-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="af5f8-112">Requirements</span></span>



| <span data-ttu-id="af5f8-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af5f8-113">Requirement</span></span>          |    <span data-ttu-id="af5f8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="af5f8-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af5f8-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af5f8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="af5f8-116">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="af5f8-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="af5f8-117">DLL</span><span class="sxs-lookup"><span data-stu-id="af5f8-117">DLL</span></span><br/>                      | <span data-ttu-id="af5f8-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="af5f8-118">EndpointDlp.dll</span></span> |