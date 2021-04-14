---
description: Inscrit la base de données spécifiée.
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: SdbRegisterDatabaseEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbRegisterDatabaseEx
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 74872f8895032abe02b024396fda12c43dc1611d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523343"
---
# <a name="sdbregisterdatabaseex-function"></a><span data-ttu-id="54304-103">SdbRegisterDatabaseEx fonction)</span><span class="sxs-lookup"><span data-stu-id="54304-103">SdbRegisterDatabaseEx function</span></span>

<span data-ttu-id="54304-104">Inscrit la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="54304-104">Registers the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="54304-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54304-105">Syntax</span></span>


```C++
BOOL WINAPI SdbRegisterDatabaseEx(
  _In_     LPCTSTR    pszDatabasePath,
  _In_     DWORD      dwDatabaseType,
  _In_opt_ PULONGLONG pTimeStamp
);
```



## <a name="parameters"></a><span data-ttu-id="54304-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54304-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54304-107">*pszDatabasePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54304-107">*pszDatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54304-108">Chemin d’accès de la base de données.</span><span class="sxs-lookup"><span data-stu-id="54304-108">The database path.</span></span> <span data-ttu-id="54304-109">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="54304-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="54304-110">*dwDatabaseType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54304-110">*dwDatabaseType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54304-111">Type de base de données.</span><span class="sxs-lookup"><span data-stu-id="54304-111">The database type.</span></span> <span data-ttu-id="54304-112">Pour obtenir la liste des valeurs, consultez [types de bases de données de shims](shim-database-types.md) .</span><span class="sxs-lookup"><span data-stu-id="54304-112">See [Shim Database Types](shim-database-types.md) for a list of values.</span></span>

</dd> <dt>

<span data-ttu-id="54304-113">*pTimeStamp* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="54304-113">*pTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="54304-114">Horodatage de la base de données.</span><span class="sxs-lookup"><span data-stu-id="54304-114">The time stamp for the database.</span></span> <span data-ttu-id="54304-115">Si ce paramètre a la **valeur null**, l’heure système est utilisée.</span><span class="sxs-lookup"><span data-stu-id="54304-115">If this parameter is **NULL**, the system time is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54304-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54304-116">Return value</span></span>

<span data-ttu-id="54304-117">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="54304-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="54304-118">Notes</span><span class="sxs-lookup"><span data-stu-id="54304-118">Remarks</span></span>

<span data-ttu-id="54304-119">Une base de données doit être inscrite pour que vous puissiez utiliser d’autres fonctions SDB.</span><span class="sxs-lookup"><span data-stu-id="54304-119">A database must be registered before you can use any other SDB functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="54304-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54304-120">Requirements</span></span>



| <span data-ttu-id="54304-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54304-121">Requirement</span></span> | <span data-ttu-id="54304-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="54304-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54304-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54304-123">Minimum supported client</span></span><br/> | <span data-ttu-id="54304-124">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54304-124">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="54304-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54304-125">Minimum supported server</span></span><br/> | <span data-ttu-id="54304-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54304-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="54304-127">DLL</span><span class="sxs-lookup"><span data-stu-id="54304-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54304-128"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54304-128"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54304-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54304-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54304-130">**SdbUnregisterDatabase**</span><span class="sxs-lookup"><span data-stu-id="54304-130">**SdbUnregisterDatabase**</span></span>](sdbunregisterdatabase.md)
</dt> </dl>

 

 




