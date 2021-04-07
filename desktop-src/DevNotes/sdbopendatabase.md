---
description: Ouvre la base de données de shims spécifiée.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: SdbOpenDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ae0bca035f203593c43bb36e70119fbaf3024059
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747853"
---
# <a name="sdbopendatabase-function"></a><span data-ttu-id="7dd0d-103">SdbOpenDatabase fonction)</span><span class="sxs-lookup"><span data-stu-id="7dd0d-103">SdbOpenDatabase function</span></span>

<span data-ttu-id="7dd0d-104">Ouvre la base de données de shims spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-104">Opens the specified shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dd0d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7dd0d-105">Syntax</span></span>


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a><span data-ttu-id="7dd0d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7dd0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dd0d-107">*pwszPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7dd0d-107">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dd0d-108">Chemin d’accès de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-108">The database path.</span></span> <span data-ttu-id="7dd0d-109">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7dd0d-110">*ETYPE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7dd0d-110">*eType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dd0d-111">Type de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-111">The path type.</span></span> <span data-ttu-id="7dd0d-112">Pour obtenir la liste des valeurs, consultez [**\_ type de chemin d’accès**](path-type.md) .</span><span class="sxs-lookup"><span data-stu-id="7dd0d-112">See [**PATH\_TYPE**](path-type.md) for a list of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dd0d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7dd0d-113">Return value</span></span>

<span data-ttu-id="7dd0d-114">La fonction retourne un descripteur à la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-114">The function returns a handle to the shim database.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dd0d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7dd0d-115">Requirements</span></span>



| <span data-ttu-id="7dd0d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7dd0d-116">Requirement</span></span> | <span data-ttu-id="7dd0d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7dd0d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd0d-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dd0d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7dd0d-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dd0d-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7dd0d-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dd0d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7dd0d-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dd0d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7dd0d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7dd0d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dd0d-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dd0d-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dd0d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dd0d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dd0d-125">**SdbCreateDatabase**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-125">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
</dt> </dl>

 

 




