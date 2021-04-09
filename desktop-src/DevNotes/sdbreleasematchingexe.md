---
description: Libère les ressources utilisées par la fonction SdbGetMatchingExe.
ms.assetid: 4a784f72-2108-4d5e-86e1-1960ac921c8f
title: SdbReleaseMatchingExe fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c98d9a79e8942f4bd3ea4c41119825d862de1418
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033639"
---
# <a name="sdbreleasematchingexe-function"></a><span data-ttu-id="4cf0e-103">SdbReleaseMatchingExe fonction)</span><span class="sxs-lookup"><span data-stu-id="4cf0e-103">SdbReleaseMatchingExe function</span></span>

<span data-ttu-id="4cf0e-104">Libère les ressources utilisées par la fonction [**SdbGetMatchingExe**](sdbgetmatchingexe.md) .</span><span class="sxs-lookup"><span data-stu-id="4cf0e-104">Releases resources used by the [**SdbGetMatchingExe**](sdbgetmatchingexe.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cf0e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cf0e-105">Syntax</span></span>


```C++
void WINAPI SdbReleaseMatchingExe(
  _In_ HSDB   hSDB,
  _In_ TAGREF trExe
);
```



## <a name="parameters"></a><span data-ttu-id="4cf0e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4cf0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cf0e-107">*hSDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4cf0e-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cf0e-108">Handle de la base de données de shims retournée par la fonction [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="4cf0e-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4cf0e-109">*trExe* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4cf0e-109">*trExe* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cf0e-110">[**TAGREF**](tagref.md) retourné par [**SdbGetMatchingExe**](sdbgetmatchingexe.md).</span><span class="sxs-lookup"><span data-stu-id="4cf0e-110">The [**TAGREF**](tagref.md) returned by [**SdbGetMatchingExe**](sdbgetmatchingexe.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cf0e-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4cf0e-111">Return value</span></span>

<span data-ttu-id="4cf0e-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4cf0e-112">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cf0e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4cf0e-113">Requirements</span></span>



| <span data-ttu-id="4cf0e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4cf0e-114">Requirement</span></span> | <span data-ttu-id="4cf0e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cf0e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf0e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cf0e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4cf0e-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4cf0e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4cf0e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cf0e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4cf0e-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4cf0e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4cf0e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4cf0e-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cf0e-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cf0e-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cf0e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cf0e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf0e-123">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="4cf0e-123">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> <dt>

[<span data-ttu-id="4cf0e-124">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="4cf0e-124">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




