---
description: Fournit au système des informations sur un document après la fin de l’opération coller à partir du presse-papiers.
title: DlpNotifyPostPasteFromClipboard, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 69a5afbc41350092ebd4d433d2f4d7259ece82cf
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495483"
---
# <a name="dlpnotifypostpastefromclipboard-function"></a><span data-ttu-id="403b3-103">DlpNotifyPostPasteFromClipboard fonction)</span><span class="sxs-lookup"><span data-stu-id="403b3-103">DlpNotifyPostPasteFromClipboard function</span></span>

<span data-ttu-id="403b3-104">Fournit au système des informations sur un document après la fin de l’opération coller à partir du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="403b3-104">Provides the system with information about a document after a paste from clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="403b3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="403b3-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="403b3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="403b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="403b3-107">*DocumentInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="403b3-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="403b3-108">Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document dans lequel le contenu a été copié.</span><span class="sxs-lookup"><span data-stu-id="403b3-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document into which content was copied.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="403b3-109">*OpStatus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="403b3-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="403b3-110">Pointeur vers une structure [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenant des informations d’État sur l’opération de collage à partir du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="403b3-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the paste from clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="403b3-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="403b3-111">Return value</span></span>

<span data-ttu-id="403b3-112">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="403b3-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="403b3-113">Notes</span><span class="sxs-lookup"><span data-stu-id="403b3-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="403b3-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="403b3-114">Requirements</span></span>



| <span data-ttu-id="403b3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="403b3-115">Requirement</span></span>          |    <span data-ttu-id="403b3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="403b3-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="403b3-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="403b3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="403b3-118">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="403b3-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="403b3-119">DLL</span><span class="sxs-lookup"><span data-stu-id="403b3-119">DLL</span></span><br/>                      | <span data-ttu-id="403b3-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="403b3-120">EndpointDlp.dll</span></span> |