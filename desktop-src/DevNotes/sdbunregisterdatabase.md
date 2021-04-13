---
description: Annule l’inscription de la base de données spécifiée, ce qui la rend n’est plus disponible.
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: SdbUnregisterDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 72171e1f9ae20ac2213a285046b2499093be4313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483120"
---
# <a name="sdbunregisterdatabase-function"></a><span data-ttu-id="d73dd-103">SdbUnregisterDatabase fonction)</span><span class="sxs-lookup"><span data-stu-id="d73dd-103">SdbUnregisterDatabase function</span></span>

<span data-ttu-id="d73dd-104">Annule l’inscription de la base de données spécifiée, ce qui la rend n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="d73dd-104">Unregisters the specified database, making it no longer available.</span></span>

## <a name="syntax"></a><span data-ttu-id="d73dd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d73dd-105">Syntax</span></span>


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a><span data-ttu-id="d73dd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d73dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d73dd-107">*pguidDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d73dd-107">*pguidDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d73dd-108">GUID de la base de données.</span><span class="sxs-lookup"><span data-stu-id="d73dd-108">The GUID of the database.</span></span> <span data-ttu-id="d73dd-109">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="d73dd-109">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d73dd-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d73dd-110">Return value</span></span>

<span data-ttu-id="d73dd-111">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="d73dd-111">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d73dd-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d73dd-112">Requirements</span></span>



| <span data-ttu-id="d73dd-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d73dd-113">Requirement</span></span> | <span data-ttu-id="d73dd-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d73dd-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d73dd-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d73dd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d73dd-116">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d73dd-116">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d73dd-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d73dd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d73dd-118">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d73dd-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d73dd-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d73dd-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d73dd-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d73dd-120"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d73dd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d73dd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d73dd-122">**SdbRegisterDatabaseEx**</span><span class="sxs-lookup"><span data-stu-id="d73dd-122">**SdbRegisterDatabaseEx**</span></span>](sdbregisterdatabaseex.md)
</dt> </dl>

 

 




