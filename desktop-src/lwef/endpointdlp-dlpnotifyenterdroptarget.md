---
description: Fournit au système des informations sur un document quand une cible de déplacement est entrée.
title: DlpNotifyEnterDropTarget, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyEnterDropTarget
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: ec1eee1cee7bbcc38ce3094e3e2f8b650cf3b2a9
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495511"
---
# <a name="dlpnotifyenterdroptarget-function"></a><span data-ttu-id="824f3-103">DlpNotifyEnterDropTarget fonction)</span><span class="sxs-lookup"><span data-stu-id="824f3-103">DlpNotifyEnterDropTarget function</span></span>

<span data-ttu-id="824f3-104">Fournit au système des informations sur un document quand une cible de déplacement est entrée.</span><span class="sxs-lookup"><span data-stu-id="824f3-104">Provides the system with information about a document when a drop target is entered.</span></span>

## <a name="syntax"></a><span data-ttu-id="824f3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="824f3-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="824f3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="824f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="824f3-107">*DocumentInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="824f3-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="824f3-108">Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document associé à l’opération de déplacement.</span><span class="sxs-lookup"><span data-stu-id="824f3-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drop operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="824f3-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="824f3-109">Return value</span></span>

<span data-ttu-id="824f3-110">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="824f3-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="824f3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="824f3-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="824f3-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="824f3-112">Requirements</span></span>



| <span data-ttu-id="824f3-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="824f3-113">Requirement</span></span>          |    <span data-ttu-id="824f3-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="824f3-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="824f3-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="824f3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="824f3-116">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="824f3-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="824f3-117">DLL</span><span class="sxs-lookup"><span data-stu-id="824f3-117">DLL</span></span><br/>                      | <span data-ttu-id="824f3-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="824f3-118">EndpointDlp.dll</span></span> |