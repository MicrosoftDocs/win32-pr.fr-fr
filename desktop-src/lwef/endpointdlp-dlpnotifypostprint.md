---
description: Fournit au système des informations sur un document une fois l’opération d’impression terminée.
title: DlpNotifyPostPrint, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b1206aa4e358e0763c10a0d9b5028acae25f5683
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495480"
---
# <a name="dlpnotifypostprint-function"></a><span data-ttu-id="cb89a-103">DlpNotifyPostPrint fonction)</span><span class="sxs-lookup"><span data-stu-id="cb89a-103">DlpNotifyPostPrint function</span></span>

<span data-ttu-id="cb89a-104">Fournit au système des informations sur un document une fois l’opération d’impression terminée.</span><span class="sxs-lookup"><span data-stu-id="cb89a-104">Provides the system with information about a document after a print operation has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb89a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb89a-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```

## <a name="parameters"></a><span data-ttu-id="cb89a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb89a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb89a-107">*DocumentInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cb89a-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb89a-108">Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document associé à l’opération d’impression.</span><span class="sxs-lookup"><span data-stu-id="cb89a-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="cb89a-109">*PrintInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cb89a-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb89a-110">Pointeur vers une structure [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) contenant des informations sur l’opération d’impression.</span><span class="sxs-lookup"><span data-stu-id="cb89a-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="cb89a-111">*OpStatus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cb89a-111">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb89a-112">Pointeur vers une structure [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenant des informations d’État sur l’opération d’impression.</span><span class="sxs-lookup"><span data-stu-id="cb89a-112">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="cb89a-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cb89a-113">Return value</span></span>

<span data-ttu-id="cb89a-114">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="cb89a-114">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb89a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="cb89a-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="cb89a-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cb89a-116">Requirements</span></span>



| <span data-ttu-id="cb89a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb89a-117">Requirement</span></span>          |    <span data-ttu-id="cb89a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb89a-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb89a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb89a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb89a-120">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="cb89a-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="cb89a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="cb89a-121">DLL</span></span><br/>                      | <span data-ttu-id="cb89a-122">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="cb89a-122">EndpointDlp.dll</span></span> |