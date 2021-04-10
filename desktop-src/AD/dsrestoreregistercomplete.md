---
title: DsRestoreRegisterComplete, fonction (ntdsbcli. h)
description: Appelé pour déverrouiller un serveur Active Directory une fois l’opération de restauration terminée.
ms.assetid: 781cd2ec-d2e2-4f3a-903d-feda4b871de5
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsRestoreRegisterComplete
topic_type:
- apiref
api_name:
- DsRestoreRegisterComplete
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5e5e01b29281860dff59fbcd08a3b48ec66c4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032978"
---
# <a name="dsrestoreregistercomplete-function"></a><span data-ttu-id="17579-104">DsRestoreRegisterComplete fonction)</span><span class="sxs-lookup"><span data-stu-id="17579-104">DsRestoreRegisterComplete function</span></span>

<span data-ttu-id="17579-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="17579-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="17579-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="17579-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="17579-107">Utilisez à la place [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="17579-107">Use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="17579-108">La fonction **DsRestoreRegisterComplete** est appelée pour déverrouiller un serveur Active Directory une fois l’opération de restauration terminée.</span><span class="sxs-lookup"><span data-stu-id="17579-108">The **DsRestoreRegisterComplete** function is called to unlock an Active Directory server after a restore operation is complete.</span></span> <span data-ttu-id="17579-109">Cette fonction est équivalente à la fonction [**DsRestoreRegister**](dsrestoreregister.md) .</span><span class="sxs-lookup"><span data-stu-id="17579-109">This function is counterpart to the [**DsRestoreRegister**](dsrestoreregister.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="17579-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17579-110">Syntax</span></span>


```C++
HRESULT DsRestoreRegisterComplete(
  _In_ HBC     hbc,
  _In_ HRESULT hrRestoreState
);
```



## <a name="parameters"></a><span data-ttu-id="17579-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17579-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17579-112">*Hbc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="17579-112">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17579-113">Contient le descripteur de contexte de restauration obtenu avec la fonction [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="17579-113">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="17579-114">*hrRestoreState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="17579-114">*hrRestoreState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17579-115">Contient l’état final de l’opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="17579-115">Contains the final status of the restore operation.</span></span> <span data-ttu-id="17579-116">Ce paramètre doit contenir **S \_ OK** si l’opération de restauration a réussi ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="17579-116">This parameter should contain **S\_OK** if the restore operation was successful or an error code otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17579-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17579-117">Return value</span></span>

<span data-ttu-id="17579-118">Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="17579-118">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="17579-119">La liste suivante répertorie les codes d’erreur possibles.</span><span class="sxs-lookup"><span data-stu-id="17579-119">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="17579-120">**ERREUR d' \_ accès \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="17579-120">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="17579-121">L’appelant ne dispose pas des privilèges d’accès appropriés pour appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="17579-121">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="17579-122">La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour définir les informations d’identification à utiliser pour les fonctions de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="17579-122">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17579-123">Notes</span><span class="sxs-lookup"><span data-stu-id="17579-123">Remarks</span></span>

<span data-ttu-id="17579-124">Avant de redémarrer le contrôleur de domaine, appelez cette fonction pour indiquer l’état de l’opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="17579-124">Before you restart the domain controller, call this function to provide the status of the restore operation.</span></span> <span data-ttu-id="17579-125">Si l’État échoue, le service d’annuaire ne démarre pas tant qu’une base de données valide n’a pas été restaurée.</span><span class="sxs-lookup"><span data-stu-id="17579-125">If the status is not successful, the directory service will not start until a valid database has been restored.</span></span> <span data-ttu-id="17579-126">Cette fonction termine l’opération de restauration et permet à Active Directory Domain Services de démarrer.</span><span class="sxs-lookup"><span data-stu-id="17579-126">This function completes the restore operation and allows Active Directory Domain Services to start.</span></span>

## <a name="requirements"></a><span data-ttu-id="17579-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17579-127">Requirements</span></span>



| <span data-ttu-id="17579-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17579-128">Requirement</span></span> | <span data-ttu-id="17579-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="17579-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17579-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17579-130">Minimum supported client</span></span><br/> | <span data-ttu-id="17579-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="17579-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="17579-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17579-132">Minimum supported server</span></span><br/> | <span data-ttu-id="17579-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="17579-133">None supported</span></span><br/>                                                               |
| <span data-ttu-id="17579-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="17579-134">End of client support</span></span><br/>    | <span data-ttu-id="17579-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="17579-135">None supported</span></span><br/>                                                               |
| <span data-ttu-id="17579-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="17579-136">End of server support</span></span><br/>    | <span data-ttu-id="17579-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="17579-137">None supported</span></span><br/>                                                               |
| <span data-ttu-id="17579-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="17579-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="17579-139"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="17579-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="17579-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17579-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="17579-141"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17579-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="17579-142">DLL</span><span class="sxs-lookup"><span data-stu-id="17579-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17579-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17579-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17579-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17579-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17579-145">**DsRestoreRegister**</span><span class="sxs-lookup"><span data-stu-id="17579-145">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="17579-146">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="17579-146">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="17579-147">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="17579-147">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="17579-148">Restauration d’un serveur Active Directory</span><span class="sxs-lookup"><span data-stu-id="17579-148">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="17579-149">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="17579-149">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

