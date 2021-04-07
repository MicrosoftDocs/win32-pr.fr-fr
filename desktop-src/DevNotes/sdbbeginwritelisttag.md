---
description: Crée une nouvelle BALIse de liste pour les opérations d’écriture.
ms.assetid: 3a52e2f2-9648-45fb-b487-ccfe5ed24f7f
title: SdbBeginWriteListTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbBeginWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a9dcf6bdd3798b18e08b796eb268f93dc4ec6bbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748748"
---
# <a name="sdbbeginwritelisttag-function"></a><span data-ttu-id="27011-103">SdbBeginWriteListTag fonction)</span><span class="sxs-lookup"><span data-stu-id="27011-103">SdbBeginWriteListTag function</span></span>

<span data-ttu-id="27011-104">Crée une nouvelle BALIse de liste pour les opérations d’écriture.</span><span class="sxs-lookup"><span data-stu-id="27011-104">Creates a new list TAG for write operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="27011-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27011-105">Syntax</span></span>


```C++
TAGID WINAPI SdbBeginWriteListTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a><span data-ttu-id="27011-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27011-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27011-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="27011-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27011-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="27011-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="27011-109">*tTag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="27011-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27011-110">BALIse pour la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="27011-110">The TAG for the new entry.</span></span> <span data-ttu-id="27011-111">Cette valeur doit être de type **\_ \_ liste de types de balises**.</span><span class="sxs-lookup"><span data-stu-id="27011-111">This value must be of type **TAG\_TYPE\_LIST**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27011-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="27011-112">Return value</span></span>

<span data-ttu-id="27011-113">La fonction retourne le [**TagId**](tagid.md) de la nouvelle liste en cas de réussite ou **TagId \_ null** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="27011-113">The function returns the [**TAGID**](tagid.md) of the new list on success or **TAGID\_NULL** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="27011-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27011-114">Requirements</span></span>



| <span data-ttu-id="27011-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27011-115">Requirement</span></span> | <span data-ttu-id="27011-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="27011-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27011-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27011-117">Minimum supported client</span></span><br/> | <span data-ttu-id="27011-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27011-118">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="27011-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27011-119">Minimum supported server</span></span><br/> | <span data-ttu-id="27011-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27011-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="27011-121">DLL</span><span class="sxs-lookup"><span data-stu-id="27011-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27011-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27011-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27011-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27011-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27011-124">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="27011-124">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="27011-125">**SdbCloseDatabaseWrite**</span><span class="sxs-lookup"><span data-stu-id="27011-125">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
</dt> <dt>

[<span data-ttu-id="27011-126">**SdbEndWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="27011-126">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="27011-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="27011-127">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="27011-128">Types de BALISes</span><span class="sxs-lookup"><span data-stu-id="27011-128">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="27011-129">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="27011-129">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




