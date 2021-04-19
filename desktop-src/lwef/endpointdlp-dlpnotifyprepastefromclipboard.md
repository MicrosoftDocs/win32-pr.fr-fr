---
description: Fournit au système des informations sur un document avant le lancement d’une opération coller à partir du presse-papiers.
title: DlpNotifyPrePasteFromClipboard, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cfec6e7abbf2b94ce8bf78e0b1a10082ec54419d
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495431"
---
# <a name="dlpnotifyprepastefromclipboard-function"></a><span data-ttu-id="30263-103">DlpNotifyPrePasteFromClipboard fonction)</span><span class="sxs-lookup"><span data-stu-id="30263-103">DlpNotifyPrePasteFromClipboard function</span></span>

<span data-ttu-id="30263-104">Fournit au système des informations sur un document avant le lancement d’une opération coller à partir du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="30263-104">Provides the system with information about a document before a paste from clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="30263-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30263-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="30263-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30263-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30263-107">*DocumentInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30263-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30263-108">Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document dans lequel le contenu est collé.</span><span class="sxs-lookup"><span data-stu-id="30263-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document into which content is being pasted.</span></span>

</dd> </dl>




## <a name="return-value"></a><span data-ttu-id="30263-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="30263-109">Return value</span></span>

<span data-ttu-id="30263-110">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="30263-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="30263-111">Notes</span><span class="sxs-lookup"><span data-stu-id="30263-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="30263-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="30263-112">Requirements</span></span>



| <span data-ttu-id="30263-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30263-113">Requirement</span></span>          |    <span data-ttu-id="30263-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="30263-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30263-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30263-115">Minimum supported client</span></span><br/> | <span data-ttu-id="30263-116">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="30263-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="30263-117">DLL</span><span class="sxs-lookup"><span data-stu-id="30263-117">DLL</span></span><br/>                      | <span data-ttu-id="30263-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="30263-118">EndpointDlp.dll</span></span> |