---
description: Fournit au système des informations sur un document après la fin de l’opération Enregistrer sous.
title: DlpNotifyPostSaveAsDocument, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 564e7173cbfe72a020f1c7e12a60ceda25fd845c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495479"
---
# <a name="dlpnotifypostsaveasdocument-function"></a><span data-ttu-id="3064b-103">DlpNotifyPostSaveAsDocument fonction)</span><span class="sxs-lookup"><span data-stu-id="3064b-103">DlpNotifyPostSaveAsDocument function</span></span>

<span data-ttu-id="3064b-104">Fournit au système des informations sur un document après la fin de l’opération Enregistrer sous.</span><span class="sxs-lookup"><span data-stu-id="3064b-104">Provides the system with information about a document after the save as operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3064b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3064b-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a><span data-ttu-id="3064b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3064b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3064b-107">*DocumentInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3064b-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3064b-108">Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document qui a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="3064b-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="3064b-109">*Destination* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3064b-109">*Destination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3064b-110">**LPCWSTR** contenant le chemin d’accès de destination du document qui a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="3064b-110">A **LPCWSTR** containing the destination path the document that was saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="3064b-111">*OpStatus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3064b-111">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3064b-112">Pointeur vers une structure [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenant des informations d’État sur l’opération Enregistrer sous.</span><span class="sxs-lookup"><span data-stu-id="3064b-112">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the save as operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="3064b-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3064b-113">Return value</span></span>

<span data-ttu-id="3064b-114">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="3064b-114">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="3064b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3064b-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="3064b-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3064b-116">Requirements</span></span>



| <span data-ttu-id="3064b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3064b-117">Requirement</span></span>          |    <span data-ttu-id="3064b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3064b-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3064b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3064b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3064b-120">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="3064b-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="3064b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3064b-121">DLL</span></span><br/>                      | <span data-ttu-id="3064b-122">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="3064b-122">EndpointDlp.dll</span></span> |