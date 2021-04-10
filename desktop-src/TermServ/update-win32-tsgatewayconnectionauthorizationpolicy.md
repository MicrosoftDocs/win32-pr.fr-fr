---
title: Méthode Update de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Met à jour la stratégie d’autorisation des connexions Bureau à distance en cours (RD \ 160 ; CAP).
ms.assetid: 6d13d1b7-1c7d-4d22-b42c-36e0f4446e86
ms.tgt_platform: multiple
keywords:
- Mettre à jour la méthode Services Bureau à distance
- Mise à jour de la méthode Services Bureau à distance, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Services Bureau à distance de la classe Win32_TSGatewayConnectionAuthorizationPolicy, méthode Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b982030170e954342dc5ff99754dcb89afd0e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032934"
---
# <a name="update-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="3eb8b-106">Méthode Update de la \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="3eb8b-106">Update method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="3eb8b-107">Met à jour la stratégie d’autorisation des connexions Bureau à distance en cours.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-107">Updates the current Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="3eb8b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3eb8b-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string  Name,
  [in] string  UserGroupNames,
  [in] string  ComputerGroupNames,
  [in] boolean SmartCard,
  [in] boolean Password,
  [in] boolean SecureId,
  [in] boolean Enabled,
  [in] uint32  DeviceRedirectionType,
  [in] boolean DiskDrivesDisabled,
  [in] boolean PrintersDisabled,
  [in] boolean SerialPortsDisabled,
  [in] boolean ClipboardDisabled,
  [in] boolean PlugAndPlayDevicesDisabled,
  [in] uint32  IdleTimeout,
  [in] uint32  SessionTimeout,
  [in] uint32  SessionTimeoutAction,
  [in] boolean AllowOnlySDRServers,
  [in] boolean CookieAuthentication
);
```



## <a name="parameters"></a><span data-ttu-id="3eb8b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3eb8b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eb8b-110">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-111">Nom de la stratégie d’autorisation des connexions aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-111">Name of the RD CAP.</span></span> <span data-ttu-id="3eb8b-112">Le nom doit comporter 64 caractères ou moins, unique (la casse est ignorée) et ne peut pas contenir les caractères réservés suivants :</span><span class="sxs-lookup"><span data-stu-id="3eb8b-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="3eb8b-113"><>  :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="3eb8b-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="3eb8b-114">\*\[Onglet\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-114">\* \[TAB\]</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-115">*UserGroupNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-115">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-116">Liste des noms de groupes d’utilisateurs séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-116">List of semicolon-separated user group names.</span></span> <span data-ttu-id="3eb8b-117">Les noms sont au format *domaine \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-117">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="3eb8b-118">Si l’utilisateur appartient à l’un de ces groupes d’utilisateurs, l’utilisateur est autorisé à accéder au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-118">If the user belongs to any one of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-119">*ComputerGroupNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-119">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-120">Liste des noms de groupes d’ordinateurs séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-120">List of semicolon-separated machine group names.</span></span> <span data-ttu-id="3eb8b-121">Cette valeur peut être vide.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-121">This value can be empty.</span></span> <span data-ttu-id="3eb8b-122">Les noms sont au format *domaine \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-122">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="3eb8b-123">Si une valeur est spécifiée, l’ordinateur client doit appartenir à l’un de ces groupes d’ordinateurs pour que l’utilisateur accède au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-123">If a value is specified, the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-124">*Carte à puce* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-124">*SmartCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-125">Spécifie si les cartes à puce peuvent être utilisées pour l’authentification auprès du serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-125">Specifies whether smart cards can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-126">*Mot de passe* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-126">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-127">Spécifie si les mots de passe peuvent être utilisés pour l’authentification auprès du serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-127">Specifies whether passwords can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-128">*SecureId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-128">*SecureId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-129">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-129">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-130">*Activé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-130">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-131">Spécifie si cette stratégie d’autorisation des connexions aux services Bureau à distance est activée.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-131">Specifies whether this RD CAP is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-132">*DeviceRedirectionType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-132">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-133">Spécifie les types d’appareils qui seront redirigés.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-133">Specifies which device types will be redirected.</span></span>

<dt>

<span data-ttu-id="3eb8b-134">0</span><span class="sxs-lookup"><span data-stu-id="3eb8b-134">0</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-135">Tous les appareils seront redirigés.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-135">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-136">1</span><span class="sxs-lookup"><span data-stu-id="3eb8b-136">1</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-137">Aucun appareil n’est redirigé.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-137">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-138">2</span><span class="sxs-lookup"><span data-stu-id="3eb8b-138">2</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-139">Les appareils spécifiés ne seront pas redirigés.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-139">Specified devices will not be redirected.</span></span> <span data-ttu-id="3eb8b-140">Les paramètres *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled* et *PlugAndPlayDevicesDisabled* contrôlent les appareils qui ne seront pas redirigés.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-140">The *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled*, and *PlugAndPlayDevicesDisabled* parameters control which devices will not be redirected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3eb8b-141">*DiskDrivesDisabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-141">*DiskDrivesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-142">Spécifie s’il faut désactiver la redirection de lecteur de disque si le paramètre *DeviceRedirectionType* est « 2 ».</span><span class="sxs-lookup"><span data-stu-id="3eb8b-142">Specifies whether to disable disk drive redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-143">*PrintersDisabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-143">*PrintersDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-144">Spécifie s’il faut désactiver la redirection de l’imprimante si le paramètre *DeviceRedirectionType* est « 2 ».</span><span class="sxs-lookup"><span data-stu-id="3eb8b-144">Specifies whether to disable printer redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-145">*SerialPortsDisabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-145">*SerialPortsDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-146">Spécifie s’il faut désactiver la redirection de port série si le paramètre *DeviceRedirectionType* est « 2 ».</span><span class="sxs-lookup"><span data-stu-id="3eb8b-146">Specifies whether to disable serial port redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-147">*ClipboardDisabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-147">*ClipboardDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-148">Spécifie s’il faut désactiver la redirection du presse-papiers si le paramètre *DeviceRedirectionType* est « 2 ».</span><span class="sxs-lookup"><span data-stu-id="3eb8b-148">Specifies whether to disable clipboard redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-149">*PlugAndPlayDevicesDisabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-149">*PlugAndPlayDevicesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-150">Spécifie s’il faut désactiver la redirection des appareils Plug-and-Play si le paramètre *DeviceRedirectionType* est « 2 ».</span><span class="sxs-lookup"><span data-stu-id="3eb8b-150">Specifies whether to disable redirection of Plug and Play devices if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-151">*IdleTimeout* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-151">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-152">Valeur du délai d’inactivité en minutes</span><span class="sxs-lookup"><span data-stu-id="3eb8b-152">Idle timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-153">*SessionTimeout* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-153">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-154">Valeur du délai d’expiration de la session en minutes</span><span class="sxs-lookup"><span data-stu-id="3eb8b-154">Session timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-155">*SessionTimeoutAction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-155">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-156">Action du délai d’expiration de session en minutes</span><span class="sxs-lookup"><span data-stu-id="3eb8b-156">Session timeout action in minutes</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-157">*AllowOnlySDRServers* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-157">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-158">Indique si les connexions sont autorisées uniquement pour les serveurs TS SDR</span><span class="sxs-lookup"><span data-stu-id="3eb8b-158">Whether connections allowed only to SDR TS servers</span></span>

</dd> <dt>

<span data-ttu-id="3eb8b-159">*CookieAuthentication* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eb8b-159">*CookieAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eb8b-160">Indique si l’authentification par cookie peut être utilisée pour se connecter au serveur de passerelle TS</span><span class="sxs-lookup"><span data-stu-id="3eb8b-160">Indicates whether cookie authentication can be used to connect to TS Gateway server</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eb8b-161">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3eb8b-161">Return value</span></span>

<span data-ttu-id="3eb8b-162">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-162">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3eb8b-163">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-163">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3eb8b-164">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3eb8b-164">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3eb8b-165">Notes</span><span class="sxs-lookup"><span data-stu-id="3eb8b-165">Remarks</span></span>

<span data-ttu-id="3eb8b-166">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-166">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3eb8b-167">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="3eb8b-167">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3eb8b-168">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-168">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3eb8b-169">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="3eb8b-169">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3eb8b-170">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3eb8b-170">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3eb8b-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3eb8b-171">Requirements</span></span>



| <span data-ttu-id="3eb8b-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3eb8b-172">Requirement</span></span> | <span data-ttu-id="3eb8b-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="3eb8b-173">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eb8b-174">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3eb8b-174">Minimum supported client</span></span><br/> | <span data-ttu-id="3eb8b-175">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3eb8b-175">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3eb8b-176">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3eb8b-176">Minimum supported server</span></span><br/> | <span data-ttu-id="3eb8b-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3eb8b-177">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3eb8b-178">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3eb8b-178">Namespace</span></span><br/>                | <span data-ttu-id="3eb8b-179">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="3eb8b-179">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3eb8b-180">MOF</span><span class="sxs-lookup"><span data-stu-id="3eb8b-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3eb8b-181"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3eb8b-181"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3eb8b-182">DLL</span><span class="sxs-lookup"><span data-stu-id="3eb8b-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3eb8b-183"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3eb8b-183"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3eb8b-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3eb8b-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eb8b-185">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="3eb8b-185">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

