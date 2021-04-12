---
title: DsBackupOpenFile, fonction (ntdsbcli. h)
description: Ouvre le fichier spécifié et exécute les opérations du client et du serveur nécessaires à la préparation du fichier pour la sauvegarde.
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupOpenFile
topic_type:
- apiref
api_name:
- DsBackupOpenFile
- DsBackupOpenFileA
- DsBackupOpenFileW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f9c4eac9c9825f510848583d7f707a2c244c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104056"
---
# <a name="dsbackupopenfile-function"></a><span data-ttu-id="d6d2a-104">DsBackupOpenFile fonction)</span><span class="sxs-lookup"><span data-stu-id="d6d2a-104">DsBackupOpenFile function</span></span>

<span data-ttu-id="d6d2a-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="d6d2a-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d6d2a-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d6d2a-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d6d2a-107">À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="d6d2a-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="d6d2a-108">La fonction **DsBackupOpenFile** ouvre le fichier spécifié et exécute les opérations du client et du serveur nécessaires à la préparation du fichier pour la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="d6d2a-108">The **DsBackupOpenFile** function opens the specified file and performs the client and server operations necessary to prepare the file for backup.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d2a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6d2a-109">Syntax</span></span>


```C++
HRESULT DsBackupOpenFile(
  _In_  HBC           hbc,
  _In_  LPCTSTR       szAttachmentName,
  _In_  DWORD         cbReadHintSize,
  _Out_ LARGE_INTEGER *pliFileSize
);
```



## <a name="parameters"></a><span data-ttu-id="d6d2a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6d2a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6d2a-111">*Hbc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6d2a-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d2a-112">Contient le descripteur de contexte de sauvegarde obtenu avec la fonction [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="d6d2a-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d6d2a-113">*szAttachmentName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6d2a-113">*szAttachmentName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d2a-114">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du fichier de sauvegarde à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="d6d2a-114">Pointer to a null-terminated string that specifies the name of the backup file to open.</span></span>

</dd> <dt>

<span data-ttu-id="d6d2a-115">*cbReadHintSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6d2a-115">*cbReadHintSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d2a-116">Contient la taille possible, en octets, de la mémoire tampon passée comme argument *pvBuffer* dans la fonction [**DsBackupRead**](dsbackupread.md) .</span><span class="sxs-lookup"><span data-stu-id="d6d2a-116">Contains the possible size, in bytes, of the buffer passed as the *pvBuffer* argument in the [**DsBackupRead**](dsbackupread.md) function.</span></span> <span data-ttu-id="d6d2a-117">Les fonctions de sauvegarde utilisent cette valeur comme indication pour optimiser le trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="d6d2a-117">The backup functions use this value as a hint to optimize the network traffic.</span></span> <span data-ttu-id="d6d2a-118">Cette valeur doit être un multiple de 8192 et doit être supérieur ou égal à 24576.</span><span class="sxs-lookup"><span data-stu-id="d6d2a-118">This value must be a multiple of 8192 and must be greater than or equal to 24576.</span></span>

</dd> <dt>

<span data-ttu-id="d6d2a-119">*pliFileSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d6d2a-119">*pliFileSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d2a-120">Pointeur vers une **valeur \_ entière de type long** qui reçoit la taille, en octets, du fichier de sauvegarde ouvert.</span><span class="sxs-lookup"><span data-stu-id="d6d2a-120">Pointer to a **LARGE\_INTEGER** value that receives the size, in bytes, of the backup file opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6d2a-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6d2a-121">Return value</span></span>

<span data-ttu-id="d6d2a-122">Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d6d2a-122">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="d6d2a-123">La liste suivante répertorie les autres codes d’erreur possibles.</span><span class="sxs-lookup"><span data-stu-id="d6d2a-123">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="d6d2a-124">**ERREUR d' \_ accès \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="d6d2a-124">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="d6d2a-125">L’appelant ne dispose pas des privilèges d’accès appropriés pour appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="d6d2a-125">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="d6d2a-126">La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour définir les informations d’identification à utiliser pour les fonctions de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="d6d2a-126">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="d6d2a-127">**paramètre d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d6d2a-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="d6d2a-128">*Hbc*, *szAttachmentName* ou *pliFileSize* ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="d6d2a-128">*hbc*, *szAttachmentName*, or *pliFileSize* are invalid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6d2a-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6d2a-129">Requirements</span></span>



| <span data-ttu-id="d6d2a-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6d2a-130">Requirement</span></span> | <span data-ttu-id="d6d2a-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6d2a-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d2a-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6d2a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d6d2a-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6d2a-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6d2a-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6d2a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d6d2a-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6d2a-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6d2a-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6d2a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6d2a-137"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6d2a-137"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6d2a-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d6d2a-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6d2a-139"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6d2a-139"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="d6d2a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d6d2a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6d2a-141"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6d2a-141"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="d6d2a-142">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="d6d2a-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d6d2a-143">**DsBackupOpenFileW** (Unicode) et **DsBackupOpenFileA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d6d2a-143">**DsBackupOpenFileW** (Unicode) and **DsBackupOpenFileA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d6d2a-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6d2a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6d2a-145">**DsBackupRead**</span><span class="sxs-lookup"><span data-stu-id="d6d2a-145">**DsBackupRead**</span></span>](dsbackupread.md)
</dt> <dt>

[<span data-ttu-id="d6d2a-146">Sauvegarde d’un serveur de Active Directory</span><span class="sxs-lookup"><span data-stu-id="d6d2a-146">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="d6d2a-147">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="d6d2a-147">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

