---
description: Fournit au système des informations sur un document après le démarrage d’une opération d’impression.
title: DlpNotifyPostStartPrint, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 7bc2505b44797edc836ed8ae89e5d9caf3f93f05
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495476"
---
# <a name="dlpnotifypoststartprint-function"></a><span data-ttu-id="391a7-103">DlpNotifyPostStartPrint fonction)</span><span class="sxs-lookup"><span data-stu-id="391a7-103">DlpNotifyPostStartPrint function</span></span>

<span data-ttu-id="391a7-104">Fournit au système des informations sur un document après le démarrage d’une opération d’impression.</span><span class="sxs-lookup"><span data-stu-id="391a7-104">Provides the system with information about a document after a print operation has started.</span></span>

## <a name="syntax"></a><span data-ttu-id="391a7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="391a7-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```

## <a name="parameters"></a><span data-ttu-id="391a7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="391a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="391a7-107">*DocumentInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="391a7-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="391a7-108">Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document associé à l’opération d’impression.</span><span class="sxs-lookup"><span data-stu-id="391a7-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="391a7-109">*PrintInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="391a7-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="391a7-110">Pointeur vers une structure [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) contenant des informations sur l’opération d’impression.</span><span class="sxs-lookup"><span data-stu-id="391a7-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about the print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="391a7-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="391a7-111">Return value</span></span>

<span data-ttu-id="391a7-112">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="391a7-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="391a7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="391a7-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="391a7-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="391a7-114">Requirements</span></span>



| <span data-ttu-id="391a7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="391a7-115">Requirement</span></span>          |    <span data-ttu-id="391a7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="391a7-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="391a7-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="391a7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="391a7-118">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="391a7-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="391a7-119">DLL</span><span class="sxs-lookup"><span data-stu-id="391a7-119">DLL</span></span><br/>                      | <span data-ttu-id="391a7-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="391a7-120">EndpointDlp.dll</span></span> |