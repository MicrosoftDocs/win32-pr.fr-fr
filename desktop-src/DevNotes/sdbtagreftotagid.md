---
description: Récupère le TAGID et un descripteur de la base de données de shims pour le TAGREF spécifié.
ms.assetid: 869c6af5-4c10-4358-9d6a-1a354be6f4e9
title: SdbTagRefToTagID fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagRefToTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: faff00adc25a741342e586adea2f645a62eca36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110426"
---
# <a name="sdbtagreftotagid-function"></a><span data-ttu-id="8bcf2-103">SdbTagRefToTagID fonction)</span><span class="sxs-lookup"><span data-stu-id="8bcf2-103">SdbTagRefToTagID function</span></span>

<span data-ttu-id="8bcf2-104">Récupère le **TagId** et un descripteur de la base de données de shims pour le [**TAGREF**](tagref.md)spécifié.</span><span class="sxs-lookup"><span data-stu-id="8bcf2-104">Retrieves the **TAGID** and a handle to the shim database for the specified [**TAGREF**](tagref.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8bcf2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8bcf2-105">Syntax</span></span>


```C++
BOOL WINAPI SdbTagRefToTagID(
  _In_  HSDB   hSDB,
  _In_  TAGREF trWhich,
  _Out_ PDB    *ppdb,
  _Out_ TAGID  *ptiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="8bcf2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bcf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bcf2-107">*hSDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8bcf2-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bcf2-108">Handle de la base de données de shims retournée par la fonction [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="8bcf2-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8bcf2-109">*trWhich* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8bcf2-109">*trWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bcf2-110">[**TAGREF**](tagref.md).</span><span class="sxs-lookup"><span data-stu-id="8bcf2-110">The [**TAGREF**](tagref.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bcf2-111">*PPDB* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8bcf2-111">*ppdb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bcf2-112">Handle résultant de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="8bcf2-112">The resulting handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="8bcf2-113">*ptiWhich* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8bcf2-113">*ptiWhich* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bcf2-114">**TagId** résultant.</span><span class="sxs-lookup"><span data-stu-id="8bcf2-114">The resulting **TAGID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bcf2-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8bcf2-115">Return value</span></span>

<span data-ttu-id="8bcf2-116">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="8bcf2-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bcf2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bcf2-117">Requirements</span></span>



| <span data-ttu-id="8bcf2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bcf2-118">Requirement</span></span> | <span data-ttu-id="8bcf2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bcf2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bcf2-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bcf2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8bcf2-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8bcf2-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8bcf2-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bcf2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8bcf2-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8bcf2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8bcf2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8bcf2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bcf2-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bcf2-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bcf2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bcf2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bcf2-127">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="8bcf2-127">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> <dt>

[<span data-ttu-id="8bcf2-128">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="8bcf2-128">**TAGID**</span></span>](tagid.md)
</dt> <dt>

[<span data-ttu-id="8bcf2-129">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="8bcf2-129">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




