---
description: Crée une nouvelle base de données de shims.
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: SdbCreateDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 1ab8b8071cc210f6129545985d2d2e089680f0f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950612"
---
# <a name="sdbcreatedatabase-function"></a><span data-ttu-id="a14e4-103">SdbCreateDatabase fonction)</span><span class="sxs-lookup"><span data-stu-id="a14e4-103">SdbCreateDatabase function</span></span>

<span data-ttu-id="a14e4-104">Crée une nouvelle base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="a14e4-104">Creates a new shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="a14e4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a14e4-105">Syntax</span></span>


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a><span data-ttu-id="a14e4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a14e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a14e4-107">*pwszPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a14e4-107">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a14e4-108">Chemin d’accès de l’emplacement où la base de données doit être enregistrée.</span><span class="sxs-lookup"><span data-stu-id="a14e4-108">The path where the database should be saved.</span></span> <span data-ttu-id="a14e4-109">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="a14e4-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a14e4-110">*ETYPE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a14e4-110">*eType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a14e4-111">Type de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="a14e4-111">The path type.</span></span> <span data-ttu-id="a14e4-112">Pour obtenir la liste des valeurs, consultez [**\_ type de chemin d’accès**](path-type.md) .</span><span class="sxs-lookup"><span data-stu-id="a14e4-112">See [**PATH\_TYPE**](path-type.md) for a list of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a14e4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a14e4-113">Return value</span></span>

<span data-ttu-id="a14e4-114">La fonction retourne un descripteur à la base de données du shim ou **null** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="a14e4-114">The function returns a handle to the shim database or **NULL** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a14e4-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a14e4-115">Requirements</span></span>



| <span data-ttu-id="a14e4-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a14e4-116">Requirement</span></span> | <span data-ttu-id="a14e4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a14e4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a14e4-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a14e4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a14e4-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a14e4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a14e4-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a14e4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a14e4-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a14e4-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a14e4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a14e4-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a14e4-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a14e4-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a14e4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a14e4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a14e4-125">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="a14e4-125">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




