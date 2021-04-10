---
title: DsIsNTDSOnline, fonction (ntdsbcli. h)
description: Détermine si Active Directory Domain Services sont en ligne sur le serveur spécifié.
ms.assetid: 8f46e4d8-6d05-402c-a5b4-291fd2d6609b
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsIsNTDSOnline
topic_type:
- apiref
api_name:
- DsIsNTDSOnline
- DsIsNTDSOnlineA
- DsIsNTDSOnlineW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f6728f4481eb8820055b48f10cfa0f94c7aaa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103798"
---
# <a name="dsisntdsonline-function"></a><span data-ttu-id="6fc66-104">DsIsNTDSOnline fonction)</span><span class="sxs-lookup"><span data-stu-id="6fc66-104">DsIsNTDSOnline function</span></span>

<span data-ttu-id="6fc66-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="6fc66-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6fc66-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="6fc66-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6fc66-107">À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="6fc66-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="6fc66-108">La fonction **DsIsNTDSOnline** détermine si Active Directory Domain Services sont en ligne sur le serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="6fc66-108">The **DsIsNTDSOnline** function determines if Active Directory Domain Services are online on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fc66-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fc66-109">Syntax</span></span>


```C++
HRESULT DsIsNTDSOnline(
  _In_  LPCTSTR szServerName,
  _Out_ BOOL    *pfNTDSOnline
);
```



## <a name="parameters"></a><span data-ttu-id="6fc66-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fc66-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fc66-111">*szServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6fc66-111">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fc66-112">Pointeur vers une chaîne se terminant par un caractère null qui contient le nom du serveur à tester.</span><span class="sxs-lookup"><span data-stu-id="6fc66-112">Pointer to a null-terminated string that contains the name of the server to test.</span></span> <span data-ttu-id="6fc66-113">Les barres obliques inverses précédentes sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="6fc66-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="6fc66-114">Le serveur doit être le même que celui à partir duquel cette fonction est appelée.</span><span class="sxs-lookup"><span data-stu-id="6fc66-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="6fc66-115">Le nom du serveur ne peut pas contenir de caractères de soulignement ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="6fc66-115">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="6fc66-116">Exemple de nom de serveur \\ \\ : « serveur1 ».</span><span class="sxs-lookup"><span data-stu-id="6fc66-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="6fc66-117">*pfNTDSOnline* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6fc66-117">*pfNTDSOnline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fc66-118">Pointeur vers une valeur **bool** qui reçoit le résultat.</span><span class="sxs-lookup"><span data-stu-id="6fc66-118">Pointer to **BOOL** value that receives the result.</span></span> <span data-ttu-id="6fc66-119">Reçoit la **valeur true** si le service d’annuaire est en ligne ou **false** si le service d’annuaire est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="6fc66-119">Receives **TRUE** if the directory service is online or **FALSE** if the directory service is offline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fc66-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6fc66-120">Return value</span></span>

<span data-ttu-id="6fc66-121">Retourne **S \_ OK** si la fonction réussit ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6fc66-121">Returns **S\_OK** if the function is successful or an error code otherwise.</span></span> <span data-ttu-id="6fc66-122">La liste suivante répertorie les codes d’erreur possibles.</span><span class="sxs-lookup"><span data-stu-id="6fc66-122">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="6fc66-123">**ERREUR d' \_ accès \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="6fc66-123">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="6fc66-124">L’appelant ne dispose pas des privilèges d’accès appropriés pour appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="6fc66-124">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="6fc66-125">La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour définir les informations d’identification à utiliser pour les fonctions de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="6fc66-125">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="6fc66-126">**hrCouldNotConnect**</span><span class="sxs-lookup"><span data-stu-id="6fc66-126">**hrCouldNotConnect**</span></span>
</dt> <dd>

<span data-ttu-id="6fc66-127">Le serveur dans *szServerName* est introuvable, n’est pas un contrôleur de domaine ou *szServerName* n’est pas mis en forme correctement.</span><span class="sxs-lookup"><span data-stu-id="6fc66-127">The server in *szServerName* cannot be found, is not a domain controller, or *szServerName* is not formatted correctly.</span></span> <span data-ttu-id="6fc66-128">Cette valeur est définie dans ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="6fc66-128">This value is defined in Ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="6fc66-129">**\_liaison RPC S \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="6fc66-129">**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd>

<span data-ttu-id="6fc66-130">La fonction [**DsIsNTDSOnline**](dsisntdsonline.md) est appelée à distance ou le serveur dans *szServerName* n’est pas un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="6fc66-130">The [**DsIsNTDSOnline**](dsisntdsonline.md) function is being called remotely or the server in *szServerName* is not a domain controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6fc66-131">Notes</span><span class="sxs-lookup"><span data-stu-id="6fc66-131">Remarks</span></span>

<span data-ttu-id="6fc66-132">Appelez cette fonction avant d’appeler l’une des fonctions de sauvegarde ou de restauration de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6fc66-132">Call this function before calling any of the directory backup or restore functions.</span></span> <span data-ttu-id="6fc66-133">Le répertoire doit être en ligne pour pouvoir effectuer une sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="6fc66-133">The directory must be online in order to perform a backup.</span></span> <span data-ttu-id="6fc66-134">Le répertoire doit être en mode hors connexion pour effectuer une restauration.</span><span class="sxs-lookup"><span data-stu-id="6fc66-134">The directory must by offline to perform a restore.</span></span>

<span data-ttu-id="6fc66-135">Cette fonction ne peut être appelée qu’à partir d’un contrôleur de domaine qui est également le serveur cible spécifié dans *szServerName*.</span><span class="sxs-lookup"><span data-stu-id="6fc66-135">This function can only be called from a domain controller that is also the target server specified in *szServerName*.</span></span> <span data-ttu-id="6fc66-136">Cette fonction ne peut pas être appelée à distance.</span><span class="sxs-lookup"><span data-stu-id="6fc66-136">This function cannot be called remotely.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fc66-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fc66-137">Requirements</span></span>



| <span data-ttu-id="6fc66-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fc66-138">Requirement</span></span> | <span data-ttu-id="6fc66-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fc66-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc66-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fc66-140">Minimum supported client</span></span><br/> | <span data-ttu-id="6fc66-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6fc66-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6fc66-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fc66-142">Minimum supported server</span></span><br/> | <span data-ttu-id="6fc66-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fc66-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6fc66-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="6fc66-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fc66-145"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fc66-145"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="6fc66-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6fc66-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="6fc66-147"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fc66-147"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="6fc66-148">DLL</span><span class="sxs-lookup"><span data-stu-id="6fc66-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fc66-149"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fc66-149"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="6fc66-150">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="6fc66-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6fc66-151">**DsIsNTDSOnlineW** (Unicode) et **DsIsNTDSOnlineA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6fc66-151">**DsIsNTDSOnlineW** (Unicode) and **DsIsNTDSOnlineA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6fc66-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fc66-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fc66-153">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="6fc66-153">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="6fc66-154">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="6fc66-154">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="6fc66-155">Sauvegarde et restauration d’un serveur Active Directory</span><span class="sxs-lookup"><span data-stu-id="6fc66-155">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> </dl>

 

