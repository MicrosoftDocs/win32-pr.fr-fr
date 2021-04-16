---
title: DsBackupTruncateLogs, fonction (ntdsbcli. h)
description: Tronque les journaux de sauvegarde précédemment lus.
ms.assetid: fae2e19f-08b8-410f-a735-dd4d41fc71a6
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupTruncateLogs
topic_type:
- apiref
api_name:
- DsBackupTruncateLogs
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051ced828656c6b6e5af156e2d1a69c3b741cdce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508501"
---
# <a name="dsbackuptruncatelogs-function"></a><span data-ttu-id="2e5ae-104">DsBackupTruncateLogs fonction)</span><span class="sxs-lookup"><span data-stu-id="2e5ae-104">DsBackupTruncateLogs function</span></span>

<span data-ttu-id="2e5ae-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2e5ae-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="2e5ae-107">À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="2e5ae-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="2e5ae-108">La fonction **DsBackupTruncateLogs** tronque les journaux de sauvegarde précédemment lus.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-108">The **DsBackupTruncateLogs** function truncates the previously read backup logs.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e5ae-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e5ae-109">Syntax</span></span>


```C++
HRESULT DsBackupTruncateLogs(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="2e5ae-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e5ae-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e5ae-111">*Hbc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e5ae-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e5ae-112">Contient le descripteur de contexte de sauvegarde obtenu avec la fonction [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="2e5ae-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e5ae-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e5ae-113">Return value</span></span>

<span data-ttu-id="2e5ae-114">Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="2e5ae-115">La liste suivante répertorie les autres codes d’erreur possibles.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-115">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="2e5ae-116">**ERREUR d' \_ accès \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="2e5ae-116">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="2e5ae-117">L’appelant ne dispose pas des privilèges d’accès appropriés pour appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-117">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="2e5ae-118">La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour définir les informations d’identification à utiliser pour les fonctions de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-118">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="2e5ae-119">**paramètre d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2e5ae-119">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="2e5ae-120">*Hbc* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-120">*hbc* is invalid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e5ae-121">Notes</span><span class="sxs-lookup"><span data-stu-id="2e5ae-121">Remarks</span></span>

<span data-ttu-id="2e5ae-122">Utilisez la fonction **DsBackupTruncateLogs** lorsqu’une sauvegarde complète ou incrémentielle s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-122">Use the **DsBackupTruncateLogs** function when a full or incremental backup has completed successfully.</span></span>

> [!Caution]  
> <span data-ttu-id="2e5ae-123">Si cette fonction est appelée après une sauvegarde différentielle, toutes les informations de sauvegarde incrémentielle seront perdues.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-123">If this function is called after a differential backup, all of the incremental backup information will be lost.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e5ae-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e5ae-124">Requirements</span></span>



| <span data-ttu-id="2e5ae-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e5ae-125">Requirement</span></span> | <span data-ttu-id="2e5ae-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e5ae-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e5ae-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e5ae-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2e5ae-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e5ae-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e5ae-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e5ae-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2e5ae-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e5ae-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e5ae-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e5ae-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e5ae-132"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e5ae-132"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e5ae-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2e5ae-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="2e5ae-134"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e5ae-134"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="2e5ae-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2e5ae-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e5ae-136"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e5ae-136"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e5ae-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e5ae-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e5ae-138">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="2e5ae-138">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="2e5ae-139">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="2e5ae-139">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="2e5ae-140">**DsSetCurrentBackupLog**</span><span class="sxs-lookup"><span data-stu-id="2e5ae-140">**DsSetCurrentBackupLog**</span></span>](dssetcurrentbackuplog.md)
</dt> <dt>

[<span data-ttu-id="2e5ae-141">Sauvegarde d’un serveur de Active Directory</span><span class="sxs-lookup"><span data-stu-id="2e5ae-141">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="2e5ae-142">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="2e5ae-142">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

