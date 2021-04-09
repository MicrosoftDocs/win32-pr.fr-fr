---
description: Ferme la base de données spécifiée.
ms.assetid: 69546f03-9912-401a-9c1a-b7fdbe16dbf8
title: SdbCloseDatabaseWrite fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabaseWrite
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 24df6f9ce2c4f0fae4dd1c1ef244e006ea00c047
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860985"
---
# <a name="sdbclosedatabasewrite-function"></a><span data-ttu-id="d7d65-103">SdbCloseDatabaseWrite fonction)</span><span class="sxs-lookup"><span data-stu-id="d7d65-103">SdbCloseDatabaseWrite function</span></span>

<span data-ttu-id="d7d65-104">Ferme la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d7d65-104">Closes the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7d65-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7d65-105">Syntax</span></span>


```C++
void WINAPI SdbCloseDatabaseWrite(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="d7d65-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7d65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7d65-107">fichier *PDB* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d7d65-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7d65-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="d7d65-108">A handle to the shim database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7d65-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d7d65-109">Return value</span></span>

<span data-ttu-id="d7d65-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d7d65-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7d65-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d7d65-111">Remarks</span></span>

<span data-ttu-id="d7d65-112">Cette fonction appelle [**SdbCloseDatabase**](sdbclosedatabase.md); par conséquent, ces deux fonctions sont équivalentes.</span><span class="sxs-lookup"><span data-stu-id="d7d65-112">This function calls [**SdbCloseDatabase**](sdbclosedatabase.md); therefore, these two functions are equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7d65-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7d65-113">Requirements</span></span>



| <span data-ttu-id="d7d65-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7d65-114">Requirement</span></span> | <span data-ttu-id="d7d65-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7d65-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7d65-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7d65-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d7d65-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7d65-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d7d65-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7d65-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d7d65-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7d65-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d7d65-120">DLL</span><span class="sxs-lookup"><span data-stu-id="d7d65-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7d65-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7d65-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7d65-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7d65-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7d65-123">**SdbBeginWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="d7d65-123">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="d7d65-124">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="d7d65-124">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="d7d65-125">**SdbEndWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="d7d65-125">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
</dt> </dl>

 

 




