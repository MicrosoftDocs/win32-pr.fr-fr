---
title: Créer une méthode de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Crée une stratégie d’autorisation de connexion Bureau à distance (RD \ 160 ; CAP) à l’aide des valeurs spécifiées. Le nouveau RD \ 160 ; Le capuchon est inséré en haut du Bureau à distance \ 160 ; Ordre d’évaluation CAP, avec la valeur de propriété Order \ 0034 ; 1 \ 0034 ;.
ms.assetid: 0010cd2b-9c23-488a-9337-d2ed338136d3
ms.tgt_platform: multiple
keywords:
- Créer une méthode Services Bureau à distance
- Create Method Services Bureau à distance, Win32_TSGatewayConnectionAuthorizationPolicy Class
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, Create, méthode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edc027c2f7fc90318bd1af6fd1254077a860a5d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032525"
---
# <a name="create-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="2ab2b-107">Créer une méthode de la \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="2ab2b-107">Create method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="2ab2b-108">Crée une stratégie d’autorisation des connexions Bureau à distance (RD CAP) à l’aide des valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-108">Creates a Remote Desktop connection authorization policy (RD CAP) by using the specified values.</span></span> <span data-ttu-id="2ab2b-109">La nouvelle stratégie d’autorisation des connexions aux services Bureau à distance sera insérée en haut de l’ordre d’évaluation des connexions aux services Bureau à distance, avec une valeur de propriété de **commande** de « 1 ».</span><span class="sxs-lookup"><span data-stu-id="2ab2b-109">The new RD CAP will be inserted at the top of the RD CAP evaluation order, with an **Order** property value of "1".</span></span>

## <a name="syntax"></a><span data-ttu-id="2ab2b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ab2b-110">Syntax</span></span>


```mof
uint32 Create(
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



## <a name="parameters"></a><span data-ttu-id="2ab2b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ab2b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ab2b-112">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-113">Nom de la stratégie d’autorisation des connexions aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-113">Name of the RD CAP.</span></span> <span data-ttu-id="2ab2b-114">Le nom doit comporter 64 caractères ou moins, unique (la casse est ignorée) et ne peut pas contenir les caractères réservés suivants :</span><span class="sxs-lookup"><span data-stu-id="2ab2b-114">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="2ab2b-115"><>  :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="2ab2b-115"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="2ab2b-116">\*\[Onglet\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-116">\* \[TAB\]</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-117">*UserGroupNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-117">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-118">Liste des noms de groupes d’utilisateurs, séparés par des points-virgules, pour la nouvelle stratégie d’autorisation des connexions aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-118">List of user group names, separated by semicolons, for the new RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-119">*ComputerGroupNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-119">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-120">Liste des noms de groupes d’ordinateurs, séparés par des points-virgules, pour la nouvelle stratégie d’autorisation des connexions aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-120">List of computer group names, separated by semicolons, for the new RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-121">*Carte à puce* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-121">*SmartCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-122">Spécifie si les cartes à puce peuvent être utilisées pour l’authentification auprès du serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-122">Specifies whether smart cards can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-123">*Mot de passe* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-123">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-124">Spécifie si les mots de passe peuvent être utilisés pour l’authentification auprès du serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-124">Specifies whether passwords can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-125">*SecureId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-125">*SecureId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-126">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-126">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-127">*Activé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-127">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-128">Spécifie si cette stratégie d’autorisation des connexions aux services Bureau à distance est activée.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-128">Specifies whether this RD CAP is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-129">*DeviceRedirectionType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-129">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-130">Spécifie les types d’appareils qui seront redirigés.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-130">Specifies which device types will be redirected.</span></span>

<dt>

<span data-ttu-id="2ab2b-131">0</span><span class="sxs-lookup"><span data-stu-id="2ab2b-131">0</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-132">Tous les appareils seront redirigés.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-132">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-133">1</span><span class="sxs-lookup"><span data-stu-id="2ab2b-133">1</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-134">Aucun appareil n’est redirigé.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-134">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-135">2</span><span class="sxs-lookup"><span data-stu-id="2ab2b-135">2</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-136">Les appareils spécifiés ne seront pas redirigés.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-136">Specified devices will not be redirected.</span></span> <span data-ttu-id="2ab2b-137">Les paramètres *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled* et *PlugAndPlayDevicesDisabled* contrôlent les appareils qui ne seront pas redirigés.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-137">The *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled*, and *PlugAndPlayDevicesDisabled* parameters control which devices will not be redirected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2ab2b-138">*DiskDrivesDisabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-138">*DiskDrivesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-139">Spécifie s’il faut désactiver la redirection de lecteur de disque si le paramètre *DeviceRedirectionType* est « 2 ».</span><span class="sxs-lookup"><span data-stu-id="2ab2b-139">Specifies whether to disable disk drive redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-140">*PrintersDisabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-140">*PrintersDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-141">Spécifie s’il faut désactiver la redirection de l’imprimante si le paramètre *DeviceRedirectionType* est « 2 ».</span><span class="sxs-lookup"><span data-stu-id="2ab2b-141">Specifies whether to disable printer redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-142">*SerialPortsDisabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-142">*SerialPortsDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-143">Spécifie s’il faut désactiver la redirection de port série si le paramètre *DeviceRedirectionType* est « 2 ».</span><span class="sxs-lookup"><span data-stu-id="2ab2b-143">Specifies whether to disable serial port redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-144">*ClipboardDisabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-144">*ClipboardDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-145">Spécifie s’il faut désactiver la redirection du presse-papiers si le paramètre *DeviceRedirectionType* est « 2 ».</span><span class="sxs-lookup"><span data-stu-id="2ab2b-145">Specifies whether to disable clipboard redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-146">*PlugAndPlayDevicesDisabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-146">*PlugAndPlayDevicesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-147">Spécifie s’il faut désactiver la redirection des appareils Plug-and-Play si le paramètre *DeviceRedirectionType* est « 2 ».</span><span class="sxs-lookup"><span data-stu-id="2ab2b-147">Specifies whether to disable redirection of Plug and Play devices if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-148">*IdleTimeout* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-148">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-149">Valeur du délai d’inactivité en minutes</span><span class="sxs-lookup"><span data-stu-id="2ab2b-149">Idle timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-150">*SessionTimeout* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-150">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-151">Valeur du délai d’expiration de la session en minutes</span><span class="sxs-lookup"><span data-stu-id="2ab2b-151">Session timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-152">*SessionTimeoutAction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-152">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-153">Action du délai d’expiration de session en minutes</span><span class="sxs-lookup"><span data-stu-id="2ab2b-153">Session timeout action in minutes</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-154">*AllowOnlySDRServers* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-154">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-155">Indique si les connexions sont autorisées uniquement pour les serveurs TS SDR</span><span class="sxs-lookup"><span data-stu-id="2ab2b-155">Whether connections allowed only to SDR TS servers</span></span>

</dd> <dt>

<span data-ttu-id="2ab2b-156">*CookieAuthentication* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab2b-156">*CookieAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab2b-157">Indique si l’authentification par cookie peut être utilisée pour se connecter au serveur de passerelle TS</span><span class="sxs-lookup"><span data-stu-id="2ab2b-157">Indicates whether cookie authentication can be used to connect to TS Gateway server</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ab2b-158">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2ab2b-158">Return value</span></span>

<span data-ttu-id="2ab2b-159">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-159">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2ab2b-160">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-160">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2ab2b-161">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2ab2b-161">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2ab2b-162">Notes</span><span class="sxs-lookup"><span data-stu-id="2ab2b-162">Remarks</span></span>

<span data-ttu-id="2ab2b-163">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-163">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2ab2b-164">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="2ab2b-164">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2ab2b-165">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-165">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2ab2b-166">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="2ab2b-166">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2ab2b-167">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2ab2b-167">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ab2b-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ab2b-168">Requirements</span></span>



| <span data-ttu-id="2ab2b-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ab2b-169">Requirement</span></span> | <span data-ttu-id="2ab2b-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ab2b-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab2b-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ab2b-171">Minimum supported client</span></span><br/> | <span data-ttu-id="2ab2b-172">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ab2b-172">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2ab2b-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ab2b-173">Minimum supported server</span></span><br/> | <span data-ttu-id="2ab2b-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ab2b-174">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2ab2b-175">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2ab2b-175">Namespace</span></span><br/>                | <span data-ttu-id="2ab2b-176">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="2ab2b-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2ab2b-177">MOF</span><span class="sxs-lookup"><span data-stu-id="2ab2b-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ab2b-178"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ab2b-178"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ab2b-179">DLL</span><span class="sxs-lookup"><span data-stu-id="2ab2b-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ab2b-180"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ab2b-180"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2ab2b-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ab2b-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ab2b-182">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="2ab2b-182">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

