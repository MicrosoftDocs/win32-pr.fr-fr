---
description: Fournit au système des informations sur un fichier de document une fois l’opération d’ouverture terminée.
title: DlpNotifyPostOpenDocumentFile, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 0aed30cc0eca066b569ad1299392430c4d1adeff
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495495"
---
# <a name="dlpnotifypostopendocumentfile-function"></a><span data-ttu-id="25be8-103">DlpNotifyPostOpenDocumentFile fonction)</span><span class="sxs-lookup"><span data-stu-id="25be8-103">DlpNotifyPostOpenDocumentFile function</span></span>

<span data-ttu-id="25be8-104">Fournit au système des informations sur un fichier de document après la fin d’une opération d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="25be8-104">Provides the system with information about a document file after an open operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="25be8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25be8-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus 
```

## <a name="parameters"></a><span data-ttu-id="25be8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25be8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25be8-107">*DocumentInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25be8-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25be8-108">Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document qui a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="25be8-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was opened.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="25be8-109">*OpStatus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25be8-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25be8-110">Pointeur vers une structure [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenant des informations d’État sur l’opération d’ouverture de document.</span><span class="sxs-lookup"><span data-stu-id="25be8-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the open document operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="25be8-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="25be8-111">Return value</span></span>

<span data-ttu-id="25be8-112">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="25be8-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="25be8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="25be8-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="25be8-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="25be8-114">Requirements</span></span>



| <span data-ttu-id="25be8-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25be8-115">Requirement</span></span>          |    <span data-ttu-id="25be8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="25be8-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25be8-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25be8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="25be8-118">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="25be8-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="25be8-119">DLL</span><span class="sxs-lookup"><span data-stu-id="25be8-119">DLL</span></span><br/>                      | <span data-ttu-id="25be8-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="25be8-120">EndpointDlp.dll</span></span> |