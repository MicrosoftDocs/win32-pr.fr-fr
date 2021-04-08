---
description: Libère les données d’attribut de fichier spécifiées.
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: SdbFreeFileAttributes fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFreeFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 6f28812fbbec83dd1a41c8a21cb4c9544dbefea5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747685"
---
# <a name="sdbfreefileattributes-function"></a><span data-ttu-id="6a84e-103">SdbFreeFileAttributes fonction)</span><span class="sxs-lookup"><span data-stu-id="6a84e-103">SdbFreeFileAttributes function</span></span>

<span data-ttu-id="6a84e-104">Libère les données d’attribut de fichier spécifiées.</span><span class="sxs-lookup"><span data-stu-id="6a84e-104">Frees the specified file attribute data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a84e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a84e-105">Syntax</span></span>


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="6a84e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a84e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a84e-107">*pFileAttributes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a84e-107">*pFileAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a84e-108">Structure [**ATTRINFO**](attrinfo.md) retournée par la fonction [**SdbGetFileAttributes**](sdbgetfileattributes.md) .</span><span class="sxs-lookup"><span data-stu-id="6a84e-108">An [**ATTRINFO**](attrinfo.md) structure returned by the [**SdbGetFileAttributes**](sdbgetfileattributes.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a84e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a84e-109">Return value</span></span>

<span data-ttu-id="6a84e-110">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="6a84e-110">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a84e-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a84e-111">Requirements</span></span>



| <span data-ttu-id="6a84e-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a84e-112">Requirement</span></span> | <span data-ttu-id="6a84e-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a84e-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a84e-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a84e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6a84e-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a84e-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6a84e-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a84e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6a84e-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a84e-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6a84e-118">DLL</span><span class="sxs-lookup"><span data-stu-id="6a84e-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a84e-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a84e-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a84e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a84e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a84e-121">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="6a84e-121">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




