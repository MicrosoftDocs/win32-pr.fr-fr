---
description: Fournit au système des informations sur un document avant le lancement de l’opération de fermeture de fichier de document.
title: DlpNotifyCloseDocumentFile, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyCloseDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 2438829cde84e9029a86d74e4ed704e1e8d33511
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495515"
---
# <a name="dlpnotifyclosedocumentfile-function"></a><span data-ttu-id="002fa-103">DlpNotifyCloseDocumentFile fonction)</span><span class="sxs-lookup"><span data-stu-id="002fa-103">DlpNotifyCloseDocumentFile function</span></span>

<span data-ttu-id="002fa-104">Fournit au système des informations sur un document avant le lancement de l’opération de fermeture de fichier de document.</span><span class="sxs-lookup"><span data-stu-id="002fa-104">Provides the system with information about a document before the document file close operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="002fa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="002fa-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="002fa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="002fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="002fa-107">*DocumentInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="002fa-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002fa-108">Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="002fa-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="002fa-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="002fa-109">Return value</span></span>

<span data-ttu-id="002fa-110">Retourne void.</span><span class="sxs-lookup"><span data-stu-id="002fa-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="002fa-111">Notes</span><span class="sxs-lookup"><span data-stu-id="002fa-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="002fa-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="002fa-112">Requirements</span></span>


| <span data-ttu-id="002fa-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="002fa-113">Requirement</span></span>          |    <span data-ttu-id="002fa-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="002fa-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="002fa-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="002fa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="002fa-116">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="002fa-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="002fa-117">DLL</span><span class="sxs-lookup"><span data-stu-id="002fa-117">DLL</span></span><br/>                      | <span data-ttu-id="002fa-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="002fa-118">EndpointDlp.dll</span></span> |