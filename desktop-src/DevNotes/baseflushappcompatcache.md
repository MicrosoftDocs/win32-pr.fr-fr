---
description: Vide le cache de compatibilité des applications.
ms.assetid: 03f47813-87f6-4b71-b453-77a2facab019
title: BaseFlushAppcompatCache fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BaseFlushAppcompatCache
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-appcompat-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-appcompat-l1-1-1.dll
ms.openlocfilehash: 6118c78784bb96b9f25e008cd2221112eeb646f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110310"
---
# <a name="baseflushappcompatcache-function"></a><span data-ttu-id="56bde-103">BaseFlushAppcompatCache fonction)</span><span class="sxs-lookup"><span data-stu-id="56bde-103">BaseFlushAppcompatCache function</span></span>

<span data-ttu-id="56bde-104">Vide le cache de compatibilité des applications.</span><span class="sxs-lookup"><span data-stu-id="56bde-104">Flushes the application compatibility cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="56bde-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56bde-105">Syntax</span></span>


```C++
BOOL WINAPI BaseFlushAppcompatCache(void);
```



## <a name="parameters"></a><span data-ttu-id="56bde-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56bde-106">Parameters</span></span>

<span data-ttu-id="56bde-107">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="56bde-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56bde-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56bde-108">Return value</span></span>

<span data-ttu-id="56bde-109">La fonction retourne **true** si elle est réussie et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="56bde-109">The function returns **TRUE** if it succeeds and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="56bde-110">Notes</span><span class="sxs-lookup"><span data-stu-id="56bde-110">Remarks</span></span>

<span data-ttu-id="56bde-111">L’appelant doit être un administrateur.</span><span class="sxs-lookup"><span data-stu-id="56bde-111">The caller must be an administrator.</span></span>

## <a name="requirements"></a><span data-ttu-id="56bde-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56bde-112">Requirements</span></span>



| <span data-ttu-id="56bde-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56bde-113">Requirement</span></span> | <span data-ttu-id="56bde-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="56bde-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56bde-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56bde-115">Minimum supported client</span></span><br/> | <span data-ttu-id="56bde-116">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56bde-116">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="56bde-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56bde-117">Minimum supported server</span></span><br/> | <span data-ttu-id="56bde-118">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56bde-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="56bde-119">DLL</span><span class="sxs-lookup"><span data-stu-id="56bde-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56bde-120"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56bde-120"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56bde-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56bde-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56bde-122">**ShimFlushCache**</span><span class="sxs-lookup"><span data-stu-id="56bde-122">**ShimFlushCache**</span></span>](shimflushcache.md)
</dt> </dl>

 

 




