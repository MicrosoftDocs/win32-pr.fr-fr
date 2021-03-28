---
description: Commence le processus d’annulation d’une recherche asynchrone en attente.
title: 'IShellFolderSearchable :: CancelAsyncSearch, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.CancelAsyncSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5c920dca-fbca-48e1-9dce-38713cf1fcef
ms.openlocfilehash: e9e3231e8cc602a4e00b6ee79a25392717b6e68b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972350"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a><span data-ttu-id="6d090-103">IShellFolderSearchable :: CancelAsyncSearch, méthode</span><span class="sxs-lookup"><span data-stu-id="6d090-103">IShellFolderSearchable::CancelAsyncSearch method</span></span>

<span data-ttu-id="6d090-104">Commence le processus d’annulation d’une recherche asynchrone en attente.</span><span class="sxs-lookup"><span data-stu-id="6d090-104">Begins the process of canceling a pending asynchronous search.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d090-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d090-105">Syntax</span></span>


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6d090-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d090-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d090-107">*pidlSearch* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d090-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d090-108">Type : **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="6d090-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="6d090-109">Pointeur vers un [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="6d090-109">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) for the search.</span></span>

</dd> <dt>

<span data-ttu-id="6d090-110">*pdwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d090-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d090-111">Type : \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="6d090-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="6d090-112">Aucun indicateur n’est actuellement défini. définissez sur _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="6d090-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d090-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d090-113">Return value</span></span>

<span data-ttu-id="6d090-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6d090-114">Type: **HRESULT**</span></span>

<span data-ttu-id="6d090-115">Retourne S \_ OK en cas d’annulation, ou \_ a la valeur false si la recherche n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6d090-115">Returns S\_OK if canceling, or S\_FALSE if search is not running.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d090-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6d090-116">Remarks</span></span>

<span data-ttu-id="6d090-117">Lorsque la recherche est effectivement annulée, [**RunEnd**](ishellfoldersearchablecallback-runend.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="6d090-117">When the search is actually canceled, [**RunEnd**](ishellfoldersearchablecallback-runend.md) will be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d090-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6d090-118">Requirements</span></span>



| <span data-ttu-id="6d090-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d090-119">Requirement</span></span> | <span data-ttu-id="6d090-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d090-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d090-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d090-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6d090-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d090-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6d090-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d090-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6d090-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d090-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6d090-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6d090-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d090-126"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d090-126"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




