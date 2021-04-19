---
description: Fournit au système des informations sur un document avant le lancement d’une opération Enregistrer sous.
title: DlpNotifyPreSaveAsDocument, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5226ed63227e2d9dd01155066e2e6e19f77e063f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495436"
---
# <a name="dlpnotifypresaveasdocument-function"></a><span data-ttu-id="28513-103">DlpNotifyPreSaveAsDocument fonction)</span><span class="sxs-lookup"><span data-stu-id="28513-103">DlpNotifyPreSaveAsDocument function</span></span>

<span data-ttu-id="28513-104">Fournit au système des informations sur un document avant le lancement d’une opération Enregistrer sous.</span><span class="sxs-lookup"><span data-stu-id="28513-104">Provides the system with information about a document before a save as operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="28513-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28513-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
```



## <a name="parameters"></a><span data-ttu-id="28513-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28513-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28513-107">*DocumentInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28513-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28513-108">Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="28513-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="28513-109">*Destination* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28513-109">*Destination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28513-110">**LPCWSTR** contenant le chemin d’accès de destination du document à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="28513-110">A **LPCWSTR** containing the destination path of the document to be saved.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="28513-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="28513-111">Return value</span></span>

<span data-ttu-id="28513-112">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="28513-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="28513-113">Notes</span><span class="sxs-lookup"><span data-stu-id="28513-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="28513-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="28513-114">Requirements</span></span>



| <span data-ttu-id="28513-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28513-115">Requirement</span></span>          |    <span data-ttu-id="28513-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="28513-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28513-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28513-117">Minimum supported client</span></span><br/> | <span data-ttu-id="28513-118">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="28513-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="28513-119">DLL</span><span class="sxs-lookup"><span data-stu-id="28513-119">DLL</span></span><br/>                      | <span data-ttu-id="28513-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="28513-120">EndpointDlp.dll</span></span> |