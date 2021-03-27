---
description: Obtient le nom de la vue par défaut. Appelez GetDisplayNameOf pour récupérer les noms des autres vues.
title: 'IShellFolderViewType :: GetDefaultViewName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetDefaultViewName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 99229d13-40dc-4750-81a7-48a2f608b778
ms.openlocfilehash: 239fcd80bcfc0b29287f8e16aeef3efb8ae032c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972342"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a><span data-ttu-id="d28c6-104">IShellFolderViewType :: GetDefaultViewName, méthode</span><span class="sxs-lookup"><span data-stu-id="d28c6-104">IShellFolderViewType::GetDefaultViewName method</span></span>

<span data-ttu-id="d28c6-105">Obtient le nom de la vue par défaut.</span><span class="sxs-lookup"><span data-stu-id="d28c6-105">Gets the name of the default view.</span></span> <span data-ttu-id="d28c6-106">Appelez [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) pour récupérer les noms des autres vues.</span><span class="sxs-lookup"><span data-stu-id="d28c6-106">Call [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span>

## <a name="syntax"></a><span data-ttu-id="d28c6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d28c6-107">Syntax</span></span>


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="d28c6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d28c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d28c6-109">*uFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d28c6-109">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d28c6-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d28c6-110">Type: **DWORD**</span></span>

<span data-ttu-id="d28c6-111">Indicateurs facultatifs ; doit être défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="d28c6-111">Optional flags; should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="d28c6-112">*ppwszName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d28c6-112">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d28c6-113">Tapez : \**LPWStr \** _</span><span class="sxs-lookup"><span data-stu-id="d28c6-113">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="d28c6-114">Adresse d’un pointeur de chaîne qui reçoit le nom de vue par défaut.</span><span class="sxs-lookup"><span data-stu-id="d28c6-114">The address of a string pointer that receives the default view name.</span></span> <span data-ttu-id="d28c6-115">La mémoire pour la chaîne est allouée avec [_ *SHStrDup* \*](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span><span class="sxs-lookup"><span data-stu-id="d28c6-115">The memory for the string is allocated with [_ *SHStrDup*\*](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d28c6-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d28c6-116">Return value</span></span>

<span data-ttu-id="d28c6-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d28c6-117">Type: **HRESULT**</span></span>

<span data-ttu-id="d28c6-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d28c6-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d28c6-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d28c6-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d28c6-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d28c6-120">Requirements</span></span>



| <span data-ttu-id="d28c6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d28c6-121">Requirement</span></span> | <span data-ttu-id="d28c6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d28c6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d28c6-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d28c6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d28c6-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d28c6-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d28c6-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d28c6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d28c6-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d28c6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d28c6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d28c6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d28c6-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d28c6-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




