---
description: Libère le descripteur associé à la liste des derniers fichiers utilisés (MRU) et écrit les données mises en cache dans le registre.
title: FreeMRUList fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMRUList
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 51db9352-7188-4fb7-9c92-1d9579cd7250
ms.openlocfilehash: 8140586d5f428a66f27a71ea665ae6761380e3a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973198"
---
# <a name="freemrulist-function"></a><span data-ttu-id="724ca-103">FreeMRUList fonction)</span><span class="sxs-lookup"><span data-stu-id="724ca-103">FreeMRUList function</span></span>

<span data-ttu-id="724ca-104">Libère le descripteur associé à la liste des derniers fichiers utilisés (MRU) et écrit les données mises en cache dans le registre.</span><span class="sxs-lookup"><span data-stu-id="724ca-104">Frees the handle associated with the most recently used (MRU) list and writes cached data to the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="724ca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="724ca-105">Syntax</span></span>


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a><span data-ttu-id="724ca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="724ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="724ca-107">*hMRU* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="724ca-107">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="724ca-108">Type : **handle**</span><span class="sxs-lookup"><span data-stu-id="724ca-108">Type: **HANDLE**</span></span>

<span data-ttu-id="724ca-109">Handle de la liste MRU à libérer.</span><span class="sxs-lookup"><span data-stu-id="724ca-109">The handle of the MRU list to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="724ca-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="724ca-110">Return value</span></span>

<span data-ttu-id="724ca-111">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="724ca-111">Type: **int**</span></span>

<span data-ttu-id="724ca-112">Retourne une valeur non négative en cas de réussite,-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="724ca-112">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="724ca-113">Notes</span><span class="sxs-lookup"><span data-stu-id="724ca-113">Remarks</span></span>

<span data-ttu-id="724ca-114">Si la liste MRU a été créée à l’aide de l’indicateur **\_ CACHEWRITE MRU** , l’appel de **FreeMRUList** entraîne l’écriture des modifications qui n’ont pas encore été écrites dans la version de la liste MRU stockée dans le registre.</span><span class="sxs-lookup"><span data-stu-id="724ca-114">If the MRU list was created using the **MRU\_CACHEWRITE** flag, calling **FreeMRUList** causes any changes not yet written to the version of the MRU list stored in registry to be written at this time.</span></span>

<span data-ttu-id="724ca-115">Cette fonction n’est pas incluse dans un en-tête public ou une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="724ca-115">This function is not included in a public header or library.</span></span> <span data-ttu-id="724ca-116">Elle doit être extraite de comctl32.dll par l’ordinal 152.</span><span class="sxs-lookup"><span data-stu-id="724ca-116">It must be extracted from comctl32.dll by ordinal 152.</span></span>

## <a name="requirements"></a><span data-ttu-id="724ca-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="724ca-117">Requirements</span></span>



| <span data-ttu-id="724ca-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="724ca-118">Requirement</span></span> | <span data-ttu-id="724ca-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="724ca-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="724ca-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="724ca-120">Minimum supported client</span></span><br/> | <span data-ttu-id="724ca-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="724ca-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="724ca-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="724ca-122">Minimum supported server</span></span><br/> | <span data-ttu-id="724ca-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="724ca-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="724ca-124">DLL</span><span class="sxs-lookup"><span data-stu-id="724ca-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="724ca-125"><dt>Comctl32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="724ca-125"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




