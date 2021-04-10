---
description: Récupère les données de chaîne pour le TAGID spécifié.
ms.assetid: c558e0bb-7e35-4298-93fb-400db00a2972
title: SdbGetStringTagPtr fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetStringTagPtr
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 56c80c4000df95fe13486d95bb872bfc39274389
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950611"
---
# <a name="sdbgetstringtagptr-function"></a><span data-ttu-id="2e6e3-103">SdbGetStringTagPtr fonction)</span><span class="sxs-lookup"><span data-stu-id="2e6e3-103">SdbGetStringTagPtr function</span></span>

<span data-ttu-id="2e6e3-104">Récupère les données de chaîne pour le **TagId** spécifié.</span><span class="sxs-lookup"><span data-stu-id="2e6e3-104">Retrieves the string data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e6e3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e6e3-105">Syntax</span></span>


```C++
LPTSTR WINAPI SdbGetStringTagPtr(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="2e6e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e6e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e6e3-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e6e3-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e6e3-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="2e6e3-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="2e6e3-109">*tiWhich* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e6e3-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e6e3-110">**TagId** qui correspond aux données de chaîne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="2e6e3-110">The **TAGID** that corresponds to the string data to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e6e3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e6e3-111">Return value</span></span>

<span data-ttu-id="2e6e3-112">La fonction retourne un pointeur vers les données de chaîne ou la **valeur null** si le **TagId** n’est pas valide ou n’est pas de type **\_ \_ chaîne** ou type de **balise \_ \_ STRINGREF**.</span><span class="sxs-lookup"><span data-stu-id="2e6e3-112">The function returns a pointer to the string data or **NULL** if the **TAGID** is invalid or not of type **TAG\_TYPE\_STRING** or **TAG\_TYPE\_STRINGREF**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e6e3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e6e3-113">Requirements</span></span>



| <span data-ttu-id="2e6e3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e6e3-114">Requirement</span></span> | <span data-ttu-id="2e6e3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e6e3-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e6e3-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e6e3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2e6e3-117">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e6e3-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2e6e3-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e6e3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2e6e3-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e6e3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2e6e3-120">DLL</span><span class="sxs-lookup"><span data-stu-id="2e6e3-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e6e3-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e6e3-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e6e3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e6e3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e6e3-123">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="2e6e3-123">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="2e6e3-124">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="2e6e3-124">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="2e6e3-125">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="2e6e3-125">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="2e6e3-126">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="2e6e3-126">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




