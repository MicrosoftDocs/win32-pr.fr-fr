---
description: Fournit au système des informations sur un document avant le lancement d’une opération copier dans le presse-papiers.
title: DlpNotifyPreCopyToClipboard, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b8e835e58d19570b9459d91ad131bbc0f38f378a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495472"
---
# <a name="dlpnotifyprecopytoclipboard-function"></a><span data-ttu-id="bdf63-103">DlpNotifyPreCopyToClipboard fonction)</span><span class="sxs-lookup"><span data-stu-id="bdf63-103">DlpNotifyPreCopyToClipboard function</span></span>

<span data-ttu-id="bdf63-104">Fournit au système des informations sur un document avant le lancement d’une opération copier dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="bdf63-104">Provides the system with information about a document before a copy to clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdf63-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdf63-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="bdf63-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdf63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdf63-107">*DocumentInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdf63-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf63-108">Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document à partir duquel le contenu est copié.</span><span class="sxs-lookup"><span data-stu-id="bdf63-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document from which content is being copied.</span></span>

</dd> </dl>




## <a name="return-value"></a><span data-ttu-id="bdf63-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bdf63-109">Return value</span></span>

<span data-ttu-id="bdf63-110">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="bdf63-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdf63-111">Notes</span><span class="sxs-lookup"><span data-stu-id="bdf63-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="bdf63-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bdf63-112">Requirements</span></span>



| <span data-ttu-id="bdf63-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdf63-113">Requirement</span></span>          |    <span data-ttu-id="bdf63-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdf63-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf63-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdf63-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bdf63-116">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="bdf63-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="bdf63-117">DLL</span><span class="sxs-lookup"><span data-stu-id="bdf63-117">DLL</span></span><br/>                      | <span data-ttu-id="bdf63-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="bdf63-118">EndpointDlp.dll</span></span> |