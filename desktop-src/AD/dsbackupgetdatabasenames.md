---
title: DsBackupGetDatabaseNames, fonction (ntdsbcli. h)
description: Obtient la liste des fichiers de base de données à sauvegarder pour le contexte de sauvegarde donné.
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupGetDatabaseNames
topic_type:
- apiref
api_name:
- DsBackupGetDatabaseNames
- DsBackupGetDatabaseNamesA
- DsBackupGetDatabaseNamesW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6643b17a85727f6e0df4e8deea9609f73afd1e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465587"
---
# <a name="dsbackupgetdatabasenames-function"></a><span data-ttu-id="e5fdf-104">DsBackupGetDatabaseNames fonction)</span><span class="sxs-lookup"><span data-stu-id="e5fdf-104">DsBackupGetDatabaseNames function</span></span>

<span data-ttu-id="e5fdf-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e5fdf-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e5fdf-107">À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="e5fdf-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="e5fdf-108">La fonction **DsBackupGetDatabaseNames** obtient la liste des fichiers de base de données à sauvegarder pour le contexte de sauvegarde donné.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-108">The **DsBackupGetDatabaseNames** function obtains the list of database files to be backed up for the given backup context.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5fdf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5fdf-109">Syntax</span></span>


```C++
HRESULT DsBackupGetDatabaseNames(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszAttachmentInfo,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="e5fdf-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5fdf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5fdf-111">*Hbc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5fdf-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5fdf-112">Contient le descripteur de contexte de sauvegarde obtenu avec la fonction [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="e5fdf-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e5fdf-113">*pszAttachmentInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e5fdf-113">*pszAttachmentInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5fdf-114">Pointeur vers un pointeur de chaîne qui reçoit la liste des noms de fichiers de base de données sous forme de chemins d’accès UNC.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-114">Pointer to a string pointer that receives the list of database file names as UNC paths.</span></span> <span data-ttu-id="e5fdf-115">Cette valeur doit être initialisée à la valeur **null** avant d’appeler **DsBackupGetDatabaseNames**.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-115">This value must be initialized to **NULL** prior to calling **DsBackupGetDatabaseNames**.</span></span>

<span data-ttu-id="e5fdf-116">Cette liste reçoit une liste double terminée par un caractère null de chaînes uniques se terminant par null.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-116">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="e5fdf-117">Cette mémoire tampon est allouée par la fonction **DsBackupGetDatabaseNames** et doit être libérée lorsqu’elle n’est plus nécessaire en appelant la fonction [**DsBackupFree**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="e5fdf-117">This buffer is allocated by the **DsBackupGetDatabaseNames** function and must be freed when it is no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="e5fdf-118">Le premier caractère de chaque nom de fichier contient une des [**constantes BFT**](bft-constants.md) qui identifient le type de nom.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-118">The first character of each file name contains one of the [**BFT Constants**](bft-constants.md) that identifies the type of name.</span></span> <span data-ttu-id="e5fdf-119">La fonction [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) fournit uniquement les types de noms suivants.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-119">The [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function only supplies the following types of names.</span></span>

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span data-ttu-id="e5fdf-120"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_ \_ base de données BFT NTDS**</span><span class="sxs-lookup"><span data-stu-id="e5fdf-120"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>


</dt> <dd>

<span data-ttu-id="e5fdf-121">Le fichier est un fichier de base de données NTDS.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-121">The file is an NTDS database file.</span></span> <span data-ttu-id="e5fdf-122">Ce fichier doit être copié dans le fichier identifié en tant que **\_ \_ base de données BFT NTDS** lorsque les données sont restaurées.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-122">This file should be copied to the file identified as **BFT\_NTDS\_DATABASE** when the data is restored.</span></span>

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span data-ttu-id="e5fdf-123"><span id="BFT_LOG"></span><span id="bft_log"></span>**\_Journal BFT**</span><span class="sxs-lookup"><span data-stu-id="e5fdf-123"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT\_LOG**</span></span>


</dt> <dd>

<span data-ttu-id="e5fdf-124">Le fichier est un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-124">The file is a log file.</span></span> <span data-ttu-id="e5fdf-125">Tous les fichiers journaux sont copiés dans le répertoire identifié en tant que répertoire du **\_ journal \_ BFT** lorsque les données sont restaurées.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-125">All log files are copied to the directory identified as **BFT\_LOG\_DIR** when the data is restored.</span></span>

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span data-ttu-id="e5fdf-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_fichier correctif \_ BFT**</span><span class="sxs-lookup"><span data-stu-id="e5fdf-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT\_PATCH\_FILE**</span></span>


</dt> <dd>

<span data-ttu-id="e5fdf-127">Le fichier est un fichier correctif.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-127">The file is a patch file.</span></span> <span data-ttu-id="e5fdf-128">Tous les fichiers de correctif sont copiés dans le répertoire identifié en tant que répertoire **\_ de point de contrôle \_ BFT** lorsque les données sont restaurées.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-128">All patch files are copied to the directory identified as **BFT\_CHECKPOINT\_DIR** when the data is restored.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e5fdf-129">*PCB* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e5fdf-129">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5fdf-130">Pointeur vers une valeur **DWORD** qui reçoit la taille, en octets, de la mémoire tampon *pszAttachmentInfo* .</span><span class="sxs-lookup"><span data-stu-id="e5fdf-130">Pointer to **DWORD** value that receives the size, in bytes, of the *pszAttachmentInfo* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5fdf-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e5fdf-131">Return value</span></span>

<span data-ttu-id="e5fdf-132">Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-132">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="e5fdf-133">La liste suivante répertorie les autres codes d’erreur possibles.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-133">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="e5fdf-134">**ERREUR d' \_ accès \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="e5fdf-134">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="e5fdf-135">L’appelant ne dispose pas des privilèges d’accès appropriés pour appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-135">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="e5fdf-136">La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour définir les informations d’identification à utiliser pour les fonctions de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-136">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="e5fdf-137">**paramètre d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="e5fdf-137">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="e5fdf-138">*Hbc*, *pszAttachmentInfo* ou *PCB* ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-138">*hbc*, *pszAttachmentInfo*, or *pcbSize* are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="e5fdf-139">**ERREUR \_ de \_ mémoire insuffisante \_**</span><span class="sxs-lookup"><span data-stu-id="e5fdf-139">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="e5fdf-140">Un échec d’allocation de mémoire s’est produit.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-140">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5fdf-141">Notes</span><span class="sxs-lookup"><span data-stu-id="e5fdf-141">Remarks</span></span>

<span data-ttu-id="e5fdf-142">La fonction **DsBackupGetDatabaseNames** fournit une liste des fichiers de base de données nécessaires pour une sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-142">The **DsBackupGetDatabaseNames** function provides a list of the database files necessary for a backup.</span></span> <span data-ttu-id="e5fdf-143">Une sauvegarde complète se compose des fichiers de base de données et des fichiers journaux fournis par la fonction [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) .</span><span class="sxs-lookup"><span data-stu-id="e5fdf-143">A full backup consists of the database files and the log files provided by the [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) function.</span></span> <span data-ttu-id="e5fdf-144">Les sauvegardes incrémentielles des serveurs Active Directory ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e5fdf-144">Incremental backups of Active Directory servers are not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5fdf-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5fdf-145">Requirements</span></span>



| <span data-ttu-id="e5fdf-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5fdf-146">Requirement</span></span> | <span data-ttu-id="e5fdf-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5fdf-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5fdf-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5fdf-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e5fdf-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5fdf-149">Windows Vista</span></span><br/>                                                                    |
| <span data-ttu-id="e5fdf-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5fdf-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e5fdf-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5fdf-151">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="e5fdf-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5fdf-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5fdf-153"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5fdf-153"><dt>Ntdsbcli.h</dt></span></span> </dl>       |
| <span data-ttu-id="e5fdf-154">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e5fdf-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5fdf-155"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5fdf-155"><dt>Ntdsbcli.lib</dt></span></span> </dl>     |
| <span data-ttu-id="e5fdf-156">DLL</span><span class="sxs-lookup"><span data-stu-id="e5fdf-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5fdf-157"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5fdf-157"><dt>Ntdsbcli.dll</dt></span></span> </dl>     |
| <span data-ttu-id="e5fdf-158">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="e5fdf-158">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e5fdf-159">**DsBackupGetDatabaseNamesW** (Unicode) et **DsBackupGetDatabaseNamesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e5fdf-159">**DsBackupGetDatabaseNamesW** (Unicode) and **DsBackupGetDatabaseNamesA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e5fdf-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5fdf-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5fdf-161">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="e5fdf-161">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="e5fdf-162">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="e5fdf-162">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="e5fdf-163">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="e5fdf-163">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="e5fdf-164">**Constantes BFT**</span><span class="sxs-lookup"><span data-stu-id="e5fdf-164">**BFT Constants**</span></span>](bft-constants.md)
</dt> <dt>

[<span data-ttu-id="e5fdf-165">Sauvegarde d’un serveur de Active Directory</span><span class="sxs-lookup"><span data-stu-id="e5fdf-165">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="e5fdf-166">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="e5fdf-166">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

