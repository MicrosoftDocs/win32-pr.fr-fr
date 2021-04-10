---
description: Crée une clé à partir d’une chaîne.
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: SdbMakeIndexKeyFromString fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 691e691f14692775f0c681a7efa3ce91f756be1d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950367"
---
# <a name="sdbmakeindexkeyfromstring-function"></a><span data-ttu-id="f3969-103">SdbMakeIndexKeyFromString fonction)</span><span class="sxs-lookup"><span data-stu-id="f3969-103">SdbMakeIndexKeyFromString function</span></span>

<span data-ttu-id="f3969-104">Crée une clé à partir d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f3969-104">Creates a key from a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3969-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3969-105">Syntax</span></span>


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a><span data-ttu-id="f3969-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3969-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3969-107">*pwszKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f3969-107">*pwszKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3969-108">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="f3969-108">The string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3969-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f3969-109">Return value</span></span>

<span data-ttu-id="f3969-110">La fonction retourne la clé ou 0 en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f3969-110">The function returns the key or 0 if there is an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3969-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f3969-111">Remarks</span></span>

<span data-ttu-id="f3969-112">La clé d’index standard est les huit premiers caractères de la chaîne, convertis en majuscules, puis castés en valeur **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="f3969-112">The standard index key is the first eight characters of the string, converted to upper case, then cast to a **ULONGLONG** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3969-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3969-113">Requirements</span></span>



| <span data-ttu-id="f3969-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3969-114">Requirement</span></span> | <span data-ttu-id="f3969-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3969-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3969-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3969-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f3969-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3969-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f3969-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3969-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f3969-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3969-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f3969-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f3969-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3969-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3969-121"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




