---
title: DsSetCurrentBackupLog, fonction (ntdsbcli. h)
description: Définit le numéro de journal de sauvegarde actuel après une restauration réussie.
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsSetCurrentBackupLog
topic_type:
- apiref
api_name:
- DsSetCurrentBackupLog
- DsSetCurrentBackupLogA
- DsSetCurrentBackupLogW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f50fc41317ae22ae89c47f63bb19f981563e5c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843829"
---
# <a name="dssetcurrentbackuplog-function"></a><span data-ttu-id="2b6b9-104">DsSetCurrentBackupLog fonction)</span><span class="sxs-lookup"><span data-stu-id="2b6b9-104">DsSetCurrentBackupLog function</span></span>

<span data-ttu-id="2b6b9-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="2b6b9-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2b6b9-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2b6b9-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="2b6b9-107">À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="2b6b9-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="2b6b9-108">La fonction **DsSetCurrentBackupLog** définit le numéro de journal de sauvegarde actuel après une restauration réussie.</span><span class="sxs-lookup"><span data-stu-id="2b6b9-108">The **DsSetCurrentBackupLog** function sets the current backup log number after a successful restore.</span></span> <span data-ttu-id="2b6b9-109">Étant donné que les Active Directory Domain Services prennent uniquement en charge la journalisation circulaire, cette fonction n’est généralement pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2b6b9-109">Because Active Directory Domain Services only support circular logging, this function is not normally used.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b6b9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b6b9-110">Syntax</span></span>


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a><span data-ttu-id="2b6b9-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b6b9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b6b9-112">*szServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b6b9-112">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6b9-113">Pointeur vers une chaîne se terminant par un caractère null qui contient le nom du serveur pour lequel le numéro de journal de sauvegarde doit être défini.</span><span class="sxs-lookup"><span data-stu-id="2b6b9-113">Pointer to a null-terminated string that contains the name of the server to set the backup log number for.</span></span> <span data-ttu-id="2b6b9-114">Les barres obliques inverses précédentes sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="2b6b9-114">Preceding backslashes are optional.</span></span> <span data-ttu-id="2b6b9-115">Le serveur doit être le même que celui à partir duquel cette fonction est appelée.</span><span class="sxs-lookup"><span data-stu-id="2b6b9-115">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="2b6b9-116">Le nom du serveur ne peut pas contenir de caractères de soulignement ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="2b6b9-116">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="2b6b9-117">Exemple de nom de serveur \\ \\ : « serveur1 ».</span><span class="sxs-lookup"><span data-stu-id="2b6b9-117">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="2b6b9-118">*dwCurrentLog* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b6b9-118">*dwCurrentLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6b9-119">Contient le numéro de journal de sauvegarde à définir.</span><span class="sxs-lookup"><span data-stu-id="2b6b9-119">Contains the backup log number to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b6b9-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2b6b9-120">Return value</span></span>

<span data-ttu-id="2b6b9-121">Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2b6b9-121">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="2b6b9-122">La liste suivante répertorie les codes d’erreur possibles.</span><span class="sxs-lookup"><span data-stu-id="2b6b9-122">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="2b6b9-123">**paramètre d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2b6b9-123">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="2b6b9-124">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="2b6b9-124">One or more parameters are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="2b6b9-125">**ERREUR \_ de \_ mémoire insuffisante \_**</span><span class="sxs-lookup"><span data-stu-id="2b6b9-125">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="2b6b9-126">Un échec d’allocation de mémoire s’est produit.</span><span class="sxs-lookup"><span data-stu-id="2b6b9-126">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b6b9-127">Notes</span><span class="sxs-lookup"><span data-stu-id="2b6b9-127">Remarks</span></span>

<span data-ttu-id="2b6b9-128">Normalement, il n’est pas nécessaire d’appeler la fonction **DsSetCurrentBackupLog** .</span><span class="sxs-lookup"><span data-stu-id="2b6b9-128">It is not normally required to call the **DsSetCurrentBackupLog** function.</span></span> <span data-ttu-id="2b6b9-129">Les fonctions de sauvegarde déterminent et définissent automatiquement le dernier numéro de journal sauvegardé.</span><span class="sxs-lookup"><span data-stu-id="2b6b9-129">The backup functions automatically determine and set the last log number backed up.</span></span> <span data-ttu-id="2b6b9-130">Utilisez **DsSetCurrentBackupLog** pour empêcher une autre sauvegarde incrémentielle de se dérouler jusqu’à ce qu’une sauvegarde complète soit effectuée.</span><span class="sxs-lookup"><span data-stu-id="2b6b9-130">Use **DsSetCurrentBackupLog** to prevent another incremental backup from succeeding until a full backup is performed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b6b9-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b6b9-131">Requirements</span></span>



| <span data-ttu-id="2b6b9-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b6b9-132">Requirement</span></span> | <span data-ttu-id="2b6b9-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b6b9-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b6b9-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b6b9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2b6b9-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b6b9-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2b6b9-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b6b9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2b6b9-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b6b9-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2b6b9-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b6b9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b6b9-139"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b6b9-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b6b9-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2b6b9-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b6b9-141"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b6b9-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="2b6b9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2b6b9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b6b9-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b6b9-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b6b9-144">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="2b6b9-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2b6b9-145">**DsSetCurrentBackupLogW** (Unicode) et **DsSetCurrentBackupLogA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2b6b9-145">**DsSetCurrentBackupLogW** (Unicode) and **DsSetCurrentBackupLogA** (ANSI)</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="2b6b9-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b6b9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b6b9-147">Sauvegarde et restauration d’un serveur Active Directory</span><span class="sxs-lookup"><span data-stu-id="2b6b9-147">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="2b6b9-148">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="2b6b9-148">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

