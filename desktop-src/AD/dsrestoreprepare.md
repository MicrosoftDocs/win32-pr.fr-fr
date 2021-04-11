---
title: DsRestorePrepare, fonction (ntdsbcli. h)
description: Établit une connexion au serveur d’annuaire spécifié et le prépare pour l’opération de restauration.
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsRestorePrepare
topic_type:
- apiref
api_name:
- DsRestorePrepare
- DsRestorePrepareA
- DsRestorePrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb040a315b6cc94f2d296b032a954b00473a4ca2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103500"
---
# <a name="dsrestoreprepare-function"></a><span data-ttu-id="c7429-104">DsRestorePrepare fonction)</span><span class="sxs-lookup"><span data-stu-id="c7429-104">DsRestorePrepare function</span></span>

<span data-ttu-id="c7429-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="c7429-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c7429-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c7429-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c7429-107">À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="c7429-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="c7429-108">La fonction **DsRestorePrepare** se connecte au serveur d’annuaire spécifié et la prépare pour l’opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="c7429-108">The **DsRestorePrepare** function connects to the specified directory server and prepares it for the restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7429-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7429-109">Syntax</span></span>


```C++
HRESULT DsRestorePrepare(
  _In_  LPCWSTR szServerName,
  _In_  ULONG   rtFlag,
  _In_  PVOID   pvExpiryToken,
  _In_  DWORD   cbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a><span data-ttu-id="c7429-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7429-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7429-111">*szServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7429-111">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7429-112">Pointeur vers une chaîne se terminant par un caractère null qui contient le nom du serveur à restaurer.</span><span class="sxs-lookup"><span data-stu-id="c7429-112">Pointer to a null-terminated string that contains the name of the server to restore.</span></span> <span data-ttu-id="c7429-113">Les barres obliques inverses précédentes sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="c7429-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="c7429-114">Le serveur doit être le même que celui à partir duquel cette fonction est appelée.</span><span class="sxs-lookup"><span data-stu-id="c7429-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="c7429-115">Le nom du serveur ne peut pas contenir de caractères de soulignement ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="c7429-115">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="c7429-116">Exemple de nom de serveur \\ \\ : « serveur1 ».</span><span class="sxs-lookup"><span data-stu-id="c7429-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="c7429-117">*rtFlag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7429-117">*rtFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7429-118">Spécifie le type de restauration à effectuer.</span><span class="sxs-lookup"><span data-stu-id="c7429-118">Specifies the type of restoration to perform.</span></span> <span data-ttu-id="c7429-119">Il peut s’agir de zéro ou de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c7429-119">This can be zero or one of the following values.</span></span>

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span data-ttu-id="c7429-120"><span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**TYPE de restauration \_ \_ rattrapage**</span><span class="sxs-lookup"><span data-stu-id="c7429-120"><span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**RESTORE\_TYPE\_CATCHUP**</span></span>


</dt> <dd>

<span data-ttu-id="c7429-121">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="c7429-121">Default.</span></span> <span data-ttu-id="c7429-122">La version restaurée est réutilisée par la logique de réconciliation standard afin que la DIT restaurée puisse se synchroniser avec d’autres ordinateurs serveurs d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c7429-122">The restored version is reconciled through the standard reconciliation logic so that the restored DIT can synchronize with other enterprise server computers.</span></span>

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span data-ttu-id="c7429-123"><span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**TYPE de restauration \_ \_ AUTHORATATIVE**</span><span class="sxs-lookup"><span data-stu-id="c7429-123"><span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**RESTORE\_TYPE\_AUTHORATATIVE**</span></span>


</dt> <dd>

<span data-ttu-id="c7429-124">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c7429-124">Not Supported.</span></span>

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span data-ttu-id="c7429-125"><span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**TYPE de restauration \_ \_ en ligne**</span><span class="sxs-lookup"><span data-stu-id="c7429-125"><span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**RESTORE\_TYPE\_ONLINE**</span></span>


</dt> <dd>

<span data-ttu-id="c7429-126">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c7429-126">Not Supported.</span></span> <span data-ttu-id="c7429-127">La restauration est effectuée lorsque NTDS est en ligne.</span><span class="sxs-lookup"><span data-stu-id="c7429-127">Restoration is performed when NTDS is online.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c7429-128">*pvExpiryToken* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7429-128">*pvExpiryToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7429-129">Pointeur vers le jeton d’expiration associé à la sauvegarde en cours de restauration.</span><span class="sxs-lookup"><span data-stu-id="c7429-129">Pointer to the expiry token associated with the backup being restored.</span></span> <span data-ttu-id="c7429-130">Ce jeton a été obtenu à partir de la fonction [**DsBackupPrepare**](dsbackupprepare.md) lors de la sauvegarde du répertoire.</span><span class="sxs-lookup"><span data-stu-id="c7429-130">This token was obtained from the [**DsBackupPrepare**](dsbackupprepare.md) function when the directory was backed up.</span></span>

<span data-ttu-id="c7429-131">Si ce paramètre a la **valeur null**, le handle retourné dans *phbC* peut uniquement être utilisé pour obtenir les répertoires de restauration avec la fonction [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) .</span><span class="sxs-lookup"><span data-stu-id="c7429-131">If this parameter is **NULL**, the handle returned in *phbc* can only be used to obtain the restoration directories with the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function.</span></span> <span data-ttu-id="c7429-132">Le descripteur ne peut pas être utilisé pour d’autres fonctions de restauration.</span><span class="sxs-lookup"><span data-stu-id="c7429-132">The handle cannot be used for any other restoration functions.</span></span>

</dd> <dt>

<span data-ttu-id="c7429-133">*cbExpiryTokenSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7429-133">*cbExpiryTokenSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7429-134">Contient la taille, en octets, du jeton d’expiration dans *pvExpiryToken*.</span><span class="sxs-lookup"><span data-stu-id="c7429-134">Contains the size, in bytes, of the expiry token in *pvExpiryToken*.</span></span>

</dd> <dt>

<span data-ttu-id="c7429-135">*phbC* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c7429-135">*phbc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7429-136">Pointeur vers une valeur **Hbc** qui reçoit le handle pour la restauration.</span><span class="sxs-lookup"><span data-stu-id="c7429-136">Pointer to an **HBC** value that receives the handle for the restore.</span></span> <span data-ttu-id="c7429-137">Ce descripteur est utilisé lors de l’appel d’autres fonctions de restauration du service d’annuaire, telles que [**DsBackupOpenFile**](dsbackupopenfile.md) et [**DsRestoreEnd**](dsrestoreend.md).</span><span class="sxs-lookup"><span data-stu-id="c7429-137">This handle is used when calling other Directory Service restore functions, such as [**DsBackupOpenFile**](dsbackupopenfile.md) and [**DsRestoreEnd**](dsrestoreend.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7429-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7429-138">Return value</span></span>

<span data-ttu-id="c7429-139">En cas de réussite, retourne un code **HRESULT** standard ; dans le cas contraire, un code d’échec est retourné.</span><span class="sxs-lookup"><span data-stu-id="c7429-139">If successful, returns a standard **HRESULT** codes; otherwise, a failure code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7429-140">Notes</span><span class="sxs-lookup"><span data-stu-id="c7429-140">Remarks</span></span>

<span data-ttu-id="c7429-141">La fonction **DsRestorePrepare** nécessite que l’appelant soit membre du groupe Administrateurs sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="c7429-141">The **DsRestorePrepare** function requires that the caller is a member of the Administrators group on the server.</span></span>

<span data-ttu-id="c7429-142">**DsRestorePrepare** peut être utilisé avec ou sans jeton fourni.</span><span class="sxs-lookup"><span data-stu-id="c7429-142">**DsRestorePrepare** may be used with or without a token provided.</span></span> <span data-ttu-id="c7429-143">Si le jeton est fourni, l’expiration est vérifiée et toutes les opérations sont autorisées sur le contexte retourné.</span><span class="sxs-lookup"><span data-stu-id="c7429-143">If the token is provided, it is checked for expiration, and all operations are allowed on the context returned.</span></span> <span data-ttu-id="c7429-144">Si le jeton n’est pas fourni, le contexte retourné est Restricted et peut être utilisé uniquement pour la fonction [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) .</span><span class="sxs-lookup"><span data-stu-id="c7429-144">If the token is not provided, the context returned is restricted, and may be used only for the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function.</span></span> <span data-ttu-id="c7429-145">Elle ne peut pas être utilisée pour la fonction [**DsRestoreRegister**](dsrestoreregister.md) .</span><span class="sxs-lookup"><span data-stu-id="c7429-145">It may not be used for the [**DsRestoreRegister**](dsrestoreregister.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7429-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7429-146">Requirements</span></span>



| <span data-ttu-id="c7429-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7429-147">Requirement</span></span> | <span data-ttu-id="c7429-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7429-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7429-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7429-149">Minimum supported client</span></span><br/> | <span data-ttu-id="c7429-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7429-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7429-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7429-151">Minimum supported server</span></span><br/> | <span data-ttu-id="c7429-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7429-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7429-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7429-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7429-154"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7429-154"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7429-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c7429-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7429-156"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7429-156"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="c7429-157">DLL</span><span class="sxs-lookup"><span data-stu-id="c7429-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7429-158"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7429-158"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="c7429-159">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="c7429-159">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c7429-160">**DsRestorePrepareW** (Unicode) et **DsRestorePrepareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c7429-160">**DsRestorePrepareW** (Unicode) and **DsRestorePrepareA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="c7429-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7429-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7429-162">Restauration d’un serveur Active Directory</span><span class="sxs-lookup"><span data-stu-id="c7429-162">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="c7429-163">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="c7429-163">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="c7429-164">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="c7429-164">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="c7429-165">**DsRestoreRegister**</span><span class="sxs-lookup"><span data-stu-id="c7429-165">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="c7429-166">**DsRestoreRegisterComplete**</span><span class="sxs-lookup"><span data-stu-id="c7429-166">**DsRestoreRegisterComplete**</span></span>](dsrestoreregistercomplete.md)
</dt> <dt>

[<span data-ttu-id="c7429-167">**DsRestoreEnd**</span><span class="sxs-lookup"><span data-stu-id="c7429-167">**DsRestoreEnd**</span></span>](dsrestoreend.md)
</dt> </dl>

 

