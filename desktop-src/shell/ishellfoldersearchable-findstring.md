---
description: Commence une recherche pour une chaîne de recherche spécifiée.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: 'IShellFolderSearchable :: FindString, méthode (MMC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.FindString
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e256329bc235f7fe5a0428ba33710fa6b838f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753061"
---
# <a name="ishellfoldersearchablefindstring-method"></a><span data-ttu-id="551af-103">IShellFolderSearchable :: FindString, méthode</span><span class="sxs-lookup"><span data-stu-id="551af-103">IShellFolderSearchable::FindString method</span></span>

<span data-ttu-id="551af-104">Commence une recherche pour une chaîne de recherche spécifiée.</span><span class="sxs-lookup"><span data-stu-id="551af-104">Begins a search for a specified search string.</span></span>

## <a name="syntax"></a><span data-ttu-id="551af-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="551af-105">Syntax</span></span>


```C++
HRESULT FindString(
  [in]  LPCWSTR      pwszTarget,
  [in]  DWORD        *pdwFlags,
  [in]  IUnknown     *punkOnAsyncSearch,
  [out] LPITEMIDLIST ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="551af-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="551af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="551af-107">*pwszTarget* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="551af-107">*pwszTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="551af-108">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="551af-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="551af-109">Pointeur vers une chaîne qui spécifie le mot clé de recherche.</span><span class="sxs-lookup"><span data-stu-id="551af-109">A pointer to a string that specifies the search keyword.</span></span>

</dd> <dt>

<span data-ttu-id="551af-110">*pdwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="551af-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="551af-111">Type : \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="551af-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="551af-112">Aucun indicateur n’est actuellement défini. définissez sur _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="551af-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="551af-113">*punkOnAsyncSearch* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="551af-113">*punkOnAsyncSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="551af-114">Tapez : \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="551af-114">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="551af-115">Pointeur vers un objet de type [_ *IUnknown* \*](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="551af-115">A pointer to an object of type [_ *IUnknown*\*](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="551af-116">Cet objet doit prendre en charge l’interface [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="551af-116">This object must support the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface.</span></span> <span data-ttu-id="551af-117">Affectez la valeur **null** si aucun rappel n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="551af-117">Set to **NULL** if no callback is necessary.</span></span>

</dd> <dt>

<span data-ttu-id="551af-118">*ppidlOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="551af-118">*ppidlOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="551af-119">Type : **LPITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="551af-119">Type: **LPITEMIDLIST**</span></span>

<span data-ttu-id="551af-120">Pointeur vers une structure [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) pour le dossier de recherche.</span><span class="sxs-lookup"><span data-stu-id="551af-120">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="551af-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="551af-121">Return value</span></span>

<span data-ttu-id="551af-122">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="551af-122">Type: **HRESULT**</span></span>

<span data-ttu-id="551af-123">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="551af-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="551af-124">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="551af-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="551af-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="551af-125">Requirements</span></span>



| <span data-ttu-id="551af-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="551af-126">Requirement</span></span> | <span data-ttu-id="551af-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="551af-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="551af-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="551af-128">Minimum supported client</span></span><br/> | <span data-ttu-id="551af-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="551af-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="551af-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="551af-130">Minimum supported server</span></span><br/> | <span data-ttu-id="551af-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="551af-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="551af-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="551af-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="551af-133"><dt>MMC. h</dt></span><span class="sxs-lookup"><span data-stu-id="551af-133"><dt>Mmc.h</dt></span></span> </dl>       |
| <span data-ttu-id="551af-134">DLL</span><span class="sxs-lookup"><span data-stu-id="551af-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="551af-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="551af-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
