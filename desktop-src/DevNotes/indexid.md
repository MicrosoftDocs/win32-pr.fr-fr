---
description: Identificateur de l’index à accéder dans une base de données.
ms.assetid: 559e73bf-91c2-4dbf-a667-e5c0431aaffa
title: INDEXID contient
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b6ef6b79dd19183f575930e9793a6ab2f1f5cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111138"
---
# <a name="indexid"></a><span data-ttu-id="30860-103">INDEXID contient</span><span class="sxs-lookup"><span data-stu-id="30860-103">INDEXID</span></span>

<span data-ttu-id="30860-104">Identificateur de l’index à accéder dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="30860-104">The identifier of the index to be accessed in a database.</span></span>


```C++
typedef DWORD INDEXID;
```



## <a name="remarks"></a><span data-ttu-id="30860-105">Notes</span><span class="sxs-lookup"><span data-stu-id="30860-105">Remarks</span></span>

<span data-ttu-id="30860-106">Un **IndexID contient** peut être une valeur entière qui représente l’index ou la valeur suivante :</span><span class="sxs-lookup"><span data-stu-id="30860-106">An **INDEXID** can be an integer value that represents the index, or the following value:</span></span>

<dl> <dt>

<span data-ttu-id="30860-107"><span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>INDEXID contient \_ null ((IndexID contient)-1)</span><span class="sxs-lookup"><span data-stu-id="30860-107"><span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>INDEXID\_NULL ((INDEXID)-1)</span></span>
</dt> <dd>

<span data-ttu-id="30860-108">**IndexID contient** non valide.</span><span class="sxs-lookup"><span data-stu-id="30860-108">An invalid **INDEXID**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30860-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30860-109">Requirements</span></span>



| <span data-ttu-id="30860-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30860-110">Requirement</span></span> | <span data-ttu-id="30860-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="30860-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="30860-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30860-112">Minimum supported client</span></span><br/> | <span data-ttu-id="30860-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30860-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="30860-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30860-114">Minimum supported server</span></span><br/> | <span data-ttu-id="30860-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30860-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30860-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30860-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30860-117">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="30860-117">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="30860-118">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="30860-118">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="30860-119">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="30860-119">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




