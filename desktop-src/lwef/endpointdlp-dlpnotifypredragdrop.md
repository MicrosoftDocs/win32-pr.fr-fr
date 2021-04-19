---
description: Fournit au système des informations sur un document avant le lancement d’une opération glisser-déplacer.
title: DlpNotifyPreDragDrop, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreDragDrop
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d88a28c0dff4b13cf1c1848eeb8623c3acd1c024
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495471"
---
# <a name="dlpnotifypredragdrop-function"></a><span data-ttu-id="6d644-103">DlpNotifyPreDragDrop fonction)</span><span class="sxs-lookup"><span data-stu-id="6d644-103">DlpNotifyPreDragDrop function</span></span>

<span data-ttu-id="6d644-104">Fournit au système des informations sur un document avant le lancement d’une opération glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="6d644-104">Provides the system with information about a document before a drag drop operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d644-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d644-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="6d644-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d644-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d644-107">*DocumentInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d644-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d644-108">Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document associé à l’opération glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="6d644-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drag drop operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="6d644-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6d644-109">Return value</span></span>

<span data-ttu-id="6d644-110">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="6d644-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d644-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6d644-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="6d644-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6d644-112">Requirements</span></span>



| <span data-ttu-id="6d644-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d644-113">Requirement</span></span>          |    <span data-ttu-id="6d644-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d644-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d644-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d644-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6d644-116">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="6d644-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="6d644-117">DLL</span><span class="sxs-lookup"><span data-stu-id="6d644-117">DLL</span></span><br/>                      | <span data-ttu-id="6d644-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="6d644-118">EndpointDlp.dll</span></span> |