---
description: Détermine si l’application doit extraire les données du presse-papiers du système au lieu de les extraire de son cache interne.
title: DlpMustPasteFromSystemClipboard, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpMustPasteFromSystemClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5863173b02cb5c63a2de46653c2d268464e82e65
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495520"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a><span data-ttu-id="b2ff5-103">DlpMustPasteFromSystemClipboard fonction)</span><span class="sxs-lookup"><span data-stu-id="b2ff5-103">DlpMustPasteFromSystemClipboard function</span></span>

<span data-ttu-id="b2ff5-104">Détermine si l’application doit extraire les données du presse-papiers du système au lieu de les extraire de son cache interne.</span><span class="sxs-lookup"><span data-stu-id="b2ff5-104">Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2ff5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2ff5-105">Syntax</span></span>


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a><span data-ttu-id="b2ff5-106">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b2ff5-106">Return value</span></span>

<span data-ttu-id="b2ff5-107">TRUE si l’appel dans le presse-papiers du système d’exploitation est obligatoire ; Sinon, FALSe.</span><span class="sxs-lookup"><span data-stu-id="b2ff5-107">TRUE if calling into the OS clipboard is mandatory; otherwise, FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2ff5-108">Notes</span><span class="sxs-lookup"><span data-stu-id="b2ff5-108">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="b2ff5-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b2ff5-109">Requirements</span></span>



| <span data-ttu-id="b2ff5-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2ff5-110">Requirement</span></span>          |    <span data-ttu-id="b2ff5-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2ff5-111">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2ff5-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2ff5-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b2ff5-113">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="b2ff5-113">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="b2ff5-114">DLL</span><span class="sxs-lookup"><span data-stu-id="b2ff5-114">DLL</span></span><br/>                      | <span data-ttu-id="b2ff5-115">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="b2ff5-115">EndpointDlp.dll</span></span> |