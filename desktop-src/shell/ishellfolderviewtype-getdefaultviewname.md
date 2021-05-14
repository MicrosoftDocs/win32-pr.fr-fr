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
ms.openlocfilehash: 808f68093512e2da602d5e73775b47943b140a46
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842760"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a><span data-ttu-id="d6ab0-104">IShellFolderViewType :: GetDefaultViewName, méthode</span><span class="sxs-lookup"><span data-stu-id="d6ab0-104">IShellFolderViewType::GetDefaultViewName method</span></span>

<span data-ttu-id="d6ab0-105">Obtient le nom de la vue par défaut.</span><span class="sxs-lookup"><span data-stu-id="d6ab0-105">Gets the name of the default view.</span></span> <span data-ttu-id="d6ab0-106">Appelez [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) pour récupérer les noms des autres vues.</span><span class="sxs-lookup"><span data-stu-id="d6ab0-106">Call [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6ab0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6ab0-107">Syntax</span></span>


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="d6ab0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6ab0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6ab0-109">*uFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6ab0-109">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ab0-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d6ab0-110">Type: **DWORD**</span></span>

<span data-ttu-id="d6ab0-111">Indicateurs facultatifs ; doit être défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="d6ab0-111">Optional flags; should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="d6ab0-112">*ppwszName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d6ab0-112">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ab0-113">Type : **LPWStr \***</span><span class="sxs-lookup"><span data-stu-id="d6ab0-113">Type: **LPWSTR\***</span></span>

<span data-ttu-id="d6ab0-114">Adresse d’un pointeur de chaîne qui reçoit le nom de vue par défaut.</span><span class="sxs-lookup"><span data-stu-id="d6ab0-114">The address of a string pointer that receives the default view name.</span></span> <span data-ttu-id="d6ab0-115">La mémoire pour la chaîne est allouée avec [**SHStrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span><span class="sxs-lookup"><span data-stu-id="d6ab0-115">The memory for the string is allocated with [**SHStrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6ab0-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d6ab0-116">Return value</span></span>

<span data-ttu-id="d6ab0-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d6ab0-117">Type: **HRESULT**</span></span>

<span data-ttu-id="d6ab0-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d6ab0-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6ab0-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d6ab0-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6ab0-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d6ab0-120">Requirements</span></span>



| <span data-ttu-id="d6ab0-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6ab0-121">Requirement</span></span> | <span data-ttu-id="d6ab0-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6ab0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6ab0-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6ab0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d6ab0-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6ab0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d6ab0-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6ab0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d6ab0-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6ab0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d6ab0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d6ab0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6ab0-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6ab0-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




