---
title: DsRestoreGetDatabaseLocations, fonction (ntdsbcli. h)
description: Obtient les emplacements où les fichiers de sauvegarde doivent être copiés au cours d’une opération de restauration.
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsRestoreGetDatabaseLocations
topic_type:
- apiref
api_name:
- DsRestoreGetDatabaseLocations
- DsRestoreGetDatabaseLocationsA
- DsRestoreGetDatabaseLocationsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bcebb9f3822332269e1db09f3246c128e4ad1f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843905"
---
# <a name="dsrestoregetdatabaselocations-function"></a><span data-ttu-id="706a8-104">DsRestoreGetDatabaseLocations fonction)</span><span class="sxs-lookup"><span data-stu-id="706a8-104">DsRestoreGetDatabaseLocations function</span></span>

<span data-ttu-id="706a8-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="706a8-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="706a8-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="706a8-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="706a8-107">À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="706a8-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="706a8-108">La fonction **DsRestoreGetDatabaseLocations** obtient les emplacements où les fichiers de sauvegarde doivent être copiés au cours d’une opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="706a8-108">The **DsRestoreGetDatabaseLocations** function obtains the locations where backup files should be copied during a restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="706a8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="706a8-109">Syntax</span></span>


```C++
HRESULT DsRestoreGetDatabaseLocations(
  _In_  HBC     hbc,
  _Out_ LPWSTR  *pszDatabaseLocationList,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="706a8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="706a8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="706a8-111">*Hbc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="706a8-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="706a8-112">Contient le descripteur de contexte de restauration obtenu avec la fonction [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="706a8-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="706a8-113">*pszDatabaseLocationList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="706a8-113">*pszDatabaseLocationList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="706a8-114">Pointeur vers un pointeur de chaîne qui reçoit la liste d’emplacements de base de données sous forme de chemins d’accès UNC.</span><span class="sxs-lookup"><span data-stu-id="706a8-114">Pointer to a string pointer that receives the list of database locations as UNC paths.</span></span> <span data-ttu-id="706a8-115">Cette liste reçoit une liste double terminée par un caractère null de chaînes uniques se terminant par null.</span><span class="sxs-lookup"><span data-stu-id="706a8-115">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="706a8-116">Cette mémoire tampon est allouée par la fonction **DsRestoreGetDatabaseLocations** et doit être libérée lorsqu’elle n’est plus nécessaire en appelant la fonction [**DsBackupFree**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="706a8-116">This buffer is allocated by the **DsRestoreGetDatabaseLocations** function and must be freed when it is no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="706a8-117">Le premier caractère de chaque nom de fichier contient une des [**constantes BFT**](bft-constants.md) qui identifient le type de nom.</span><span class="sxs-lookup"><span data-stu-id="706a8-117">The first character of each of the file names contains one of the [**BFT Constants**](bft-constants.md) that identifies the name type.</span></span> <span data-ttu-id="706a8-118">La fonction **DsRestoreGetDatabaseLocations** fournit uniquement les types de nom suivants.</span><span class="sxs-lookup"><span data-stu-id="706a8-118">The **DsRestoreGetDatabaseLocations** function only supplies the following name types.</span></span>

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span data-ttu-id="706a8-119"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_ \_ base de données BFT NTDS**</span><span class="sxs-lookup"><span data-stu-id="706a8-119"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>


</dt> <dd>

<span data-ttu-id="706a8-120">Le fichier de base de données NTDS doit être copié dans ce fichier.</span><span class="sxs-lookup"><span data-stu-id="706a8-120">The NTDS database file should be copied to this file.</span></span> <span data-ttu-id="706a8-121">Il s’agit du fichier qui a été identifié en tant que **\_ \_ base de données BFT NTDS** lorsque la sauvegarde a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="706a8-121">This is the file that was identified as **BFT\_NTDS\_DATABASE** when the backup was performed.</span></span>

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span data-ttu-id="706a8-122"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**\_répertoire du journal BFT \_**</span><span class="sxs-lookup"><span data-stu-id="706a8-122"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT\_LOG\_DIR**</span></span>


</dt> <dd>

<span data-ttu-id="706a8-123">Tous les fichiers journaux sont copiés dans ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="706a8-123">All log files are copied to this directory.</span></span> <span data-ttu-id="706a8-124">Les fichiers journaux ont été identifiés en tant que **\_ Journal BFT** lorsque la sauvegarde a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="706a8-124">The log files were identified as **BFT\_LOG** when the backup was performed.</span></span>

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span data-ttu-id="706a8-125"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT \_ Répertoire de point de contrôle \_**</span><span class="sxs-lookup"><span data-stu-id="706a8-125"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT\_CHECKPOINT\_DIR**</span></span>


</dt> <dd>

<span data-ttu-id="706a8-126">Tous les fichiers correctifs sont copiés dans ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="706a8-126">All patch files are copied to this directory.</span></span> <span data-ttu-id="706a8-127">Les fichiers correctifs ont été identifiés en tant que **\_ \_ fichier correctif BFT** lors de l’exécution de la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="706a8-127">The patch files were identified as **BFT\_PATCH\_FILE** when the backup was performed.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="706a8-128">*PCB* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="706a8-128">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="706a8-129">Pointeur vers une valeur **DWORD** qui reçoit la taille, en octets, de la mémoire tampon *pszDatabaseLocationList* .</span><span class="sxs-lookup"><span data-stu-id="706a8-129">Pointer to **DWORD** value that receives the size, in bytes, of the *pszDatabaseLocationList* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="706a8-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="706a8-130">Return value</span></span>

<span data-ttu-id="706a8-131">Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="706a8-131">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="706a8-132">La liste suivante répertorie les codes d’erreur possibles.</span><span class="sxs-lookup"><span data-stu-id="706a8-132">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="706a8-133">**ERREUR d' \_ accès \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="706a8-133">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="706a8-134">L’appelant ne dispose pas des privilèges d’accès appropriés pour appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="706a8-134">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="706a8-135">La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour définir les informations d’identification à utiliser pour les fonctions de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="706a8-135">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="706a8-136">**paramètre d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="706a8-136">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="706a8-137">*Hbc*, *pszDatabaseLocationList* ou *PCB* ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="706a8-137">*hbc*, *pszDatabaseLocationList*, or *pcbSize* are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="706a8-138">**ERREUR \_ de \_ mémoire insuffisante \_**</span><span class="sxs-lookup"><span data-stu-id="706a8-138">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="706a8-139">Un échec d’allocation de mémoire s’est produit.</span><span class="sxs-lookup"><span data-stu-id="706a8-139">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="706a8-140">Notes</span><span class="sxs-lookup"><span data-stu-id="706a8-140">Remarks</span></span>

<span data-ttu-id="706a8-141">La fonction **DsRestoreGetDatabaseLocations** peut être utilisée pour obtenir les répertoires de restauration sans avoir accès aux données sauvegardées.</span><span class="sxs-lookup"><span data-stu-id="706a8-141">The **DsRestoreGetDatabaseLocations** function can be used to obtain the restoration directories without access to the backed up data.</span></span> <span data-ttu-id="706a8-142">Pour ce faire, appelez [**DsRestorePrepare**](dsrestoreprepare.md) avec la **valeur null** pour le paramètre *pvExpiryToken* .</span><span class="sxs-lookup"><span data-stu-id="706a8-142">To do this, call [**DsRestorePrepare**](dsrestoreprepare.md) with **NULL** for the *pvExpiryToken* parameter.</span></span> <span data-ttu-id="706a8-143">**DsRestorePrepare** retourne alors un handle de contexte restreint qui peut uniquement être utilisé avec la fonction **DsRestoreGetDatabaseLocations** .</span><span class="sxs-lookup"><span data-stu-id="706a8-143">This causes **DsRestorePrepare** to return a restricted context handle which can only be used with the **DsRestoreGetDatabaseLocations** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="706a8-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="706a8-144">Requirements</span></span>



| <span data-ttu-id="706a8-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="706a8-145">Requirement</span></span> | <span data-ttu-id="706a8-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="706a8-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="706a8-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="706a8-147">Minimum supported client</span></span><br/> | <span data-ttu-id="706a8-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="706a8-148">Windows Vista</span></span><br/>                                                                              |
| <span data-ttu-id="706a8-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="706a8-149">Minimum supported server</span></span><br/> | <span data-ttu-id="706a8-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="706a8-150">Windows Server 2008</span></span><br/>                                                                        |
| <span data-ttu-id="706a8-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="706a8-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="706a8-152"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="706a8-152"><dt>Ntdsbcli.h</dt></span></span> </dl>                 |
| <span data-ttu-id="706a8-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="706a8-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="706a8-154"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="706a8-154"><dt>Ntdsbcli.lib</dt></span></span> </dl>               |
| <span data-ttu-id="706a8-155">DLL</span><span class="sxs-lookup"><span data-stu-id="706a8-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="706a8-156"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="706a8-156"><dt>Ntdsbcli.dll</dt></span></span> </dl>               |
| <span data-ttu-id="706a8-157">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="706a8-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="706a8-158">**DsRestoreGetDatabaseLocationsW** (Unicode) et **DsRestoreGetDatabaseLocationsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="706a8-158">**DsRestoreGetDatabaseLocationsW** (Unicode) and **DsRestoreGetDatabaseLocationsA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="706a8-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="706a8-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="706a8-160">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="706a8-160">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="706a8-161">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="706a8-161">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="706a8-162">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="706a8-162">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="706a8-163">Restauration d’Active Directory</span><span class="sxs-lookup"><span data-stu-id="706a8-163">Restoring Active Directory</span></span>](restoring-an-active-directory-server.md)
</dt> </dl>

 

