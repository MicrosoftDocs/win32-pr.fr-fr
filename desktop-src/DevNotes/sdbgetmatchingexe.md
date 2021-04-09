---
description: Recherche l’exécutable spécifié.
ms.assetid: 32c6b054-7e47-4427-bdfe-6b5066db4ac3
title: SdbGetMatchingExe fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9d9c8c8c5e9ba0c55068558698b40c7274929364
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861050"
---
# <a name="sdbgetmatchingexe-function"></a><span data-ttu-id="f726f-103">SdbGetMatchingExe fonction)</span><span class="sxs-lookup"><span data-stu-id="f726f-103">SdbGetMatchingExe function</span></span>

<span data-ttu-id="f726f-104">Recherche l’exécutable spécifié.</span><span class="sxs-lookup"><span data-stu-id="f726f-104">Searches for the specified executable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f726f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f726f-105">Syntax</span></span>


```C++
BOOL WINAPI SdbGetMatchingExe(
  _In_opt_ HSDB            hSDB,
  _In_     LPCTSTR         szPath,
  _In_opt_ LPCTSTR         szModuleName,
  _In_opt_ LPCTSTR         pszEnvironment,
  _In_     DWORD           dwFlags,
  _Out_    PSDBQUERYRESULT pQueryResult
);
```



## <a name="parameters"></a><span data-ttu-id="f726f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f726f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f726f-107">*hSDB* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f726f-107">*hSDB* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f726f-108">Handle de la base de données de shims retournée par la fonction [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="f726f-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f726f-109">*szPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f726f-109">*szPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f726f-110">Chemin de l’exécutable.</span><span class="sxs-lookup"><span data-stu-id="f726f-110">The path of the executable.</span></span>

</dd> <dt>

<span data-ttu-id="f726f-111">*szModuleName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f726f-111">*szModuleName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f726f-112">Nom du module.</span><span class="sxs-lookup"><span data-stu-id="f726f-112">The module name.</span></span>

</dd> <dt>

<span data-ttu-id="f726f-113">*pszEnvironment* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f726f-113">*pszEnvironment* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f726f-114">Variables d’environnement à utiliser comme contexte de recherche.</span><span class="sxs-lookup"><span data-stu-id="f726f-114">The environment variables to be used as search context.</span></span>

</dd> <dt>

<span data-ttu-id="f726f-115">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f726f-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f726f-116">Ce paramètre peut avoir la valeur 0 ou **SDBGMEF \_ ignorer l' \_ environnement** (0x1).</span><span class="sxs-lookup"><span data-stu-id="f726f-116">This parameter can be 0 or **SDBGMEF\_IGNORE\_ENVIRONMENT** (0x1).</span></span>

</dd> <dt>

<span data-ttu-id="f726f-117">*pQueryResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f726f-117">*pQueryResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f726f-118">Structure [**SDBQUERYRESULT**](sdbqueryresult.md) .</span><span class="sxs-lookup"><span data-stu-id="f726f-118">An [**SDBQUERYRESULT**](sdbqueryresult.md) structure.</span></span> <span data-ttu-id="f726f-119">Si aucune correspondance n’est trouvée, la structure contient **TAGREF \_ null**.</span><span class="sxs-lookup"><span data-stu-id="f726f-119">If no match is found, the structure contains **TAGREF\_NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f726f-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f726f-120">Return value</span></span>

<span data-ttu-id="f726f-121">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="f726f-121">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="f726f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="f726f-122">Remarks</span></span>

<span data-ttu-id="f726f-123">Une fois que vous avez terminé avec le [**TAGREF**](tagref.md)retourné, libérez-le à l’aide de la fonction [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) .</span><span class="sxs-lookup"><span data-stu-id="f726f-123">When you have finished with the returned [**TAGREF**](tagref.md), free it using the [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f726f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f726f-124">Requirements</span></span>



| <span data-ttu-id="f726f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f726f-125">Requirement</span></span> | <span data-ttu-id="f726f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f726f-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f726f-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f726f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f726f-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f726f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f726f-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f726f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f726f-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f726f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f726f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f726f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f726f-132"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f726f-132"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f726f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f726f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f726f-134">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="f726f-134">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> <dt>

[<span data-ttu-id="f726f-135">**SdbReleaseMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="f726f-135">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
</dt> </dl>

 

 




