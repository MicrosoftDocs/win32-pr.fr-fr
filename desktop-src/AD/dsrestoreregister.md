---
title: DsRestoreRegister, fonction (ntdsbcli. h)
description: Inscrit une opération de restauration.
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsRestoreRegister
topic_type:
- apiref
api_name:
- DsRestoreRegister
- DsRestoreRegisterA
- DsRestoreRegisterW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 610d49c73ade9bab47c95e90af73bac606f4bd23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032979"
---
# <a name="dsrestoreregister-function"></a><span data-ttu-id="5ad4f-104">DsRestoreRegister fonction)</span><span class="sxs-lookup"><span data-stu-id="5ad4f-104">DsRestoreRegister function</span></span>

<span data-ttu-id="5ad4f-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5ad4f-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="5ad4f-107">À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="5ad4f-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="5ad4f-108">La fonction **DsRestoreRegister** enregistre une opération de restauration. Cette fonction interverrouille toutes les opérations de restauration ultérieures et empêche le démarrage de la cible de restauration jusqu’à ce que la fonction [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) soit appelée.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-108">The **DsRestoreRegister** function registers a restore operation.This function interlocks all subsequent restore operations and prevents the restore target from starting until the [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) function is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ad4f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ad4f-109">Syntax</span></span>


```C++
HRESULT DsRestoreRegister(
  _In_ HBC        hbc,
  _In_ LPCTSTR    szCheckPointFilePath,
  _In_ LPCTSTR    szLogPath,
  _In_ EDB_RSTMAP rgrstmap[],
  _In_ LONG       crstmap,
  _In_ LPCTSTR    szBackupLogPath,
  _In_ ULONG      genLow,
  _In_ ULONG      genHigh
);
```



## <a name="parameters"></a><span data-ttu-id="5ad4f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ad4f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ad4f-111">*Hbc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ad4f-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad4f-112">Contient le descripteur de contexte de restauration obtenu avec la fonction [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="5ad4f-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="5ad4f-113">*szCheckPointFilePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ad4f-113">*szCheckPointFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad4f-114">Pointeur vers une chaîne se terminant par un caractère null qui contient le chemin d’accès au fichier de point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-114">Pointer to a null-terminated string that contains the path to the checkpoint file.</span></span> <span data-ttu-id="5ad4f-115">Ce chemin d’accès est fourni par la fonction [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) et a une valeur **BFT** de **BFT \_ Checkpoint \_ dir**.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-115">This path is provided by the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function and has a **BFT** value of **BFT\_CHECKPOINT\_DIR**.</span></span> <span data-ttu-id="5ad4f-116">En général, il est identique au chemin d’accès de la base de données système.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-116">Typically this is the same as the system database path.</span></span> <span data-ttu-id="5ad4f-117">Ce chemin d’accès est requis pour la fonction de restauration de sauvegarde appropriée.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-117">This path is required for proper backup restore function.</span></span> <span data-ttu-id="5ad4f-118">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-118">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="5ad4f-119">Le passage de **null** dans ce paramètre entraîne une erreur pendant le processus de restauration.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-119">Passing **NULL** in this parameter will cause an error during the restore process.</span></span>

</dd> <dt>

<span data-ttu-id="5ad4f-120">*szLogPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ad4f-120">*szLogPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad4f-121">Pointeur vers une chaîne se terminant par un caractère null qui contient le chemin d’accès où les fichiers journaux seront restaurés.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-121">Pointer to a null-terminated string that contains the path where the log files will be restored.</span></span> <span data-ttu-id="5ad4f-122">Ce chemin d’accès est fourni par la fonction [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) et a la valeur **BFT** **BFT \_ log \_ dir**.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-122">This path is provided by the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function and has a **BFT** value of **BFT\_LOG\_DIR**.</span></span> <span data-ttu-id="5ad4f-123">Si le chemin d’accès pointe vers un répertoire vide, de nouveaux fichiers journaux y sont créés.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-123">If the path points to an empty directory, new log files are created there.</span></span> <span data-ttu-id="5ad4f-124">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5ad4f-125">*rgrstmap* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ad4f-125">*rgrstmap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad4f-126">Tableau de structures [**\_ RSTMAP edb**](edb-rstmap.md) qui contient les chemins d’accès anciens et nouveaux pour chaque base de données.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-126">An array of [**EDB\_RSTMAP**](edb-rstmap.md) structures that contains the old and new paths for each database.</span></span> <span data-ttu-id="5ad4f-127">Il existe une structure pour chaque base de données.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-127">There is one structure for each database.</span></span> <span data-ttu-id="5ad4f-128">Pour le répertoire, il existe une structure pour la base de données système et une autre structure pour la base de données d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-128">For the directory, there is a structure for the system database and another structure for the directory database.</span></span> <span data-ttu-id="5ad4f-129">L’ordre des éléments dans le tableau n’a pas d’importance.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-129">The order of the elements in the array does not matter.</span></span> <span data-ttu-id="5ad4f-130">Le paramètre *crstmap* contient le nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-130">The *crstmap* parameter contains the number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="5ad4f-131">*crstmap* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ad4f-131">*crstmap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad4f-132">Contient le nombre d’éléments dans le tableau *rgrstmap* .</span><span class="sxs-lookup"><span data-stu-id="5ad4f-132">Contains the number of elements in the *rgrstmap* array.</span></span>

</dd> <dt>

<span data-ttu-id="5ad4f-133">*szBackupLogPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ad4f-133">*szBackupLogPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad4f-134">Pointeur vers une chaîne se terminant par un caractère null qui contient le chemin d’accès de l’emplacement où les fichiers journaux sauvegardés résident actuellement.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-134">Pointer to a null-terminated string that contains the path where the backed up log files currently reside.</span></span> <span data-ttu-id="5ad4f-135">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-135">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5ad4f-136">*genLow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ad4f-136">*genLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad4f-137">Contient le numéro de journal le plus bas à restaurer dans cette session de restauration.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-137">Contains the lowest log number to restore in this restore session.</span></span> <span data-ttu-id="5ad4f-138">Il s’agit d’un nombre hexadécimal compris entre 0x00000 et 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-138">This is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="5ad4f-139">*genHigh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ad4f-139">*genHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad4f-140">Contient le numéro de journal le plus élevé à restaurer dans cette session de restauration.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-140">Contains the highest log number to restore in this restore session.</span></span> <span data-ttu-id="5ad4f-141">Il s’agit d’un nombre hexadécimal compris entre 0x00000 et 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-141">This is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ad4f-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ad4f-142">Return value</span></span>

<span data-ttu-id="5ad4f-143">Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-143">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="5ad4f-144">La liste suivante répertorie les codes d’erreur possibles.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-144">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="5ad4f-145">**ERREUR d' \_ accès \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="5ad4f-145">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="5ad4f-146">L’appelant ne dispose pas des privilèges d’accès appropriés pour appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-146">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="5ad4f-147">La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour définir les informations d’identification à utiliser pour les fonctions de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-147">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="5ad4f-148">**paramètre d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="5ad4f-148">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="5ad4f-149">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-149">One or more parameters are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="5ad4f-150">**hrMissingExpiryToken**</span><span class="sxs-lookup"><span data-stu-id="5ad4f-150">**hrMissingExpiryToken**</span></span>
</dt> <dd>

<span data-ttu-id="5ad4f-151">Le jeton d’expiration fourni à [**DsRestorePrepare**](dsrestoreprepare.md) n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-151">The expiry token supplied to [**DsRestorePrepare**](dsrestoreprepare.md) was invalid.</span></span> <span data-ttu-id="5ad4f-152">Cette valeur est définie dans ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-152">This value is defined in Ntdsbmsg.h.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ad4f-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ad4f-153">Requirements</span></span>



| <span data-ttu-id="5ad4f-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ad4f-154">Requirement</span></span> | <span data-ttu-id="5ad4f-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ad4f-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad4f-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ad4f-156">Minimum supported client</span></span><br/> | <span data-ttu-id="5ad4f-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ad4f-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ad4f-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ad4f-158">Minimum supported server</span></span><br/> | <span data-ttu-id="5ad4f-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ad4f-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ad4f-160">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ad4f-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ad4f-161"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ad4f-161"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ad4f-162">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5ad4f-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ad4f-163"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ad4f-163"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="5ad4f-164">DLL</span><span class="sxs-lookup"><span data-stu-id="5ad4f-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ad4f-165"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ad4f-165"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="5ad4f-166">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="5ad4f-166">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5ad4f-167">**DsRestoreRegisterW** (Unicode) et **DsRestoreRegisterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5ad4f-167">**DsRestoreRegisterW** (Unicode) and **DsRestoreRegisterA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="5ad4f-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ad4f-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad4f-169">**DsRestoreRegisterComplete**</span><span class="sxs-lookup"><span data-stu-id="5ad4f-169">**DsRestoreRegisterComplete**</span></span>](dsrestoreregistercomplete.md)
</dt> <dt>

[<span data-ttu-id="5ad4f-170">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="5ad4f-170">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="5ad4f-171">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="5ad4f-171">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="5ad4f-172">**DsRestoreEnd**</span><span class="sxs-lookup"><span data-stu-id="5ad4f-172">**DsRestoreEnd**</span></span>](dsrestoreend.md)
</dt> <dt>

[<span data-ttu-id="5ad4f-173">**\_RSTMAP edb**</span><span class="sxs-lookup"><span data-stu-id="5ad4f-173">**EDB\_RSTMAP**</span></span>](edb-rstmap.md)
</dt> <dt>

[<span data-ttu-id="5ad4f-174">Restauration d’Active Directory</span><span class="sxs-lookup"><span data-stu-id="5ad4f-174">Restoring Active Directory</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="5ad4f-175">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="5ad4f-175">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

