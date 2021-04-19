---
description: Fournit au système des informations sur un document lors de la sortie d’une cible de déplacement.
title: DlpNotifyLeaveDropTarget, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyLeaveDropTarget
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 2f96ea9a825ca930631fe94dd1a3d632019dd9c1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495512"
---
# <a name="dlpnotifyleavedroptarget-function"></a><span data-ttu-id="f357c-103">DlpNotifyLeaveDropTarget fonction)</span><span class="sxs-lookup"><span data-stu-id="f357c-103">DlpNotifyLeaveDropTarget function</span></span>

<span data-ttu-id="f357c-104">Fournit au système des informations sur un document lors de la sortie d’une cible de déplacement.</span><span class="sxs-lookup"><span data-stu-id="f357c-104">Provides the system with information about a document when a drop target is exited.</span></span>

## <a name="syntax"></a><span data-ttu-id="f357c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f357c-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="f357c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f357c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f357c-107">*DocumentInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f357c-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f357c-108">Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document associé à l’opération de déplacement.</span><span class="sxs-lookup"><span data-stu-id="f357c-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drop operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="f357c-109">*OpStatus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f357c-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f357c-110">Pointeur vers une structure [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenant des informations d’État sur l’opération de sortie de la cible de déplacement.</span><span class="sxs-lookup"><span data-stu-id="f357c-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the drop target exit operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="f357c-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f357c-111">Return value</span></span>

<span data-ttu-id="f357c-112">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="f357c-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="f357c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f357c-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="f357c-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f357c-114">Requirements</span></span>



| <span data-ttu-id="f357c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f357c-115">Requirement</span></span>          |    <span data-ttu-id="f357c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f357c-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f357c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f357c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f357c-118">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="f357c-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="f357c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f357c-119">DLL</span></span><br/>                      | <span data-ttu-id="f357c-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="f357c-120">EndpointDlp.dll</span></span> |