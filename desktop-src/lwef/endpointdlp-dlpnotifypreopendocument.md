---
description: Fournit au système des informations sur un document avant le lancement d’une opération d’ouverture.
title: DlpNotifyPreOpenDocument, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 557554ad55a3a520fa95fcf53c8044881eed8b21
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495468"
---
# <a name="dlpnotifypreopendocument-function"></a><span data-ttu-id="da993-103">DlpNotifyPreOpenDocument fonction)</span><span class="sxs-lookup"><span data-stu-id="da993-103">DlpNotifyPreOpenDocument function</span></span>

<span data-ttu-id="da993-104">Fournit au système des informations sur un document avant le lancement d’une opération d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="da993-104">Provides the system with information about a document before an open operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="da993-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da993-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="da993-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da993-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da993-107">*DocumentInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da993-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da993-108">Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="da993-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="da993-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="da993-109">Return value</span></span>

<span data-ttu-id="da993-110">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="da993-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="da993-111">Notes</span><span class="sxs-lookup"><span data-stu-id="da993-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="da993-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="da993-112">Requirements</span></span>



| <span data-ttu-id="da993-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da993-113">Requirement</span></span>          |    <span data-ttu-id="da993-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="da993-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da993-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da993-115">Minimum supported client</span></span><br/> | <span data-ttu-id="da993-116">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="da993-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="da993-117">DLL</span><span class="sxs-lookup"><span data-stu-id="da993-117">DLL</span></span><br/>                      | <span data-ttu-id="da993-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="da993-118">EndpointDlp.dll</span></span> |