---
title: DsBackupGetBackupLogs, fonction (ntdsbcli. h)
description: Obtient la liste des fichiers journaux qui doivent être sauvegardés pour le contexte de sauvegarde donné.
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupGetBackupLogs
topic_type:
- apiref
api_name:
- DsBackupGetBackupLogs
- DsBackupGetBackupLogsA
- DsBackupGetBackupLogsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a02c5c7234810623a95dea030f0c623cca92293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942248"
---
# <a name="dsbackupgetbackuplogs-function"></a><span data-ttu-id="77bc0-104">DsBackupGetBackupLogs fonction)</span><span class="sxs-lookup"><span data-stu-id="77bc0-104">DsBackupGetBackupLogs function</span></span>

<span data-ttu-id="77bc0-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="77bc0-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="77bc0-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="77bc0-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="77bc0-107">À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="77bc0-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="77bc0-108">La fonction **DsBackupGetBackupLogs** obtient la liste des fichiers journaux qui doivent être sauvegardés pour le contexte de sauvegarde donné.</span><span class="sxs-lookup"><span data-stu-id="77bc0-108">The **DsBackupGetBackupLogs** function obtains the list of log files that must be backed up for the given backup context.</span></span>

## <a name="syntax"></a><span data-ttu-id="77bc0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77bc0-109">Syntax</span></span>


```C++
HRESULT DsBackupGetBackupLogs(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszBackupLogFiles,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="77bc0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77bc0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77bc0-111">*Hbc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77bc0-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77bc0-112">Contient le descripteur de contexte de sauvegarde obtenu avec la fonction [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="77bc0-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="77bc0-113">*pszBackupLogFiles* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="77bc0-113">*pszBackupLogFiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77bc0-114">Pointeur vers un pointeur de chaîne qui reçoit la liste de noms de fichiers journaux sous forme de chemins d’accès UNC.</span><span class="sxs-lookup"><span data-stu-id="77bc0-114">Pointer to a string pointer that receives the list of log file names as UNC paths.</span></span> <span data-ttu-id="77bc0-115">Initialisez cette valeur sur **null** avant d’appeler **DsBackupGetBackupLogs**.</span><span class="sxs-lookup"><span data-stu-id="77bc0-115">Initialize this value to **NULL** before calling **DsBackupGetBackupLogs**.</span></span>

<span data-ttu-id="77bc0-116">Cette liste reçoit une liste double terminée par un caractère null de chaînes uniques se terminant par null.</span><span class="sxs-lookup"><span data-stu-id="77bc0-116">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="77bc0-117">Cette mémoire tampon est allouée par la fonction **DsBackupGetBackupLogs** et doit être libérée lorsqu’elle n’est plus nécessaire en appelant la fonction [**DsBackupFree**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="77bc0-117">This buffer is allocated by the **DsBackupGetBackupLogs** function and must be freed when no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="77bc0-118">Le premier caractère de chaque nom de fichier contient une des [**constantes BFT**](bft-constants.md) qui identifient le type de nom.</span><span class="sxs-lookup"><span data-stu-id="77bc0-118">The first character of each of the file names contains one of the [**BFT Constants**](bft-constants.md) that identifies the type of name.</span></span>

</dd> <dt>

<span data-ttu-id="77bc0-119">*PCB* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="77bc0-119">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77bc0-120">Pointeur vers une valeur **DWORD** qui reçoit la taille, en octets, de la mémoire tampon *pszBackupLogFiles* .</span><span class="sxs-lookup"><span data-stu-id="77bc0-120">Pointer to **DWORD** value that receives the size, in bytes, of the *pszBackupLogFiles* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77bc0-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77bc0-121">Return value</span></span>

<span data-ttu-id="77bc0-122">Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="77bc0-122">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="77bc0-123">La liste suivante répertorie les autres codes d’erreur possibles.</span><span class="sxs-lookup"><span data-stu-id="77bc0-123">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="77bc0-124">**ERREUR d' \_ accès \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="77bc0-124">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="77bc0-125">L’appelant ne dispose pas des privilèges d’accès appropriés pour appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="77bc0-125">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="77bc0-126">La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour définir les informations d’identification à utiliser pour les fonctions de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="77bc0-126">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="77bc0-127">**paramètre d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="77bc0-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="77bc0-128">*Hbc*, *pszBackupLogFiles* ou *PCB* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="77bc0-128">*hbc*, *pszBackupLogFiles*, or *pcbSize* is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="77bc0-129">**ERREUR \_ de \_ mémoire insuffisante \_**</span><span class="sxs-lookup"><span data-stu-id="77bc0-129">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="77bc0-130">Un échec d’allocation de mémoire s’est produit.</span><span class="sxs-lookup"><span data-stu-id="77bc0-130">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77bc0-131">Notes</span><span class="sxs-lookup"><span data-stu-id="77bc0-131">Remarks</span></span>

<span data-ttu-id="77bc0-132">La fonction **DsBackupGetBackupLogs** fournit une liste des fichiers journaux nécessaires pour une sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="77bc0-132">The **DsBackupGetBackupLogs** function provides a list of the log files necessary for a backup.</span></span> <span data-ttu-id="77bc0-133">Une sauvegarde complète se compose des fichiers de base de données fournis par la fonction [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) et des fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="77bc0-133">A full backup consists of the database files provided by the [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) function and the log files.</span></span> <span data-ttu-id="77bc0-134">Les sauvegardes incrémentielles des serveurs Active Directory ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="77bc0-134">Incremental backups of Active Directory servers are not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="77bc0-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77bc0-135">Requirements</span></span>



| <span data-ttu-id="77bc0-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77bc0-136">Requirement</span></span> | <span data-ttu-id="77bc0-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="77bc0-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77bc0-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77bc0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="77bc0-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77bc0-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="77bc0-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77bc0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="77bc0-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77bc0-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="77bc0-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="77bc0-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="77bc0-143"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="77bc0-143"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="77bc0-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="77bc0-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="77bc0-145"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77bc0-145"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="77bc0-146">DLL</span><span class="sxs-lookup"><span data-stu-id="77bc0-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77bc0-147"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77bc0-147"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="77bc0-148">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="77bc0-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="77bc0-149">**DsBackupGetBackupLogsW** (Unicode) et **DsBackupGetBackupLogsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="77bc0-149">**DsBackupGetBackupLogsW** (Unicode) and **DsBackupGetBackupLogsA** (ANSI)</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="77bc0-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77bc0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77bc0-151">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="77bc0-151">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="77bc0-152">**DsBackupGetDatabaseNames**</span><span class="sxs-lookup"><span data-stu-id="77bc0-152">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
</dt> <dt>

[<span data-ttu-id="77bc0-153">**Constantes BFT**</span><span class="sxs-lookup"><span data-stu-id="77bc0-153">**BFT Constants**</span></span>](bft-constants.md)
</dt> <dt>

[<span data-ttu-id="77bc0-154">Sauvegarde d’un serveur de Active Directory</span><span class="sxs-lookup"><span data-stu-id="77bc0-154">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="77bc0-155">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="77bc0-155">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

