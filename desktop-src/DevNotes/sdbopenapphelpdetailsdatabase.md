---
description: Ouvre la base de données de détails AppHelp spécifiée.
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: SdbOpenApphelpDetailsDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpDetailsDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2810b0bbe1f10f013f39570aecda448a4ceeea6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109915"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a><span data-ttu-id="f125e-103">SdbOpenApphelpDetailsDatabase fonction)</span><span class="sxs-lookup"><span data-stu-id="f125e-103">SdbOpenApphelpDetailsDatabase function</span></span>

<span data-ttu-id="f125e-104">Ouvre la base de données de détails AppHelp spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f125e-104">Opens the specified Apphelp details database.</span></span>

## <a name="syntax"></a><span data-ttu-id="f125e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f125e-105">Syntax</span></span>


```C++
PDB WINAPI SdbOpenApphelpDetailsDatabase(
  _In_opt_ LPCWSTR pwsDetailsDatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="f125e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f125e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f125e-107">*pwsDetailsDatabasePath* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f125e-107">*pwsDetailsDatabasePath* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f125e-108">Chemin d’accès de la base de données.</span><span class="sxs-lookup"><span data-stu-id="f125e-108">The database path.</span></span> <span data-ttu-id="f125e-109">Si ce paramètre a la **valeur null**, la base de données système locale est ouverte.</span><span class="sxs-lookup"><span data-stu-id="f125e-109">If this parameter is **NULL**, the local system database is opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f125e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f125e-110">Return value</span></span>

<span data-ttu-id="f125e-111">La fonction retourne un descripteur à la base de données de détails AppHelp.</span><span class="sxs-lookup"><span data-stu-id="f125e-111">The function returns a handle to the Apphelp details database.</span></span>

## <a name="requirements"></a><span data-ttu-id="f125e-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f125e-112">Requirements</span></span>



| <span data-ttu-id="f125e-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f125e-113">Requirement</span></span> | <span data-ttu-id="f125e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f125e-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f125e-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f125e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f125e-116">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f125e-116">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f125e-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f125e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f125e-118">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f125e-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f125e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f125e-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f125e-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f125e-120"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




