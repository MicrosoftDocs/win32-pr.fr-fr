---
description: Fournit au système des informations sur un document avant le lancement d’une opération d’impression.
title: DlpNotifyPrePrint, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: eef5e3a19a6b93a49ba8b600be77385a99d3153a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495435"
---
# <a name="dlpnotifypreprint-function"></a><span data-ttu-id="2d6fc-103">DlpNotifyPrePrint fonction)</span><span class="sxs-lookup"><span data-stu-id="2d6fc-103">DlpNotifyPrePrint function</span></span>

<span data-ttu-id="2d6fc-104">Fournit au système des informations sur un document avant le lancement d’une opération d’impression.</span><span class="sxs-lookup"><span data-stu-id="2d6fc-104">Provides the system with information about a document before a print operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d6fc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d6fc-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```



## <a name="parameters"></a><span data-ttu-id="2d6fc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d6fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d6fc-107">*DocumentInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d6fc-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d6fc-108">Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document à imprimer.</span><span class="sxs-lookup"><span data-stu-id="2d6fc-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be printed.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="2d6fc-109">*PrintInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d6fc-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d6fc-110">Pointeur vers une structure [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) contenant des informations sur l’opération d’impression.</span><span class="sxs-lookup"><span data-stu-id="2d6fc-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="2d6fc-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2d6fc-111">Return value</span></span>

<span data-ttu-id="2d6fc-112">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="2d6fc-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d6fc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2d6fc-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="2d6fc-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2d6fc-114">Requirements</span></span>



| <span data-ttu-id="2d6fc-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d6fc-115">Requirement</span></span>          |    <span data-ttu-id="2d6fc-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d6fc-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d6fc-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d6fc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2d6fc-118">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="2d6fc-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="2d6fc-119">DLL</span><span class="sxs-lookup"><span data-stu-id="2d6fc-119">DLL</span></span><br/>                      | <span data-ttu-id="2d6fc-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="2d6fc-120">EndpointDlp.dll</span></span> |