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
ms.openlocfilehash: 3146fea4f6c8d8547c8c86096b434cbaea5b5926
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842990"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a><span data-ttu-id="f89ec-103">IShellFolderSearchable :: CancelAsyncSearch, méthode</span><span class="sxs-lookup"><span data-stu-id="f89ec-103">IShellFolderSearchable::CancelAsyncSearch method</span></span>

<span data-ttu-id="f89ec-104">Commence le processus d’annulation d’une recherche asynchrone en attente.</span><span class="sxs-lookup"><span data-stu-id="f89ec-104">Begins the process of canceling a pending asynchronous search.</span></span>

## <a name="syntax"></a><span data-ttu-id="f89ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f89ec-105">Syntax</span></span>


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f89ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f89ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f89ec-107">*pidlSearch* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f89ec-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f89ec-108">Type : **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="f89ec-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="f89ec-109">Pointeur vers un [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="f89ec-109">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) for the search.</span></span>

</dd> <dt>

<span data-ttu-id="f89ec-110">*pdwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f89ec-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f89ec-111">Type : **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="f89ec-111">Type: **DWORD\***</span></span>

<span data-ttu-id="f89ec-112">Aucun indicateur n’est actuellement défini. Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="f89ec-112">No flags are currently defined; set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f89ec-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f89ec-113">Return value</span></span>

<span data-ttu-id="f89ec-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f89ec-114">Type: **HRESULT**</span></span>

<span data-ttu-id="f89ec-115">Retourne S \_ OK en cas d’annulation, ou \_ a la valeur false si la recherche n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f89ec-115">Returns S\_OK if canceling, or S\_FALSE if search is not running.</span></span>

## <a name="remarks"></a><span data-ttu-id="f89ec-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f89ec-116">Remarks</span></span>

<span data-ttu-id="f89ec-117">Lorsque la recherche est effectivement annulée, [**RunEnd**](ishellfoldersearchablecallback-runend.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="f89ec-117">When the search is actually canceled, [**RunEnd**](ishellfoldersearchablecallback-runend.md) will be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="f89ec-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f89ec-118">Requirements</span></span>



| <span data-ttu-id="f89ec-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f89ec-119">Requirement</span></span> | <span data-ttu-id="f89ec-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f89ec-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f89ec-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f89ec-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f89ec-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f89ec-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f89ec-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f89ec-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f89ec-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f89ec-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f89ec-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f89ec-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f89ec-126"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f89ec-126"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




