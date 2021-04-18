---
title: Méthode ModifyPermissions de la classe Win32_TSAccount
description: Définit une autorisation pour le compte spécifié.
ms.assetid: cef36f7f-d327-4bb6-9bff-282036c1a5d5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ModifyPermissions
- Services Bureau à distance de la méthode ModifyPermissions, classe Win32_TSAccount
- Win32_TSAccount de la classe Services Bureau à distance, méthode ModifyPermissions
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4bf6147c215475314f65bb8fa426442884bc82e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511758"
---
# <a name="modifypermissions-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="60fe8-106">Méthode ModifyPermissions de la \_ classe Win32 TSAccount</span><span class="sxs-lookup"><span data-stu-id="60fe8-106">ModifyPermissions method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="60fe8-107">Définit une autorisation pour le compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="60fe8-107">Sets a permission for the specified account.</span></span>

## <a name="syntax"></a><span data-ttu-id="60fe8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60fe8-108">Syntax</span></span>


```mof
uint32 ModifyPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Allow
);
```



## <a name="parameters"></a><span data-ttu-id="60fe8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60fe8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60fe8-110">*PermissionMask* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60fe8-110">*PermissionMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60fe8-111">Autorisation de l' [hôte de Session Bureau à distance](terminal-services-permissions.md) pour définir.</span><span class="sxs-lookup"><span data-stu-id="60fe8-111">The [Remote Desktop Session Host Permission](terminal-services-permissions.md) to set.</span></span>

<span data-ttu-id="60fe8-112">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="60fe8-112">The possible values are:</span></span>

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span data-ttu-id="60fe8-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**Station \_ de REQUÊTE** (0)</span><span class="sxs-lookup"><span data-stu-id="60fe8-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION\_QUERY** (0)</span></span>


</dt> <dd>

<span data-ttu-id="60fe8-114">Autorisation d’interroger les informations relatives à une session.</span><span class="sxs-lookup"><span data-stu-id="60fe8-114">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="60fe8-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**Station \_ de SET** (1)</span><span class="sxs-lookup"><span data-stu-id="60fe8-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (1)</span></span>


</dt> <dd>

<span data-ttu-id="60fe8-116">Autorisation de modifier les paramètres de connexion.</span><span class="sxs-lookup"><span data-stu-id="60fe8-116">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="60fe8-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**Station \_ de RÉINITIALISER** (6)</span><span class="sxs-lookup"><span data-stu-id="60fe8-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (6)</span></span>


</dt> <dd>

<span data-ttu-id="60fe8-118">Autorisation de réinitialiser ou de mettre fin à une session ou à une connexion.</span><span class="sxs-lookup"><span data-stu-id="60fe8-118">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="60fe8-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**Station \_ de \| Droits standard \_ virtuels \_ requis** (3)</span><span class="sxs-lookup"><span data-stu-id="60fe8-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (3)</span></span>


</dt> <dd>

<span data-ttu-id="60fe8-120">Autorisation d’utiliser des canaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="60fe8-120">Permission to use virtual channels.</span></span> <span data-ttu-id="60fe8-121">Les canaux virtuels fournissent un accès à partir d’un programme serveur sur les périphériques clients.</span><span class="sxs-lookup"><span data-stu-id="60fe8-121">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="60fe8-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**Station \_ de OMBRE** (4)</span><span class="sxs-lookup"><span data-stu-id="60fe8-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (4)</span></span>


</dt> <dd>

<span data-ttu-id="60fe8-123">Autorisation d’ombrer ou de contrôler à distance la session d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="60fe8-123">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="60fe8-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**Station \_ de Ouverture de session** (5)</span><span class="sxs-lookup"><span data-stu-id="60fe8-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (5)</span></span>


</dt> <dd>

<span data-ttu-id="60fe8-125">Autorisation de se connecter à une session sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="60fe8-125">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="60fe8-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**Station \_ de Fermeture de session** (2)</span><span class="sxs-lookup"><span data-stu-id="60fe8-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (2)</span></span>


</dt> <dd>

<span data-ttu-id="60fe8-127">Autorisation de fermer la session d’un utilisateur à partir d’une session.</span><span class="sxs-lookup"><span data-stu-id="60fe8-127">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="60fe8-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**Station \_ de MSG** (7)</span><span class="sxs-lookup"><span data-stu-id="60fe8-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (7)</span></span>


</dt> <dd>

<span data-ttu-id="60fe8-129">Autorisation d’envoyer un message à la session d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="60fe8-129">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="60fe8-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**Station \_ de SE connecter** (8)</span><span class="sxs-lookup"><span data-stu-id="60fe8-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (8)</span></span>


</dt> <dd>

<span data-ttu-id="60fe8-131">Autorisation de se connecter à une autre session.</span><span class="sxs-lookup"><span data-stu-id="60fe8-131">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="60fe8-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**Station \_ de Déconnexion** (9)</span><span class="sxs-lookup"><span data-stu-id="60fe8-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (9)</span></span>


</dt> <dd>

<span data-ttu-id="60fe8-133">Autorisation de déconnecter une session.</span><span class="sxs-lookup"><span data-stu-id="60fe8-133">Permission to disconnect a session.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="60fe8-134">*Autoriser* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60fe8-134">*Allow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60fe8-135">Spécifie si l’autorisation dans le paramètre *PermissionMask* est autorisée ou refusée.</span><span class="sxs-lookup"><span data-stu-id="60fe8-135">Specifies whether the permission in the *PermissionMask* parameter is allowed or denied.</span></span>

<span data-ttu-id="60fe8-136">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="60fe8-136">The possible values are:</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="60fe8-137"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="60fe8-137"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="60fe8-138">Le jeu d’autorisations spécifié est autorisé.</span><span class="sxs-lookup"><span data-stu-id="60fe8-138">The specified permission set is allowed.</span></span>

</dd> <dt>

<span id="0"></span>

<span data-ttu-id="60fe8-139"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="60fe8-139"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="60fe8-140">Le jeu d’autorisations spécifié est refusé.</span><span class="sxs-lookup"><span data-stu-id="60fe8-140">The specified permission set is denied.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60fe8-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60fe8-141">Return value</span></span>

<span data-ttu-id="60fe8-142">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="60fe8-142">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="60fe8-143">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="60fe8-143">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="60fe8-144">Notes</span><span class="sxs-lookup"><span data-stu-id="60fe8-144">Remarks</span></span>

<span data-ttu-id="60fe8-145">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="60fe8-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="60fe8-146">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="60fe8-146">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="60fe8-147">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="60fe8-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="60fe8-148">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="60fe8-148">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="60fe8-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60fe8-149">Requirements</span></span>



| <span data-ttu-id="60fe8-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60fe8-150">Requirement</span></span> | <span data-ttu-id="60fe8-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="60fe8-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60fe8-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60fe8-152">Minimum supported client</span></span><br/> | <span data-ttu-id="60fe8-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60fe8-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60fe8-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60fe8-154">Minimum supported server</span></span><br/> | <span data-ttu-id="60fe8-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60fe8-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60fe8-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="60fe8-156">Namespace</span></span><br/>                | <span data-ttu-id="60fe8-157">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="60fe8-157">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="60fe8-158">MOF</span><span class="sxs-lookup"><span data-stu-id="60fe8-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60fe8-159"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60fe8-159"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="60fe8-160">DLL</span><span class="sxs-lookup"><span data-stu-id="60fe8-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60fe8-161"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60fe8-161"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60fe8-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60fe8-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60fe8-163">**\_TSAccount Win32**</span><span class="sxs-lookup"><span data-stu-id="60fe8-163">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 

