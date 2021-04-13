---
title: DsBackupPrepare, fonction (ntdsbcli. h)
description: Prépare le répertoire sur le serveur spécifié pour la sauvegarde en ligne et retourne un handle de contexte de sauvegarde utilisé dans les appels ultérieurs à d’autres fonctions de sauvegarde.
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupPrepare
topic_type:
- apiref
api_name:
- DsBackupPrepare
- DsBackupPrepareA
- DsBackupPrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa561a7e41164ece68fb18fd882a8b05d6357cec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465586"
---
# <a name="dsbackupprepare-function"></a><span data-ttu-id="49cf8-104">DsBackupPrepare fonction)</span><span class="sxs-lookup"><span data-stu-id="49cf8-104">DsBackupPrepare function</span></span>

<span data-ttu-id="49cf8-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="49cf8-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="49cf8-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="49cf8-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="49cf8-107">À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="49cf8-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="49cf8-108">La fonction **DsBackupPrepare** prépare le répertoire sur le serveur spécifié pour la sauvegarde en ligne et retourne un handle de contexte de sauvegarde utilisé dans les appels ultérieurs à d’autres fonctions de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="49cf8-108">The **DsBackupPrepare** function prepares the directory on the specified server for the online backup and returns a backup context handle used in subsequent calls to other backup functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="49cf8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49cf8-109">Syntax</span></span>


```C++
HRESULT DsBackupPrepare(
  _In_  LPCTSTR szBackupServer,
  _In_  ULONG   grbit,
  _In_  ULONG   btBackupType,
  _Out_ PVOID   *ppvExpiryToken,
  _Out_ LPDWORD pcbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a><span data-ttu-id="49cf8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49cf8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49cf8-111">*szBackupServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49cf8-111">*szBackupServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49cf8-112">Pointeur vers une chaîne se terminant par un caractère null qui contient le nom du serveur à sauvegarder.</span><span class="sxs-lookup"><span data-stu-id="49cf8-112">Pointer to a null-terminated string that contains the name of the server to backup.</span></span> <span data-ttu-id="49cf8-113">Les barres obliques inverses précédentes sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="49cf8-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="49cf8-114">Le serveur doit être le même que celui à partir duquel cette fonction est appelée.</span><span class="sxs-lookup"><span data-stu-id="49cf8-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="49cf8-115">Le nom du serveur ne peut pas contenir de caractère de soulignement ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="49cf8-115">The server name cannot contain an underscore (\_) character.</span></span> <span data-ttu-id="49cf8-116">Exemple de nom de serveur \\ \\ : « serveur1 ».</span><span class="sxs-lookup"><span data-stu-id="49cf8-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="49cf8-117">*Grbit* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49cf8-117">*grbit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49cf8-118">Détermine si les fichiers journaux seront sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="49cf8-118">Determines if the log files will be backed up.</span></span> <span data-ttu-id="49cf8-119">Cette valeur doit toujours être 0, car les sauvegardes incrémentielles ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="49cf8-119">This value should always be 0 because incremental backups are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="49cf8-120">*btBackupType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49cf8-120">*btBackupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49cf8-121">Spécifie le type de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="49cf8-121">Specifies the type of backup.</span></span> <span data-ttu-id="49cf8-122">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="49cf8-122">This can be one of the following values.</span></span>

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span data-ttu-id="49cf8-123"><span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**TYPE de sauvegarde \_ \_ complet**</span><span class="sxs-lookup"><span data-stu-id="49cf8-123"><span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**BACKUP\_TYPE\_FULL**</span></span>


</dt> <dd>

<span data-ttu-id="49cf8-124">Spécifie une sauvegarde complète.</span><span class="sxs-lookup"><span data-stu-id="49cf8-124">Specifies a full backup.</span></span> <span data-ttu-id="49cf8-125">Le répertoire complet (DIT, les fichiers journaux et les fichiers de mise à jour) sont sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="49cf8-125">The complete directory (DIT, log files, and update files) are backed up.</span></span> <span data-ttu-id="49cf8-126">Toutes les données sont sauvegardées et les fichiers journaux des transactions sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="49cf8-126">All data is backed up and transaction log files are truncated.</span></span> <span data-ttu-id="49cf8-127">Seules les sauvegardes complètes sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="49cf8-127">Only full backups are supported.</span></span>

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span data-ttu-id="49cf8-128"><span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**TYPE de sauvegarde \_ \_ journaux \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="49cf8-128"><span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**BACKUP\_TYPE\_LOGS\_ONLY**</span></span>


</dt> <dd>

<span data-ttu-id="49cf8-129">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="49cf8-129">This value is not supported.</span></span> <span data-ttu-id="49cf8-130">Spécifie que seuls les journaux de base de données, et non la base de données elle-même, seront sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="49cf8-130">Specifies that only the database logs, and not the database itself, will be backed up.</span></span> <span data-ttu-id="49cf8-131">Cette opération est normalement utilisée lors d’une sauvegarde différentielle ou incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="49cf8-131">This is normally used when performing a differential or incremental backup.</span></span>

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span data-ttu-id="49cf8-132"><span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**TYPE de sauvegarde \_ \_ incrémentiel**</span><span class="sxs-lookup"><span data-stu-id="49cf8-132"><span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**BACKUP\_TYPE\_INCREMENTAL**</span></span>


</dt> <dd>

<span data-ttu-id="49cf8-133">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="49cf8-133">This value is not supported.</span></span> <span data-ttu-id="49cf8-134">**DsBackupPrepare** retourne **un \_ \_ paramètre d’erreur non valide**.</span><span class="sxs-lookup"><span data-stu-id="49cf8-134">**DsBackupPrepare** returns **ERROR\_INVALID\_PARAMETER**.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="49cf8-135">*ppvExpiryToken* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="49cf8-135">*ppvExpiryToken* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49cf8-136">Pointeur vers une valeur **pVoid** qui reçoit un pointeur vers un jeton d’expiration associé à cette sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="49cf8-136">Pointer to a **PVOID** value that receives a pointer to an expiry token associated with this backup.</span></span> <span data-ttu-id="49cf8-137">*pcbExpiryTokenSize* reçoit la taille, en octets, de ces données.</span><span class="sxs-lookup"><span data-stu-id="49cf8-137">*pcbExpiryTokenSize* receives the size, in bytes, of this data.</span></span> <span data-ttu-id="49cf8-138">L’appelant doit enregistrer le contenu de ce jeton avec la sauvegarde, car le jeton doit être transmis à [**DsRestorePrepare**](dsrestoreprepare.md) lors de la tentative de restauration des données.</span><span class="sxs-lookup"><span data-stu-id="49cf8-138">The caller must save the contents of this token with the backup because the token must be passed to [**DsRestorePrepare**](dsrestoreprepare.md) when attempting to restore data.</span></span> <span data-ttu-id="49cf8-139">Une fois que le jeton a été stocké et qu’il n’est plus nécessaire, l’appelant doit libérer la mémoire allouée à l’aide de [**DsBackupFree**](dsbackupfree.md).</span><span class="sxs-lookup"><span data-stu-id="49cf8-139">After the token has been stored and is no longer required, the caller should free the allocated memory using [**DsBackupFree**](dsbackupfree.md).</span></span>

</dd> <dt>

<span data-ttu-id="49cf8-140">*pcbExpiryTokenSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="49cf8-140">*pcbExpiryTokenSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49cf8-141">Pointeur vers une valeur **DWORD** qui reçoit la taille, en octets, du jeton dans *ppvExpiryToken*.</span><span class="sxs-lookup"><span data-stu-id="49cf8-141">Pointer to a **DWORD** value that receives the size, in bytes, of the token in *ppvExpiryToken*.</span></span>

</dd> <dt>

<span data-ttu-id="49cf8-142">*phbC* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="49cf8-142">*phbc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49cf8-143">Pointeur vers une valeur **Hbc** qui reçoit le handle de la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="49cf8-143">Pointer to an **HBC** value that receives the handle for the backup.</span></span> <span data-ttu-id="49cf8-144">Ce descripteur est utilisé lors de l’appel d’autres fonctions de sauvegarde du service d’annuaire, telles que [**DsBackupOpenFile**](dsbackupopenfile.md) et [**DsBackupEnd**](dsbackupend.md).</span><span class="sxs-lookup"><span data-stu-id="49cf8-144">This handle is used when calling other Directory Service backup functions, such as [**DsBackupOpenFile**](dsbackupopenfile.md) and [**DsBackupEnd**](dsbackupend.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49cf8-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49cf8-145">Return value</span></span>

<span data-ttu-id="49cf8-146">Retourne **S \_ OK** si la fonction réussit ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="49cf8-146">Returns **S\_OK** if the function is successful or an error code otherwise.</span></span> <span data-ttu-id="49cf8-147">La liste suivante répertorie les autres codes d’erreur possibles.</span><span class="sxs-lookup"><span data-stu-id="49cf8-147">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="49cf8-148">**ERREUR d' \_ accès \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="49cf8-148">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="49cf8-149">L’appelant ne dispose pas des privilèges d’accès appropriés pour appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="49cf8-149">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="49cf8-150">La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour définir les informations d’identification à utiliser pour les fonctions de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="49cf8-150">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="49cf8-151">**paramètre d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="49cf8-151">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="49cf8-152">*szBackupServer* ou *phbcBackupContext* ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="49cf8-152">*szBackupServer* or *phbcBackupContext* are not valid.</span></span>

</dd> <dt>

<span data-ttu-id="49cf8-153">**ERREUR \_ de \_ mémoire insuffisante \_**</span><span class="sxs-lookup"><span data-stu-id="49cf8-153">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="49cf8-154">Un échec d’allocation de mémoire s’est produit.</span><span class="sxs-lookup"><span data-stu-id="49cf8-154">A memory allocation failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="49cf8-155">**hrCouldNotConnect**</span><span class="sxs-lookup"><span data-stu-id="49cf8-155">**hrCouldNotConnect**</span></span>
</dt> <dd>

<span data-ttu-id="49cf8-156">Le serveur dans *szBackupServer* est introuvable, n’est pas un contrôleur de domaine ou *szBackupServer* n’est pas mis en forme correctement.</span><span class="sxs-lookup"><span data-stu-id="49cf8-156">The server in *szBackupServer* could not be found, is not a domain controller or *szBackupServer* is not formatted correctly.</span></span> <span data-ttu-id="49cf8-157">Cette valeur est définie dans ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="49cf8-157">This value is defined in ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="49cf8-158">**hrInvalidParam**</span><span class="sxs-lookup"><span data-stu-id="49cf8-158">**hrInvalidParam**</span></span>
</dt> <dd>

<span data-ttu-id="49cf8-159">*ppvExpiryToken* et/ou *pcbExpiryTokenSize* ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="49cf8-159">*ppvExpiryToken* and/or *pcbExpiryTokenSize* are invalid.</span></span> <span data-ttu-id="49cf8-160">Cette valeur est définie dans ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="49cf8-160">This value is defined in Ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="49cf8-161">**\_liaison RPC S \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="49cf8-161">**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd>

<span data-ttu-id="49cf8-162">La fonction est appelée à distance ou le serveur dans *szServerName* n’est pas un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="49cf8-162">The function is called remotely or the server in *szServerName* is not a domain controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49cf8-163">Notes</span><span class="sxs-lookup"><span data-stu-id="49cf8-163">Remarks</span></span>

<span data-ttu-id="49cf8-164">Cette fonction requiert que l’appelant dispose du privilège de **\_ \_ nom de sauvegarde se** .</span><span class="sxs-lookup"><span data-stu-id="49cf8-164">This function requires that the caller has the **SE\_BACKUP\_NAME** privilege.</span></span> <span data-ttu-id="49cf8-165">La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour modifier le contexte de sécurité sous lequel cette fonction est appelée.</span><span class="sxs-lookup"><span data-stu-id="49cf8-165">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to change the security context under which this function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="49cf8-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49cf8-166">Requirements</span></span>



| <span data-ttu-id="49cf8-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49cf8-167">Requirement</span></span> | <span data-ttu-id="49cf8-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="49cf8-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49cf8-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49cf8-169">Minimum supported client</span></span><br/> | <span data-ttu-id="49cf8-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49cf8-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49cf8-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49cf8-171">Minimum supported server</span></span><br/> | <span data-ttu-id="49cf8-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49cf8-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49cf8-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="49cf8-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="49cf8-174"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="49cf8-174"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="49cf8-175">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="49cf8-175">Library</span></span><br/>                  | <dl> <span data-ttu-id="49cf8-176"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49cf8-176"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="49cf8-177">DLL</span><span class="sxs-lookup"><span data-stu-id="49cf8-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49cf8-178"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49cf8-178"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="49cf8-179">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="49cf8-179">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="49cf8-180">**DsBackupPrepareW** (Unicode) et **DsBackupPrepareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="49cf8-180">**DsBackupPrepareW** (Unicode) and **DsBackupPrepareA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="49cf8-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49cf8-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49cf8-182">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="49cf8-182">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="49cf8-183">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="49cf8-183">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="49cf8-184">**DsBackupOpenFile**</span><span class="sxs-lookup"><span data-stu-id="49cf8-184">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="49cf8-185">**DsBackupEnd**</span><span class="sxs-lookup"><span data-stu-id="49cf8-185">**DsBackupEnd**</span></span>](dsbackupend.md)
</dt> <dt>

[<span data-ttu-id="49cf8-186">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="49cf8-186">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="49cf8-187">Sauvegarde d’un serveur de Active Directory</span><span class="sxs-lookup"><span data-stu-id="49cf8-187">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="49cf8-188">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="49cf8-188">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

