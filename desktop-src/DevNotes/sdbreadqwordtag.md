---
Description: Récupère la valeur QWORD pour le TAGID spécifié.
ms.assetid: 5fa94a95-c7f3-477b-ab7c-931e8d62d501
title: SdbReadQWORDTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 15227f3d7c3177a226f1b3cc77fc78efd34379d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385199"
---
# <a name="sdbreadqwordtag-function"></a><span data-ttu-id="af7e2-103">SdbReadQWORDTag fonction)</span><span class="sxs-lookup"><span data-stu-id="af7e2-103">SdbReadQWORDTag function</span></span>

<span data-ttu-id="af7e2-104">Récupère la valeur **QWord** pour le **TagId** spécifié.</span><span class="sxs-lookup"><span data-stu-id="af7e2-104">Retrieves the **QWORD** value for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="af7e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af7e2-105">Syntax</span></span>


```C++
ULONGLONG WINAPI SdbReadQWORDTag(
  _In_ PDB       pdb,
  _In_ TAGID     tiWhich,
  _In_ ULONGLONG qwDefault
);
```



## <a name="parameters"></a><span data-ttu-id="af7e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af7e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af7e2-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af7e2-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af7e2-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="af7e2-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="af7e2-109">*tiWhich* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af7e2-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af7e2-110">**TagId** qui correspond aux données à récupérer.</span><span class="sxs-lookup"><span data-stu-id="af7e2-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="af7e2-111">*qwDefault* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af7e2-111">*qwDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af7e2-112">Valeur par défaut à retourner en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="af7e2-112">The default value to be returned on failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af7e2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af7e2-113">Return value</span></span>

<span data-ttu-id="af7e2-114">La fonction retourne la valeur en cas de réussite ou *qwDefault* en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="af7e2-114">The function returns the value on success or *qwDefault* on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="af7e2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af7e2-115">Requirements</span></span>



| <span data-ttu-id="af7e2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af7e2-116">Requirement</span></span> | <span data-ttu-id="af7e2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="af7e2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af7e2-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af7e2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="af7e2-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af7e2-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="af7e2-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af7e2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="af7e2-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af7e2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="af7e2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="af7e2-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af7e2-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af7e2-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af7e2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af7e2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af7e2-125">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="af7e2-125">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="af7e2-126">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="af7e2-126">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="af7e2-127">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="af7e2-127">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="af7e2-128">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="af7e2-128">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




