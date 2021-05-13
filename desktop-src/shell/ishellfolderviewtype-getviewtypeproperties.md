---
description: Obtient les propriétés de la vue.
title: 'IShellFolderViewType :: GetViewTypeProperties, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetViewTypeProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 82be6bd5-a46c-48b3-a1f0-a92b9454c35e
ms.openlocfilehash: f5c7c6b75c89711a69ac578b3d04a72362b1eac9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842700"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a><span data-ttu-id="8a13a-103">IShellFolderViewType :: GetViewTypeProperties, méthode</span><span class="sxs-lookup"><span data-stu-id="8a13a-103">IShellFolderViewType::GetViewTypeProperties method</span></span>

<span data-ttu-id="8a13a-104">Obtient les propriétés de la vue.</span><span class="sxs-lookup"><span data-stu-id="8a13a-104">Gets the properties of the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a13a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a13a-105">Syntax</span></span>


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8a13a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a13a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a13a-107">*PIDL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a13a-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a13a-108">Type : **\_ enfant PCUITEMID**</span><span class="sxs-lookup"><span data-stu-id="8a13a-108">Type: **PCUITEMID\_CHILD**</span></span>

<span data-ttu-id="8a13a-109">PIDL.</span><span class="sxs-lookup"><span data-stu-id="8a13a-109">A PIDL.</span></span>

</dd> <dt>

<span data-ttu-id="8a13a-110">*pdwFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8a13a-110">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a13a-111">Type : **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="8a13a-111">Type: **DWORD\***</span></span>

<span data-ttu-id="8a13a-112">Pointeur vers une variable entière non signée qui reçoit les propriétés de la vue, qui indiquent la marche à suivre lorsque la vue est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="8a13a-112">A pointer to an unsigned integer variable that receives the view properties, which indicate what to do when the view is selected.</span></span> <span data-ttu-id="8a13a-113">Les indicateurs peuvent être n’importe quelle combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8a13a-113">Flags may be any combination of the following values.</span></span>

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span data-ttu-id="8a13a-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG \_ NOTIFIer la \_ création** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="8a13a-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG\_NOTIFY\_CREATE** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="8a13a-115">Créer un élément d’affichage s’il n’y est pas.</span><span class="sxs-lookup"><span data-stu-id="8a13a-115">Create view item if not there.</span></span>

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span data-ttu-id="8a13a-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFIer le \_ Resort** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="8a13a-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG\_NOTIFY\_RESORT** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="8a13a-117">Réinsérez PIDL et retriez.</span><span class="sxs-lookup"><span data-stu-id="8a13a-117">Reinsert PIDL and re-sort.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a13a-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8a13a-118">Return value</span></span>

<span data-ttu-id="8a13a-119">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8a13a-119">Type: **HRESULT**</span></span>

<span data-ttu-id="8a13a-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8a13a-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8a13a-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8a13a-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a13a-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8a13a-122">Requirements</span></span>



| <span data-ttu-id="8a13a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a13a-123">Requirement</span></span> | <span data-ttu-id="8a13a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a13a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a13a-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a13a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8a13a-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a13a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8a13a-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a13a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8a13a-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a13a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8a13a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8a13a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a13a-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a13a-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




