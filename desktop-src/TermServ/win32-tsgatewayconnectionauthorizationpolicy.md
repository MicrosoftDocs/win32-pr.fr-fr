---
title: Classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Décrit une stratégie d’autorisation des connexions Bureau à distance (RD \ 160 ; CAP). RD \ 160 ; Les limites sont utilisées pour déterminer si un utilisateur est autorisé à se connecter au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy.Name
- Win32_TSGatewayConnectionAuthorizationPolicy.Order
- Win32_TSGatewayConnectionAuthorizationPolicy.SmartcardAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.PasswordAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.SecureIdAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.CookieAuthenticationAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.Enabled
- Win32_TSGatewayConnectionAuthorizationPolicy.IdleTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeoutAction
- Win32_TSGatewayConnectionAuthorizationPolicy.DeviceRedirectionType
- Win32_TSGatewayConnectionAuthorizationPolicy.DiskDrivesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PrintersDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.SerialPortsDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.ClipboardDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PlugAndPlayDevicesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.ComputerGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.HasNapAttributes
- Win32_TSGatewayConnectionAuthorizationPolicy.AllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27384ec3a5f17c3e41fe0ceccf0ee1f7f9d08044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843461"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="2e0b9-106">\_Classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="2e0b9-106">Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="2e0b9-107">Décrit une stratégie d’autorisation de connexion Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-107">Describes a Remote Desktop connection authorization policy (RD CAP).</span></span> <span data-ttu-id="2e0b9-108">Les limitations des services Bureau à distance sont utilisées pour déterminer si un utilisateur est autorisé à se connecter au serveur de passerelle Bureau à distance (passerelle Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="2e0b9-108">RD CAPs are used to determine whether a user is allowed to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e0b9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e0b9-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnectionAuthorizationPolicy
{
  string  Name;
  uint32  Order;
  boolean SmartcardAllowed;
  boolean PasswordAllowed;
  boolean SecureIdAllowed;
  boolean CookieAuthenticationAllowed;
  boolean Enabled;
  uint32  IdleTimeout;
  uint32  SessionTimeout;
  uint32  SessionTimeoutAction;
  uint32  DeviceRedirectionType;
  boolean DiskDrivesDisabled;
  boolean PrintersDisabled;
  boolean SerialPortsDisabled;
  boolean ClipboardDisabled;
  boolean PlugAndPlayDevicesDisabled;
  string  UserGroupNames;
  string  ComputerGroupNames;
  boolean HasNapAttributes;
  boolean AllowOnlySDRServers;
};
```

## <a name="members"></a><span data-ttu-id="2e0b9-110">Membres</span><span class="sxs-lookup"><span data-stu-id="2e0b9-110">Members</span></span>

<span data-ttu-id="2e0b9-111">La classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2e0b9-111">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these types of members:</span></span>

-   [<span data-ttu-id="2e0b9-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2e0b9-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2e0b9-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2e0b9-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2e0b9-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2e0b9-114">Methods</span></span>

<span data-ttu-id="2e0b9-115">La classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-115">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these methods.</span></span>



| <span data-ttu-id="2e0b9-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="2e0b9-116">Method</span></span>                                                                                                                | <span data-ttu-id="2e0b9-117">Description</span><span class="sxs-lookup"><span data-stu-id="2e0b9-117">Description</span></span>                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e0b9-118">**AddComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-118">**AddComputerGroupNames**</span></span>](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | <span data-ttu-id="2e0b9-119">Ajoute les noms de groupes d’ordinateurs spécifiés à la propriété **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-119">Adds the specified computer group names to the **ComputerGroupNames** property.</span></span><br/>                                                                                      |
| [<span data-ttu-id="2e0b9-120">**AddUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-120">**AddUserGroupNames**</span></span>](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="2e0b9-121">Ajoute les noms de groupes d’utilisateurs spécifiés à la propriété **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-121">Adds the specified user group names to the **UserGroupNames** property.</span></span><br/>                                                                                              |
| [<span data-ttu-id="2e0b9-122">**Créés**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-122">**Create**</span></span>](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="2e0b9-123">Crée une stratégie d’autorisation des connexions aux services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="2e0b9-123">Creates an RD CAP.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="2e0b9-124">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-124">**Delete**</span></span>](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="2e0b9-125">Supprime la stratégie d’autorisation des connexions aux services Bureau à distance actuelle.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-125">Deletes the current RD CAP.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="2e0b9-126">**DisableClipboard**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-126">**DisableClipboard**</span></span>](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | <span data-ttu-id="2e0b9-127">Définit la propriété **ClipboardDisabled** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-127">Sets the **ClipboardDisabled** property.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="2e0b9-128">**DisableDiskDrives**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-128">**DisableDiskDrives**</span></span>](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="2e0b9-129">Définit la propriété **DiskDrivesDisabled** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-129">Sets the **DiskDrivesDisabled** property.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="2e0b9-130">**DisablePlugAndPlayDevices**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-130">**DisablePlugAndPlayDevices**</span></span>](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | <span data-ttu-id="2e0b9-131">Définit la propriété **PlugAndPlayDevicesDisabled** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-131">Sets the **PlugAndPlayDevicesDisabled** property.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="2e0b9-132">**DisablePrinters**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-132">**DisablePrinters**</span></span>](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | <span data-ttu-id="2e0b9-133">Définit la propriété **PrintersDisabled** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-133">Sets the **PrintersDisabled** property.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="2e0b9-134">**DisableSerialPorts**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-134">**DisableSerialPorts**</span></span>](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="2e0b9-135">Définit la propriété **SerialPortsDisabled** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-135">Sets the **SerialPortsDisabled** property.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="2e0b9-136">**EnableAllowOnlySDRServers**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-136">**EnableAllowOnlySDRServers**</span></span>](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | <span data-ttu-id="2e0b9-137">Utilisé pour basculer la propriété **AllowOnlySDRServers**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-137">Used to toggle the **AllowOnlySDRServers** property</span></span><br/> <span data-ttu-id="2e0b9-138">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-138">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                  |
| [<span data-ttu-id="2e0b9-139">**Descendre**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-139">**MoveDown**</span></span>](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | <span data-ttu-id="2e0b9-140">Déplace la position de la stratégie d’autorisation des connexions aux services Bureau à distance active vers le début dans la liste.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-140">Moves the current RD CAP one position down in the list.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="2e0b9-141">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-141">**MoveUp**</span></span>](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="2e0b9-142">Déplace la position de la stratégie d’autorisation des connexions aux services Bureau à distance actuelle vers le haut dans la liste.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-142">Moves the current RD CAP one position up in the list.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="2e0b9-143">**RemoveComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-143">**RemoveComputerGroupNames**</span></span>](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | <span data-ttu-id="2e0b9-144">Supprime les noms de groupes d’ordinateurs spécifiés de la propriété **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-144">Removes the specified computer group names from the **ComputerGroupNames** property.</span></span><br/>                                                                                 |
| [<span data-ttu-id="2e0b9-145">**RemoveUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-145">**RemoveUserGroupNames**</span></span>](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | <span data-ttu-id="2e0b9-146">Supprime les noms de groupes d’utilisateurs spécifiés de la propriété **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-146">Removes specified user group names from the **UserGroupNames** property.</span></span><br/>                                                                                             |
| [<span data-ttu-id="2e0b9-147">**SetComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-147">**SetComputerGroupNames**</span></span>](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | <span data-ttu-id="2e0b9-148">Définit la propriété **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-148">Sets the **ComputerGroupNames** property.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="2e0b9-149">**SetCookieAuthenticationAllowed**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-149">**SetCookieAuthenticationAllowed**</span></span>](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | <span data-ttu-id="2e0b9-150">Définit la propriété **CookieAuthenticationAllowed** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-150">Sets the **CookieAuthenticationAllowed** property.</span></span><br/> <span data-ttu-id="2e0b9-151">**Windows Server 2008 :** Cette méthode n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-151">**Windows Server 2008:** This method is not available.</span></span><br/>                                                 |
| [<span data-ttu-id="2e0b9-152">**SetDeviceRedirectionType**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-152">**SetDeviceRedirectionType**</span></span>](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | <span data-ttu-id="2e0b9-153">Définit la propriété **DeviceRedirectionType** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-153">Sets the **DeviceRedirectionType** property.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="2e0b9-154">**SetEnabled**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-154">**SetEnabled**</span></span>](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | <span data-ttu-id="2e0b9-155">Active ou désactive la stratégie d’autorisation des connexions aux services Bureau à distance actuelle.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-155">Enables or disables the current RD CAP.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="2e0b9-156">**SetIdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-156">**SetIdleTimeout**</span></span>](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | <span data-ttu-id="2e0b9-157">Définit la propriété **IdleTimeout** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-157">Sets the **IdleTimeout** property.</span></span><br/> <span data-ttu-id="2e0b9-158">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-158">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                   |
| [<span data-ttu-id="2e0b9-159">**SetName**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-159">**SetName**</span></span>](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | <span data-ttu-id="2e0b9-160">Définit un nouveau nom pour cette stratégie d’autorisation des connexions aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-160">Sets a new name for this RD CAP.</span></span> <span data-ttu-id="2e0b9-161">Cette méthode garantit que les noms seront uniques.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-161">This method ensures that names will be unique.</span></span><br/>                                                                                      |
| [<span data-ttu-id="2e0b9-162">**SetPasswordAllowed**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-162">**SetPasswordAllowed**</span></span>](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="2e0b9-163">Définit la propriété **PasswordAllowed** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-163">Sets the **PasswordAllowed** property.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="2e0b9-164">**SetSecureIdAllowed**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-164">**SetSecureIdAllowed**</span></span>](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="2e0b9-165">Définit la propriété **SecureIdAllowed** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-165">Sets the **SecureIdAllowed** property.</span></span><br/> <span data-ttu-id="2e0b9-166">**Windows Server 2008 :** Cette méthode est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-166">**Windows Server 2008:** This method is reserved for future use.</span></span><br/>                                                   |
| [<span data-ttu-id="2e0b9-167">**SetSessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-167">**SetSessionTimeout**</span></span>](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="2e0b9-168">Définit les propriétés **SessionTimeout** et **SessionTimeoutAction** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-168">Sets the **SessionTimeout** and **SessionTimeoutAction** properties.</span></span><br/> <span data-ttu-id="2e0b9-169">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-169">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/> |
| [<span data-ttu-id="2e0b9-170">**SetSmartcardAllowed**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-170">**SetSmartcardAllowed**</span></span>](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | <span data-ttu-id="2e0b9-171">Définit la propriété **SmartcardAllowed** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-171">Sets the **SmartcardAllowed** property.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="2e0b9-172">**SetUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-172">**SetUserGroupNames**</span></span>](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="2e0b9-173">Définit la propriété **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-173">Sets the **UserGroupNames** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="2e0b9-174">**Mise à jour**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-174">**Update**</span></span>](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="2e0b9-175">Met à jour la stratégie d’autorisation des connexions aux services Bureau à distance actuelle.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-175">Updates the current RD CAP.</span></span><br/>                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="2e0b9-176">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2e0b9-176">Properties</span></span>

<span data-ttu-id="2e0b9-177">La classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-177">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e0b9-178">**AllowOnlySDRServers**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-178">**AllowOnlySDRServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-179">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-181">Indique si les connexions sont autorisées uniquement pour sécuriser les serveurs RDS de redirection des appareils (SDR).</span><span class="sxs-lookup"><span data-stu-id="2e0b9-181">Indicates whether connections allowed only to secure device redirection (SDR) RDS servers.</span></span> <span data-ttu-id="2e0b9-182">Cette propriété peut être définie à l’aide de la méthode [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-182">This property can be set using the [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) method.</span></span>

<span data-ttu-id="2e0b9-183">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-183">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-184">**ClipboardDisabled**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-184">**ClipboardDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-185">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-187">Indique si la redirection du presse-papiers est désactivée.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-187">Indicates if clipboard redirection will be disabled.</span></span> <span data-ttu-id="2e0b9-188">Cette propriété a un effet uniquement si la propriété **DeviceRedirectionType** a la valeur « 2 ».</span><span class="sxs-lookup"><span data-stu-id="2e0b9-188">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-189">**ComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-189">**ComputerGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-192">Liste des noms de groupes d’ordinateurs séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-192">List of semicolon-separated computer group names.</span></span> <span data-ttu-id="2e0b9-193">Cette valeur peut être vide.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-193">This value can be empty.</span></span> <span data-ttu-id="2e0b9-194">Les noms sont au format *domaine \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-194">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="2e0b9-195">Si une valeur est spécifiée, l’ordinateur client doit appartenir à l’un de ces groupes d’ordinateurs pour que l’utilisateur accède au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-195">If a value is specified, then the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-196">**CookieAuthenticationAllowed**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-196">**CookieAuthenticationAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-197">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-199">Indique si l’authentification par cookie peut être utilisée pour se connecter au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-199">Indicates if cookie authentication can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="2e0b9-200">Cette propriété peut être définie à l’aide de la méthode [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-200">This property can be set by using the [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="2e0b9-201">**Windows Server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-201">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-202">**DeviceRedirectionType**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-202">**DeviceRedirectionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-203">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-205">Spécifie les appareils qui seront redirigés.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-205">Specifies which devices will be redirected.</span></span>

<dt>

<span data-ttu-id="2e0b9-206">0</span><span class="sxs-lookup"><span data-stu-id="2e0b9-206">0</span></span>
</dt> <dd>

<span data-ttu-id="2e0b9-207">Tous les appareils seront redirigés.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-207">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-208">1</span><span class="sxs-lookup"><span data-stu-id="2e0b9-208">1</span></span>
</dt> <dd>

<span data-ttu-id="2e0b9-209">Aucun appareil n’est redirigé.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-209">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-210">2</span><span class="sxs-lookup"><span data-stu-id="2e0b9-210">2</span></span>
</dt> <dd>

<span data-ttu-id="2e0b9-211">Les appareils spécifiés ne seront pas redirigés.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-211">Specified devices will not be redirected.</span></span> <span data-ttu-id="2e0b9-212">Les propriétés **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled** et **PlugAndPlayDevicesDisabled** contrôlent les appareils qui ne seront pas redirigés.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-212">The **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled**, and **PlugAndPlayDevicesDisabled** properties control which devices will not be redirected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e0b9-213">**DiskDrivesDisabled**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-213">**DiskDrivesDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-214">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-216">Indique si la redirection de lecteur de disque est désactivée.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-216">Indicates if disk drive redirection will be disabled.</span></span> <span data-ttu-id="2e0b9-217">Cette propriété a un effet uniquement si la propriété **DeviceRedirectionType** a la valeur « 2 ».</span><span class="sxs-lookup"><span data-stu-id="2e0b9-217">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-218">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-218">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-219">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-221">Indique si cette limite d’accès aux services Bureau à distance sera utilisée pour évaluer l’autorisation d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-221">Indicates whether this RD CAP will be used to evaluate a user for authorization.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-222">**HasNapAttributes**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-222">**HasNapAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-223">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-225">Indique si les connexions aux services Bureau à distance utilisent des attributs de protection d’accès réseau (NAP).</span><span class="sxs-lookup"><span data-stu-id="2e0b9-225">Indicates if the RD CAP uses Network Access Protection (NAP) attributes.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-226">**IdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-226">**IdleTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-227">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-229">Valeur du délai d’inactivité en minutes.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-229">The idle timeout value, in minutes.</span></span> <span data-ttu-id="2e0b9-230">La valeur 0 signifie qu’il n’y a aucun délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-230">A value of 0 means there is no timeout.</span></span> <span data-ttu-id="2e0b9-231">Cette propriété peut être définie à l’aide de la méthode [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-231">This property can be set by using the [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="2e0b9-232">**Windows Server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-232">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-233">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-233">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-234">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-236">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2e0b9-236">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-237">Nom de la stratégie d’autorisation des connexions aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-237">Name of the RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-238">**Commande**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-238">**Order**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-239">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-241">Ordre d’évaluation de la stratégie d’autorisation des connexions aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-241">Evaluation order of the RD CAP.</span></span> <span data-ttu-id="2e0b9-242">La première valeur d’évaluation des connexions aux services Bureau à distance a la valeur « 1 ».</span><span class="sxs-lookup"><span data-stu-id="2e0b9-242">The first RD CAP evaluated has a value of "1".</span></span> <span data-ttu-id="2e0b9-243">La propriété **Order** peut être modifiée lors de l’appel des méthodes [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)ou [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-243">The **Order** property can be changed when the [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md), or [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-244">**PasswordAllowed**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-244">**PasswordAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-245">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-247">Indique si un mot de passe peut être utilisé pour se connecter au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-247">Indicates if a password can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="2e0b9-248">Cette propriété peut être modifiée à l’aide de la méthode [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-248">This property can be changed by using the [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-249">**PlugAndPlayDevicesDisabled**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-249">**PlugAndPlayDevicesDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-250">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-250">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-252">Indique si la redirection des appareils Plug-and-Plays est désactivée.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-252">Indicates if redirection of Plug and Play devices will be disabled.</span></span> <span data-ttu-id="2e0b9-253">Cette propriété a un effet uniquement si la propriété **DeviceRedirectionType** a la valeur « 2 ».</span><span class="sxs-lookup"><span data-stu-id="2e0b9-253">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-254">**PrintersDisabled**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-254">**PrintersDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-255">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-257">Indique si la redirection d’imprimante est désactivée.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-257">Indicates if printer redirection will be disabled.</span></span> <span data-ttu-id="2e0b9-258">Cette propriété a un effet uniquement si la propriété **DeviceRedirectionType** a la valeur « 2 ».</span><span class="sxs-lookup"><span data-stu-id="2e0b9-258">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-259">**SecureIdAllowed**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-259">**SecureIdAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-260">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-260">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-262">Indique si un identificateur sécurisé peut être utilisé pour se connecter au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-262">Indicates if a secure identifier can be used to connect to the RD Gateway server.</span></span>

<span data-ttu-id="2e0b9-263">**Windows Server 2008 :** Cette propriété n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-263">**Windows Server 2008:** This property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-264">**SerialPortsDisabled**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-264">**SerialPortsDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-265">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-266">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-267">Indique si la redirection de port série est désactivée.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-267">Indicates if serial port redirection will be disabled.</span></span> <span data-ttu-id="2e0b9-268">Cette propriété a un effet uniquement si la propriété **DeviceRedirectionType** a la valeur « 2 ».</span><span class="sxs-lookup"><span data-stu-id="2e0b9-268">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-269">**SessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-269">**SessionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-270">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-271">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-272">La valeur du délai d’expiration de session, en minutes.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-272">The session timeout value, in minutes.</span></span> <span data-ttu-id="2e0b9-273">La valeur 0 signifie qu’il n’y a aucun délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-273">A value of 0 means there is no timeout.</span></span> <span data-ttu-id="2e0b9-274">Cette propriété peut être définie à l’aide de la méthode [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-274">This property can be set by using the [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="2e0b9-275">**Windows Server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-275">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-276">**SessionTimeoutAction**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-276">**SessionTimeoutAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-277">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-277">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-279">Spécifie l’action à entreprendre dans le cas d’un délai d’expiration de session.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-279">Specifies the action to be taken in the case of a session timeout.</span></span> <span data-ttu-id="2e0b9-280">Cette propriété peut être définie à l’aide de la méthode [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-280">This property can be set by using the [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="2e0b9-281">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-281">This can be one of the following values.</span></span>

<span data-ttu-id="2e0b9-282">**Windows Server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-282">**Windows Server 2008:** This property is not available.</span></span>

<dt>

<span data-ttu-id="2e0b9-283">0</span><span class="sxs-lookup"><span data-stu-id="2e0b9-283">0</span></span>
</dt> <dd>

<span data-ttu-id="2e0b9-284">Déconnectez la session.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-284">Disconnect the session.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-285">1</span><span class="sxs-lookup"><span data-stu-id="2e0b9-285">1</span></span>
</dt> <dd>

<span data-ttu-id="2e0b9-286">Essayez de réautoriser la session.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-286">Attempt to re-authorize the session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e0b9-287">**SmartcardAllowed**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-287">**SmartcardAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-288">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-288">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-290">Indique si une carte à puce peut être utilisée pour se connecter au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-290">Indicates if a smart card can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="2e0b9-291">Cette propriété peut être modifiée à l’aide de la méthode [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="2e0b9-291">This property can be changed by using the [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="2e0b9-292">**UserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-292">**UserGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0b9-293">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e0b9-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e0b9-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0b9-295">Liste des noms de groupes d’utilisateurs séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-295">List of semicolon-separated user group names.</span></span> <span data-ttu-id="2e0b9-296">Les noms sont au format *domaine \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-296">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="2e0b9-297">Si l’utilisateur appartient à l’un de ces groupes d’utilisateurs, l’utilisateur est autorisé à accéder au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-297">If the user belongs to any of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e0b9-298">Notes</span><span class="sxs-lookup"><span data-stu-id="2e0b9-298">Remarks</span></span>

<span data-ttu-id="2e0b9-299">Pour utiliser cette classe, vous devez être membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-299">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="2e0b9-300">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="2e0b9-300">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2e0b9-301">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-301">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2e0b9-302">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-302">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2e0b9-303">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2e0b9-303">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e0b9-304">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e0b9-304">Requirements</span></span>



| <span data-ttu-id="2e0b9-305">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e0b9-305">Requirement</span></span> | <span data-ttu-id="2e0b9-306">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e0b9-306">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e0b9-307">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e0b9-307">Minimum supported client</span></span><br/> | <span data-ttu-id="2e0b9-308">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e0b9-308">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2e0b9-309">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e0b9-309">Minimum supported server</span></span><br/> | <span data-ttu-id="2e0b9-310">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e0b9-310">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2e0b9-311">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2e0b9-311">Namespace</span></span><br/>                | <span data-ttu-id="2e0b9-312">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="2e0b9-312">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2e0b9-313">MOF</span><span class="sxs-lookup"><span data-stu-id="2e0b9-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e0b9-314"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e0b9-314"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e0b9-315">DLL</span><span class="sxs-lookup"><span data-stu-id="2e0b9-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e0b9-316"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e0b9-316"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2e0b9-317">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e0b9-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e0b9-318">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-318">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="2e0b9-319">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-319">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="2e0b9-320">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-320">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="2e0b9-321">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-321">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="2e0b9-322">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-322">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="2e0b9-323">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-323">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

