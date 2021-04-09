---
title: DsRestoreEnd, fonction (ntdsbcli. h)
description: Appelé pour terminer une opération de restauration.
ms.assetid: 2c3b9aba-3e92-4e5b-afff-3ed9bf64832b
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsRestoreEnd
topic_type:
- apiref
api_name:
- DsRestoreEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabbe216875c2fe934f3c87e32688cd17bc8992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032767"
---
# <a name="dsrestoreend-function"></a><span data-ttu-id="0075d-104">DsRestoreEnd fonction)</span><span class="sxs-lookup"><span data-stu-id="0075d-104">DsRestoreEnd function</span></span>

<span data-ttu-id="0075d-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="0075d-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0075d-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0075d-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="0075d-107">Utilisez à la place [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="0075d-107">Use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="0075d-108">La fonction **DsRestoreEnd** est appelée pour terminer une opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="0075d-108">The **DsRestoreEnd** function is called to terminate a restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0075d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0075d-109">Syntax</span></span>


```C++
HRESULT DsRestoreEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="0075d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0075d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0075d-111">*Hbc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0075d-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0075d-112">Contient le descripteur de contexte de restauration obtenu avec la fonction [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="0075d-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0075d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0075d-113">Return value</span></span>

<span data-ttu-id="0075d-114">Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0075d-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="0075d-115">La liste suivante répertorie les codes d’erreur possibles.</span><span class="sxs-lookup"><span data-stu-id="0075d-115">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="0075d-116">**paramètre d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="0075d-116">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="0075d-117">*Hbc* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0075d-117">*hbc* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0075d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="0075d-118">Remarks</span></span>

<span data-ttu-id="0075d-119">La fonction **DsRestoreEnd** ferme les handles de liaison en attente et effectue une opération de nettoyage après une tentative de restauration.</span><span class="sxs-lookup"><span data-stu-id="0075d-119">The **DsRestoreEnd** function closes outstanding binding handles and performs a cleanup operation after a restore attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="0075d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0075d-120">Requirements</span></span>



| <span data-ttu-id="0075d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0075d-121">Requirement</span></span> | <span data-ttu-id="0075d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0075d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0075d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0075d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0075d-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0075d-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0075d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0075d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0075d-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0075d-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0075d-127">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0075d-127">End of client support</span></span><br/>    | <span data-ttu-id="0075d-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0075d-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0075d-129">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="0075d-129">End of server support</span></span><br/>    | <span data-ttu-id="0075d-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0075d-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0075d-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="0075d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0075d-132"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="0075d-132"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="0075d-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0075d-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="0075d-134"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0075d-134"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="0075d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0075d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0075d-136"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0075d-136"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0075d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0075d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0075d-138">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="0075d-138">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="0075d-139">Restauration d’un serveur Active Directory</span><span class="sxs-lookup"><span data-stu-id="0075d-139">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="0075d-140">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="0075d-140">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

