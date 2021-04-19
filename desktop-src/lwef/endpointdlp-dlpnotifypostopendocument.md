---
description: Fournit au système des informations sur un document une fois l’opération d’ouverture terminée.
title: DlpNotifyPostOpenDocument, fonction (endpointdlp. h)
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
ms.openlocfilehash: 10121e69ddbdc41516e56ec07e87a2f6dd8148cd
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495504"
---
# <a name="dlpnotifypostopendocument-function"></a><span data-ttu-id="b7035-103">DlpNotifyPostOpenDocument fonction)</span><span class="sxs-lookup"><span data-stu-id="b7035-103">DlpNotifyPostOpenDocument function</span></span>

<span data-ttu-id="b7035-104">Fournit au système des informations sur un document après l’achèvement d’une opération d’ouverture de document.</span><span class="sxs-lookup"><span data-stu-id="b7035-104">Provides the system with information about a document after an open document operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7035-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7035-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a><span data-ttu-id="b7035-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7035-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7035-107">*DocumentInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7035-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7035-108">Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document qui a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="b7035-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was opened.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="b7035-109">*OpStatus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7035-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7035-110">Pointeur vers une structure [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenant des informations d’État sur l’opération d’ouverture de document.</span><span class="sxs-lookup"><span data-stu-id="b7035-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the open document operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="b7035-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b7035-111">Return value</span></span>

<span data-ttu-id="b7035-112">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="b7035-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7035-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b7035-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="b7035-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b7035-114">Requirements</span></span>



| <span data-ttu-id="b7035-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7035-115">Requirement</span></span>          |    <span data-ttu-id="b7035-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7035-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7035-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7035-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b7035-118">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="b7035-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="b7035-119">DLL</span><span class="sxs-lookup"><span data-stu-id="b7035-119">DLL</span></span><br/>                      | <span data-ttu-id="b7035-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="b7035-120">EndpointDlp.dll</span></span> |