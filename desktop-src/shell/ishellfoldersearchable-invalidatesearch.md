---
description: Convertit ce pointeur vers une liste d’identificateurs d’élément (PIDL) en une partie non valide du dossier shell.
title: 'IShellFolderSearchable :: InvalidateSearch, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 36c1de0a606fdfddbe8eb74b5cc6c20cdda8e983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201708"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a><span data-ttu-id="8121d-103">IShellFolderSearchable :: InvalidateSearch, méthode</span><span class="sxs-lookup"><span data-stu-id="8121d-103">IShellFolderSearchable::InvalidateSearch method</span></span>

<span data-ttu-id="8121d-104">Convertit ce pointeur vers une liste d’identificateurs d’élément (PIDL) en une partie non valide du dossier shell.</span><span class="sxs-lookup"><span data-stu-id="8121d-104">Makes this pointer to an item identifier list (PIDL) an invalid portion of the Shell folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="8121d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8121d-105">Syntax</span></span>


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8121d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8121d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8121d-107">*pidlSearch* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8121d-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8121d-108">Type : **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="8121d-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="8121d-109">Pointeur vers la structure [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) pour le dossier de recherche.</span><span class="sxs-lookup"><span data-stu-id="8121d-109">A pointer to the [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> <dt>

<span data-ttu-id="8121d-110">*pdwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8121d-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8121d-111">Type : \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="8121d-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="8121d-112">Aucun indicateur n’est actuellement défini. définissez sur _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="8121d-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8121d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8121d-113">Return value</span></span>

<span data-ttu-id="8121d-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8121d-114">Type: **HRESULT**</span></span>

<span data-ttu-id="8121d-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8121d-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8121d-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8121d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8121d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8121d-117">Remarks</span></span>

<span data-ttu-id="8121d-118">Lorsqu’un dossier de recherche est invalidé, il peut effectuer le nettoyage des ressources qu’il a utilisées.</span><span class="sxs-lookup"><span data-stu-id="8121d-118">When a search folder is invalidated, it can perform cleanup of any resources it has used.</span></span> <span data-ttu-id="8121d-119">La méthode **IShellFolderSearchable :: InvalidateSearch** peut provoquer l’annulation d’une recherche asynchrone et provoquera la libération finale de l’objet d’interface [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="8121d-119">The **IShellFolderSearchable::InvalidateSearch** method may cause an asynchronous search to be canceled and will result in the eventual release of the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface object.</span></span>

## <a name="requirements"></a><span data-ttu-id="8121d-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8121d-120">Requirements</span></span>



| <span data-ttu-id="8121d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8121d-121">Requirement</span></span> | <span data-ttu-id="8121d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="8121d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8121d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8121d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8121d-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8121d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8121d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8121d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8121d-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8121d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8121d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8121d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8121d-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8121d-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




