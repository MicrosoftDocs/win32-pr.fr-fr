---
description: La fonction DestroyHandoffTable détruit une table de remise créée avec CreateHandoffTable.
ms.assetid: 01ae9899-4f7c-4706-a2ce-9f55b112351d
title: DestroyHandoffTable, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7afccfd1932c57b2a0d77dbb5467afc31726c6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951896"
---
# <a name="destroyhandofftable-function"></a><span data-ttu-id="b5ad3-103">DestroyHandoffTable fonction)</span><span class="sxs-lookup"><span data-stu-id="b5ad3-103">DestroyHandoffTable function</span></span>

<span data-ttu-id="b5ad3-104">La fonction **DestroyHandoffTable** détruit une table de remise créée avec **CreateHandoffTable**.</span><span class="sxs-lookup"><span data-stu-id="b5ad3-104">The **DestroyHandoffTable** function destroys a handoff table created with **CreateHandoffTable**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ad3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5ad3-105">Syntax</span></span>


```C++
VOID WINAPI DestroyHandoffTable(
  _In_ LPHANDOFFTABLE hTable
);
```



## <a name="parameters"></a><span data-ttu-id="b5ad3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5ad3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5ad3-107">*htable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5ad3-107">*hTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ad3-108">Handle vers la table de remise détruite.</span><span class="sxs-lookup"><span data-stu-id="b5ad3-108">Handle to the destroyed handoff table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5ad3-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5ad3-109">Return value</span></span>

<span data-ttu-id="b5ad3-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="b5ad3-110">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ad3-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5ad3-111">Requirements</span></span>



| <span data-ttu-id="b5ad3-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5ad3-112">Requirement</span></span> | <span data-ttu-id="b5ad3-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5ad3-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ad3-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5ad3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b5ad3-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5ad3-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b5ad3-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5ad3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b5ad3-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5ad3-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b5ad3-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5ad3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5ad3-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5ad3-119"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b5ad3-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5ad3-120">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5ad3-121"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5ad3-121"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5ad3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b5ad3-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5ad3-123"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5ad3-123"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




