---
description: Ferme la base de données de shims spécifiée.
ms.assetid: e4480860-8055-4134-b6ed-926c010d462f
title: SdbCloseDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 376d97b8386f127a945cb118639be1e38ae68737
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033673"
---
# <a name="sdbclosedatabase-function"></a><span data-ttu-id="e4557-103">SdbCloseDatabase fonction)</span><span class="sxs-lookup"><span data-stu-id="e4557-103">SdbCloseDatabase function</span></span>

<span data-ttu-id="e4557-104">Ferme la base de données de shims spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e4557-104">Closes the specified shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4557-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4557-105">Syntax</span></span>


```C++
void WINAPI SdbCloseDatabase(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="e4557-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4557-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4557-107">fichier *PDB* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e4557-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4557-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="e4557-108">A handle to the shim database.</span></span> <span data-ttu-id="e4557-109">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="e4557-109">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4557-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e4557-110">Return value</span></span>

<span data-ttu-id="e4557-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e4557-111">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4557-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4557-112">Requirements</span></span>



| <span data-ttu-id="e4557-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4557-113">Requirement</span></span> | <span data-ttu-id="e4557-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4557-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4557-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4557-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e4557-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4557-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e4557-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4557-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e4557-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4557-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e4557-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e4557-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4557-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4557-120"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4557-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4557-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4557-122">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="e4557-122">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




