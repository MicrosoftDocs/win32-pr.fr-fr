---
title: Classe Win32_TerminalServiceSetting
description: Représente la configuration d’un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 4cd047db-921f-4ccb-946b-d2c7b8d6beea
ms.tgt_platform: multiple
keywords:
- Win32_TerminalServiceSetting de la classe Services Bureau à distance
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting.Caption
- Win32_TerminalServiceSetting.Description
- Win32_TerminalServiceSetting.InstallDate
- Win32_TerminalServiceSetting.Name
- Win32_TerminalServiceSetting.Status
- Win32_TerminalServiceSetting.ServerName
- Win32_TerminalServiceSetting.TerminalServerMode
- Win32_TerminalServiceSetting.GetCapabilitiesID
- Win32_TerminalServiceSetting.LicensingType
- Win32_TerminalServiceSetting.PolicySourceLicensingType
- Win32_TerminalServiceSetting.PossibleLicensingTypes
- Win32_TerminalServiceSetting.LicensingName
- Win32_TerminalServiceSetting.LicensingDescription
- Win32_TerminalServiceSetting.ActiveDesktop
- Win32_TerminalServiceSetting.UserPermission
- Win32_TerminalServiceSetting.DeleteTempFolders
- Win32_TerminalServiceSetting.PolicySourceDeleteTempFolders
- Win32_TerminalServiceSetting.UseTempFolders
- Win32_TerminalServiceSetting.PolicySourceUseTempFolders
- Win32_TerminalServiceSetting.AllowTSConnections
- Win32_TerminalServiceSetting.PolicySourceAllowTSConnections
- Win32_TerminalServiceSetting.SingleSession
- Win32_TerminalServiceSetting.PolicySourceSingleSession
- Win32_TerminalServiceSetting.ProfilePath
- Win32_TerminalServiceSetting.PolicySourceProfilePath
- Win32_TerminalServiceSetting.HomeDirectory
- Win32_TerminalServiceSetting.PolicySourceHomeDirectory
- Win32_TerminalServiceSetting.TimeZoneRedirection
- Win32_TerminalServiceSetting.PolicySourceTimeZoneRedirection
- Win32_TerminalServiceSetting.Logons
- Win32_TerminalServiceSetting.DirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceDirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceConfiguredLicenseServers
- Win32_TerminalServiceSetting.DisableForcibleLogoff
- Win32_TerminalServiceSetting.PolicySourceDisableForcibleLogoff
- Win32_TerminalServiceSetting.FallbackPrintDriverType
- Win32_TerminalServiceSetting.PolicySourceFallbackPrintDriverType
- Win32_TerminalServiceSetting.SessionBrokerDrainMode
- Win32_TerminalServiceSetting.LimitedUserSessions
- Win32_TerminalServiceSetting.EnableDFSS
- Win32_TerminalServiceSetting.PolicySourceEnableDFSS
- Win32_TerminalServiceSetting.EnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.PolicySourceEnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.EnableAutomaticReconnection
- Win32_TerminalServiceSetting.PolicySourceEnableAutomaticReconnection
- Win32_TerminalServiceSetting.UseRDEasyPrintDriver
- Win32_TerminalServiceSetting.PolicySourceUseRDEasyPrintDriver
- Win32_TerminalServiceSetting.RedirectSmartCards
- Win32_TerminalServiceSetting.PolicySourceRedirectSmartCards
- Win32_TerminalServiceSetting.EnableDiskFSS
- Win32_TerminalServiceSetting.EnableNetworkFSS
- Win32_TerminalServiceSetting.NetworkFSSUserSessionWeight
- Win32_TerminalServiceSetting.NetworkFSSLocalSystemWeight
- Win32_TerminalServiceSetting.NetworkFSSCatchAllWeight
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f02028a331a3688152a1ce8c57ada7269d07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317422"
---
# <a name="win32_terminalservicesetting-class"></a><span data-ttu-id="c628d-105">\_Classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="c628d-105">Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="c628d-106">La classe WMI **\_ TerminalServiceSetting** WMI représente la configuration d’un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="c628d-106">The **Win32\_TerminalServiceSetting** WMI class represents the configuration for a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="c628d-107">Les paramètres incluent des fonctionnalités telles que le mode serveur hôte de session Bureau à distance, la licence, le bureau actif, les autorisations, la suppression de dossiers temporaires et les répertoires temporaires pour les sessions.</span><span class="sxs-lookup"><span data-stu-id="c628d-107">Settings include capabilities such as RD Session Host server mode, licensing, Active Desktop, permissions, deletion of temporary folders, and temporary directories for sessions.</span></span>

<span data-ttu-id="c628d-108">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="c628d-108">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="c628d-109">Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="c628d-109">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="c628d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c628d-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICESETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   ServerName;
  uint32   TerminalServerMode;
  uint32   GetCapabilitiesID;
  uint32   LicensingType;
  uint32   PolicySourceLicensingType;
  uint32   PossibleLicensingTypes;
  string   LicensingName;
  string   LicensingDescription;
  uint32   ActiveDesktop;
  uint32   UserPermission;
  uint32   DeleteTempFolders;
  uint32   PolicySourceDeleteTempFolders;
  uint32   UseTempFolders;
  uint32   PolicySourceUseTempFolders;
  uint32   AllowTSConnections;
  uint32   PolicySourceAllowTSConnections;
  uint32   SingleSession;
  uint32   PolicySourceSingleSession;
  string   ProfilePath;
  uint32   PolicySourceProfilePath;
  string   HomeDirectory;
  uint32   PolicySourceHomeDirectory;
  uint32   TimeZoneRedirection;
  uint32   PolicySourceTimeZoneRedirection;
  string   Logons;
  string   DirectConnectLicenseServers;
  uint32   PolicySourceDirectConnectLicenseServers;
  uint32   PolicySourceConfiguredLicenseServers;
  uint32   DisableForcibleLogoff;
  uint32   PolicySourceDisableForcibleLogoff;
  uint32   FallbackPrintDriverType;
  uint32   PolicySourceFallbackPrintDriverType;
  uint32   SessionBrokerDrainMode;
  uint32   LimitedUserSessions;
  uint32   EnableDFSS;
  uint32   PolicySourceEnableDFSS;
  uint32   EnableRemoteDesktopMSI;
  uint32   PolicySourceEnableRemoteDesktopMSI;
  uint32   EnableAutomaticReconnection;
  uint32   PolicySourceEnableAutomaticReconnection;
  uint32   UseRDEasyPrintDriver;
  uint32   PolicySourceUseRDEasyPrintDriver;
  uint32   RedirectSmartCards;
  uint32   PolicySourceRedirectSmartCards;
  uint32   EnableDiskFSS;
  uint32   EnableNetworkFSS;
  uint32   NetworkFSSUserSessionWeight;
  uint32   NetworkFSSLocalSystemWeight;
  uint32   NetworkFSSCatchAllWeight;
};
```

## <a name="members"></a><span data-ttu-id="c628d-111">Membres</span><span class="sxs-lookup"><span data-stu-id="c628d-111">Members</span></span>

<span data-ttu-id="c628d-112">La classe **Win32 \_ TerminalServiceSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c628d-112">The **Win32\_TerminalServiceSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="c628d-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c628d-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="c628d-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c628d-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c628d-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c628d-115">Methods</span></span>

<span data-ttu-id="c628d-116">La classe **Win32 \_ TerminalServiceSetting** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c628d-116">The **Win32\_TerminalServiceSetting** class has these methods.</span></span>



| <span data-ttu-id="c628d-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="c628d-117">Method</span></span>                                                                                                                | <span data-ttu-id="c628d-118">Description</span><span class="sxs-lookup"><span data-stu-id="c628d-118">Description</span></span>                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c628d-119">**AddDirectConnectLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="c628d-119">**AddDirectConnectLicenseServer**</span></span>](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | <span data-ttu-id="c628d-120">Configure un nouveau serveur de licences dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c628d-120">Configures a new license server in the enterprise.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="c628d-121">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="c628d-121">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | <span data-ttu-id="c628d-122">Ajoute le serveur de licences donné à la fin de la liste des serveurs de licences spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c628d-122">Adds the given license server to the end of the list of specified license servers.</span></span><br/>                                                                                  |
| [<span data-ttu-id="c628d-123">**CanAccessLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="c628d-123">**CanAccessLicenseServer**</span></span>](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | <span data-ttu-id="c628d-124">Détermine si le serveur hôte de session Bureau à distance est autorisé à demander des licences d’accès client Services Bureau à distance (CAL RDS) à partir d’un serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="c628d-124">Determines whether the RD Session Host server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from a Remote Desktop license server.</span></span><br/> |
| [<span data-ttu-id="c628d-125">**ChangeMode**</span><span class="sxs-lookup"><span data-stu-id="c628d-125">**ChangeMode**</span></span>](win32-terminalservicesetting-changemode.md)                                                         | <span data-ttu-id="c628d-126">Définit le type de licence du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="c628d-126">Sets the licensing type of the Remote Desktop license server.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="c628d-127">**CreateWinstation**</span><span class="sxs-lookup"><span data-stu-id="c628d-127">**CreateWinstation**</span></span>](createwinstation-win32-terminalservicesetting.md)                                             | <span data-ttu-id="c628d-128">Crée une pile d’écouteurs basée sur la combinaison unique du nom d’écouteur et de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="c628d-128">Creates a new listener stack based on the unique combination of listener name and NIC.</span></span><br/>                                                                              |
| [<span data-ttu-id="c628d-129">**DeleteDirectConnectLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="c628d-129">**DeleteDirectConnectLicenseServer**</span></span>](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | <span data-ttu-id="c628d-130">Supprime le serveur de licences spécifié de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c628d-130">Deletes the specified license server from the enterprise.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="c628d-131">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="c628d-131">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | <span data-ttu-id="c628d-132">Supprime tous les serveurs de licences de la liste des serveurs de licences spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c628d-132">Removes all license servers from the list of specified license servers.</span></span><br/>                                                                                             |
| [<span data-ttu-id="c628d-133">**FindLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="c628d-133">**FindLicenseServers**</span></span>](findlicenseservers-win32-terminalservicesetting.md)                                         | <span data-ttu-id="c628d-134">Énumère tous les serveurs de licences Bureau à distance et la méthode de découverte.</span><span class="sxs-lookup"><span data-stu-id="c628d-134">Enumerates all of the Remote Desktop license servers and the method of discovery.</span></span><br/>                                                                                   |
| [<span data-ttu-id="c628d-135">**GetDomain**</span><span class="sxs-lookup"><span data-stu-id="c628d-135">**GetDomain**</span></span>](getdomain-win32-terminalservicesetting.md)                                                           | <span data-ttu-id="c628d-136">Récupère le nom du domaine auquel le serveur hôte de session Bureau à distance est membre.</span><span class="sxs-lookup"><span data-stu-id="c628d-136">Retrieves the name of the domain that the RD Session Host server is a member of.</span></span><br/>                                                                                    |
| [<span data-ttu-id="c628d-137">**GetGracePeriodDays**</span><span class="sxs-lookup"><span data-stu-id="c628d-137">**GetGracePeriodDays**</span></span>](getgraceperioddays-win32-terminalservicesetting.md)                                         | <span data-ttu-id="c628d-138">Récupère le nombre de jours restants dans la période de grâce du gestionnaire de licences des services Bureau à distance pour un serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="c628d-138">Retrieves the number of days that are remaining in the RD Licensing grace period for an RD Session Host server.</span></span><br/>                                                     |
| [<span data-ttu-id="c628d-139">**GetRegisteredLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="c628d-139">**GetRegisteredLicenseServerList**</span></span>](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | <span data-ttu-id="c628d-140">Obtient la liste des serveurs de licences inscrits.</span><span class="sxs-lookup"><span data-stu-id="c628d-140">Gets the list of registered license servers.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="c628d-141">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="c628d-141">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | <span data-ttu-id="c628d-142">Récupère la liste des serveurs de licences spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c628d-142">Retrieves the list of specified license servers.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="c628d-143">**GetTSLanaIds**</span><span class="sxs-lookup"><span data-stu-id="c628d-143">**GetTSLanaIds**</span></span>](gettslanaids-win32-terminalservicesetting.md)                                                     | <span data-ttu-id="c628d-144">Obtient les ID et les descriptions de Services Bureau à distance cartes réseau.</span><span class="sxs-lookup"><span data-stu-id="c628d-144">Gets the IDs and descriptions of Remote Desktop Services network adapters.</span></span><br/>                                                                                          |
| [<span data-ttu-id="c628d-145">**GetTStoLSConnectivityStatus**</span><span class="sxs-lookup"><span data-stu-id="c628d-145">**GetTStoLSConnectivityStatus**</span></span>](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | <span data-ttu-id="c628d-146">Détermine l’état de la connectivité entre Services Bureau à distance et un serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="c628d-146">Determines the connectivity status between Remote Desktop Services and a license server.</span></span><br/>                                                                            |
| [<span data-ttu-id="c628d-147">**GetWinstationDriverNames**</span><span class="sxs-lookup"><span data-stu-id="c628d-147">**GetWinstationDriverNames**</span></span>](getwinstationdrivernames-win32-terminalservicesetting.md)                             | <span data-ttu-id="c628d-148">Récupère une liste de noms de pilote de station de noms.</span><span class="sxs-lookup"><span data-stu-id="c628d-148">Retrieves a list of Winstation driver names.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="c628d-149">**PingLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="c628d-149">**PingLicenseServer**</span></span>](pinglicenseserver-win32-terminalservicesetting.md)                                           | <span data-ttu-id="c628d-150">Exécute une commande ping sur le serveur de licences pour déterminer s’il s’agit d’un serveur de licences valide.</span><span class="sxs-lookup"><span data-stu-id="c628d-150">Pings the license server to determine whether it is a valid license server.</span></span><br/>                                                                                         |
| [<span data-ttu-id="c628d-151">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="c628d-151">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | <span data-ttu-id="c628d-152">Supprime le serveur de licences donné de la liste des serveurs de licences spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c628d-152">Removes the given license server from the list of specified license servers.</span></span><br/>                                                                                        |
| [<span data-ttu-id="c628d-153">**SetAllowTSConnections**</span><span class="sxs-lookup"><span data-stu-id="c628d-153">**SetAllowTSConnections**</span></span>](win32-terminalservicesetting-setallowtsconnections.md)                                   | <span data-ttu-id="c628d-154">Définit la propriété **AllowTSConnections** .</span><span class="sxs-lookup"><span data-stu-id="c628d-154">Sets the **AllowTSConnections** property.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="c628d-155">**SetDisableForcibleLogoff**</span><span class="sxs-lookup"><span data-stu-id="c628d-155">**SetDisableForcibleLogoff**</span></span>](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | <span data-ttu-id="c628d-156">Définit la propriété **DisableForcibleLogoff** .</span><span class="sxs-lookup"><span data-stu-id="c628d-156">Sets the **DisableForcibleLogoff** property.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="c628d-157">**SetFallbackPrintDriverType**</span><span class="sxs-lookup"><span data-stu-id="c628d-157">**SetFallbackPrintDriverType**</span></span>](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | <span data-ttu-id="c628d-158">Définit la propriété **FallbackPrintDriverType** .</span><span class="sxs-lookup"><span data-stu-id="c628d-158">Sets the **FallbackPrintDriverType** property.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="c628d-159">**SetHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="c628d-159">**SetHomeDirectory**</span></span>](win32-terminalservicesetting-sethomedirectory.md)                                             | <span data-ttu-id="c628d-160">Définit la propriété **HomeDirectory** .</span><span class="sxs-lookup"><span data-stu-id="c628d-160">Sets the **HomeDirectory** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="c628d-161">**SetPolicyPropertyName**</span><span class="sxs-lookup"><span data-stu-id="c628d-161">**SetPolicyPropertyName**</span></span>](win32-terminalservicesetting-setpolicypropertyname.md)                                   | <span data-ttu-id="c628d-162">Définit l’une des propriétés suivantes : **DeleteTempFolders** ou **UseTempFolders**.</span><span class="sxs-lookup"><span data-stu-id="c628d-162">Sets one of the following properties: **DeleteTempFolders** or **UseTempFolders**.</span></span><br/>                                                                                  |
| [<span data-ttu-id="c628d-163">**SetPrimaryLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="c628d-163">**SetPrimaryLicenseServer**</span></span>](setprimarylicenseserver-win32-terminalservicesetting.md)                               | <span data-ttu-id="c628d-164">Définit le serveur de licences donné comme première entrée de la liste des serveurs de licences spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c628d-164">Sets the given license server as the first entry in the list of specified license servers.</span></span><br/>                                                                          |
| [<span data-ttu-id="c628d-165">**SetProfilePath**</span><span class="sxs-lookup"><span data-stu-id="c628d-165">**SetProfilePath**</span></span>](win32-terminalservicesetting-setprofilepath.md)                                                 | <span data-ttu-id="c628d-166">Définit la propriété **profilePath** .</span><span class="sxs-lookup"><span data-stu-id="c628d-166">Sets the **ProfilePath** property.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="c628d-167">**SetSingleSession**</span><span class="sxs-lookup"><span data-stu-id="c628d-167">**SetSingleSession**</span></span>](win32-terminalservicesetting-setsinglesession.md)                                             | <span data-ttu-id="c628d-168">Définit la propriété **SingleSession** .</span><span class="sxs-lookup"><span data-stu-id="c628d-168">Sets the **SingleSession** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="c628d-169">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="c628d-169">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | <span data-ttu-id="c628d-170">Met à jour la liste des serveurs de licences spécifiés, en remplaçant tous les serveurs de licences spécifiés existants.</span><span class="sxs-lookup"><span data-stu-id="c628d-170">Updates the list of specified license servers, replacing any existing specified license servers.</span></span><br/>                                                                    |
| [<span data-ttu-id="c628d-171">**SetTimeZoneRedirection**</span><span class="sxs-lookup"><span data-stu-id="c628d-171">**SetTimeZoneRedirection**</span></span>](win32-terminalservicesetting-settimezoneredirection.md)                                 | <span data-ttu-id="c628d-172">Définit la propriété **TimeZoneRedirection** .</span><span class="sxs-lookup"><span data-stu-id="c628d-172">Sets the **TimeZoneRedirection** property.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="c628d-173">**UpdateDirectConnectLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="c628d-173">**UpdateDirectConnectLicenseServer**</span></span>](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | <span data-ttu-id="c628d-174">Met à jour la liste des serveurs de licences de découverte.</span><span class="sxs-lookup"><span data-stu-id="c628d-174">Updates the list of discovery license servers.</span></span><br/>                                                                                                                      |



 

### <a name="properties"></a><span data-ttu-id="c628d-175">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c628d-175">Properties</span></span>

<span data-ttu-id="c628d-176">La classe **Win32 \_ TerminalServiceSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c628d-176">The **Win32\_TerminalServiceSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c628d-177">**ActiveDesktop**</span><span class="sxs-lookup"><span data-stu-id="c628d-177">**ActiveDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-178">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-179">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c628d-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c628d-180">Spécifie si Active Desktop est autorisé dans chaque session utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c628d-180">Specifies whether Active Desktop is allowed in each user session.</span></span>

<dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="c628d-181"><span id="TRUE"></span><span id="true"></span>**True** (0)</span><span class="sxs-lookup"><span data-stu-id="c628d-181"><span id="TRUE"></span><span id="true"></span>**TRUE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-182">Active Desktop n’est pas autorisé dans chaque session utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c628d-182">Active Desktop is not allowed in each user session.</span></span>

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="c628d-183"><span id="FALSE"></span><span id="false"></span>**False** (1)</span><span class="sxs-lookup"><span data-stu-id="c628d-183"><span id="FALSE"></span><span id="false"></span>**FALSE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-184">Active Desktop est autorisé dans chaque session utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c628d-184">Active Desktop is allowed in each user session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-185">**AllowTSConnections**</span><span class="sxs-lookup"><span data-stu-id="c628d-185">**AllowTSConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-186">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-186">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-188">Spécifie si de nouvelles connexions Services Bureau à distance sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="c628d-188">Specifies whether new Remote Desktop Services connections are allowed.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="c628d-189"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="c628d-189"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-190">Les nouvelles connexions ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="c628d-190">New connections are not allowed.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="c628d-191"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="c628d-191"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-192">Les nouvelles connexions sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="c628d-192">New connections are allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-193">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c628d-193">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c628d-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c628d-196">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c628d-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c628d-197">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c628d-197">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="c628d-198">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c628d-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c628d-199">**DeleteTempFolders**</span><span class="sxs-lookup"><span data-stu-id="c628d-199">**DeleteTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-200">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-202">Spécifie si les répertoires temporaires sont supprimés à la sortie.</span><span class="sxs-lookup"><span data-stu-id="c628d-202">Specifies whether temporary directories are deleted on exit.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="c628d-203"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="c628d-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-204">La suppression des répertoires temporaires est désactivée.</span><span class="sxs-lookup"><span data-stu-id="c628d-204">Deletion of temporary directories is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="c628d-205"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="c628d-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-206">La suppression des répertoires temporaires est activée.</span><span class="sxs-lookup"><span data-stu-id="c628d-206">Deletion of temporary directories is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-207">**Description**</span><span class="sxs-lookup"><span data-stu-id="c628d-207">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c628d-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-210">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c628d-210">Description of the object.</span></span>

<span data-ttu-id="c628d-211">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c628d-211">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c628d-212">**DirectConnectLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="c628d-212">**DirectConnectLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c628d-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c628d-215">Qualificateurs : [ **déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c628d-215">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c628d-216">Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c628d-216">This property is not available.</span></span>

<span data-ttu-id="c628d-217">**Windows Server 2008 :** Énumère la liste des serveurs de licences.</span><span class="sxs-lookup"><span data-stu-id="c628d-217">**Windows Server 2008:** Enumerates the list of license servers.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-218">**DisableForcibleLogoff**</span><span class="sxs-lookup"><span data-stu-id="c628d-218">**DisableForcibleLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-219">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-219">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-221">Détermine si un administrateur connecté à la console peut être déconnecté de force.</span><span class="sxs-lookup"><span data-stu-id="c628d-221">Determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span data-ttu-id="c628d-222">0</span><span class="sxs-lookup"><span data-stu-id="c628d-222">0</span></span>
</dt> <dd>

<span data-ttu-id="c628d-223">L’administrateur peut être déconnecté de force.</span><span class="sxs-lookup"><span data-stu-id="c628d-223">Administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-224">1</span><span class="sxs-lookup"><span data-stu-id="c628d-224">1</span></span>
</dt> <dd>

<span data-ttu-id="c628d-225">L’administrateur ne peut pas être déconnecté de force.</span><span class="sxs-lookup"><span data-stu-id="c628d-225">Administrator cannot be forcibly logged off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-226">**EnableAutomaticReconnection**</span><span class="sxs-lookup"><span data-stu-id="c628d-226">**EnableAutomaticReconnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-227">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-228">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c628d-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c628d-229">Spécifie s’il faut autoriser Bureau à distance clients de connexion à se reconnecter automatiquement aux sessions sur un serveur hôte de session Bureau à distance si la liaison réseau est temporairement perdue.</span><span class="sxs-lookup"><span data-stu-id="c628d-229">Specifies whether to allow Remote Desktop connection clients to automatically reconnect to sessions on an RD Session Host server if the network link is temporarily lost.</span></span>

<dt>

<span data-ttu-id="c628d-230">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-230">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-231">La reconnexion automatique est désactivée.</span><span class="sxs-lookup"><span data-stu-id="c628d-231">Automatic reconnection is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-232">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-232">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-233">La reconnexion automatique est activée.</span><span class="sxs-lookup"><span data-stu-id="c628d-233">Automatic reconnection is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="c628d-234">**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c628d-234">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-235">**EnableDFSS**</span><span class="sxs-lookup"><span data-stu-id="c628d-235">**EnableDFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-236">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-237">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c628d-237">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c628d-238">Indique si la planification de partage de foire dynamique (DFSS) est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="c628d-238">Indicates whether dynamic fair-share scheduling (DFSS) is enabled or disabled.</span></span> <span data-ttu-id="c628d-239">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c628d-239">This can be one of the following values.</span></span>

<span data-ttu-id="c628d-240">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c628d-240">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="c628d-241">0</span><span class="sxs-lookup"><span data-stu-id="c628d-241">0</span></span>
</dt> <dd>

<span data-ttu-id="c628d-242">DFSS est désactivé.</span><span class="sxs-lookup"><span data-stu-id="c628d-242">DFSS is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-243">1</span><span class="sxs-lookup"><span data-stu-id="c628d-243">1</span></span>
</dt> <dd>

<span data-ttu-id="c628d-244">DFSS est activé.</span><span class="sxs-lookup"><span data-stu-id="c628d-244">DFSS is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-245">**EnableDiskFSS**</span><span class="sxs-lookup"><span data-stu-id="c628d-245">**EnableDiskFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-246">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-246">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-247">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c628d-247">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c628d-248">Spécifie si la planification du partage de disque est activée.</span><span class="sxs-lookup"><span data-stu-id="c628d-248">Specifies if disk fair share scheduling is enabled.</span></span>

<dt>

<span data-ttu-id="c628d-249">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-249">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-250">La planification de la répartition des disques est désactivée.</span><span class="sxs-lookup"><span data-stu-id="c628d-250">Disk fair share scheduling is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-251">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-251">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-252">La planification de la répartition des disques est activée.</span><span class="sxs-lookup"><span data-stu-id="c628d-252">Disk fair share scheduling is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="c628d-253">**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c628d-253">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-254">**EnableNetworkFSS**</span><span class="sxs-lookup"><span data-stu-id="c628d-254">**EnableNetworkFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-255">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-256">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c628d-256">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c628d-257">Spécifie si la planification de partage de la charge réseau est activée.</span><span class="sxs-lookup"><span data-stu-id="c628d-257">Specifies if network fair share scheduling is enabled.</span></span>

<dt>

<span data-ttu-id="c628d-258">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-258">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-259">La planification de la répartition des réseaux est désactivée.</span><span class="sxs-lookup"><span data-stu-id="c628d-259">Network fair share scheduling is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-260">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-260">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-261">La planification de la répartition des réseaux est activée.</span><span class="sxs-lookup"><span data-stu-id="c628d-261">Network fair share scheduling is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="c628d-262">**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c628d-262">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-263">**EnableRemoteDesktopMSI**</span><span class="sxs-lookup"><span data-stu-id="c628d-263">**EnableRemoteDesktopMSI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-264">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-265">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c628d-265">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c628d-266">Indique si le Bureau à distance MSI est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="c628d-266">Indicates whether the Remote Desktop MSI is enabled or disabled.</span></span>

<dt>

<span data-ttu-id="c628d-267">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-267">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-268">Désactivé</span><span class="sxs-lookup"><span data-stu-id="c628d-268">Disabled</span></span>

</dd> <dt>

<span data-ttu-id="c628d-269">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-269">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-270">activé</span><span class="sxs-lookup"><span data-stu-id="c628d-270">Enabled</span></span>

</dd> </dl>

<span data-ttu-id="c628d-271">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c628d-271">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-272">**FallbackPrintDriverType**</span><span class="sxs-lookup"><span data-stu-id="c628d-272">**FallbackPrintDriverType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-273">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-275">Spécifie le pilote d’imprimante à partir duquel effectuer le secours.</span><span class="sxs-lookup"><span data-stu-id="c628d-275">Specifies which printer driver to fallback to.</span></span>

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span data-ttu-id="c628d-276"><span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**Pas de dirvers de secours = 0** (0)</span><span class="sxs-lookup"><span data-stu-id="c628d-276"><span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**No fallback dirvers=0** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-277">Aucun pilote de secours.</span><span class="sxs-lookup"><span data-stu-id="c628d-277">No fallback drivers.</span></span>

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span data-ttu-id="c628d-278"><span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Meilleure estimation = 1** (1)</span><span class="sxs-lookup"><span data-stu-id="c628d-278"><span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Best guess=1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-279">Meilleure hypothèse.</span><span class="sxs-lookup"><span data-stu-id="c628d-279">Best guess.</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span data-ttu-id="c628d-280"><span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Meilleure hypothèse, si aucune correspondance n’est trouvée dans PCL = 2** (2)</span><span class="sxs-lookup"><span data-stu-id="c628d-280"><span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Best guess, if no match is found fallback to PCL=2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-281">Meilleure hypothèse.</span><span class="sxs-lookup"><span data-stu-id="c628d-281">Best guess.</span></span> <span data-ttu-id="c628d-282">Si aucune correspondance n’est trouvée, vous pouvez revenir à Hewlett-Packard PCL (Printer Control Language).</span><span class="sxs-lookup"><span data-stu-id="c628d-282">If no match is found, fallback to Hewlett-Packard Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span data-ttu-id="c628d-283"><span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Meilleure hypothèse, si aucune correspondance n’est trouvée, de secours pour PS = 3** (3)</span><span class="sxs-lookup"><span data-stu-id="c628d-283"><span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Best guess, if no match is found fallback to PS=3** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-284">Meilleure hypothèse.</span><span class="sxs-lookup"><span data-stu-id="c628d-284">Best guess.</span></span> <span data-ttu-id="c628d-285">Si aucune correspondance n’est trouvée, basculez vers PostScript (PS).</span><span class="sxs-lookup"><span data-stu-id="c628d-285">If no match is found, fallback to Postscript (PS).</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span data-ttu-id="c628d-286"><span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Meilleure hypothèse, si aucune correspondance n’est trouvée, afficher les pilotes PCL et PS = 4** (4)</span><span class="sxs-lookup"><span data-stu-id="c628d-286"><span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Best guess, if no match is found show both PCL and PS drivers=4** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-287">Meilleure hypothèse.</span><span class="sxs-lookup"><span data-stu-id="c628d-287">Best guess.</span></span> <span data-ttu-id="c628d-288">Si aucune correspondance n’est trouvée, affichez les pilotes PS et PCL.</span><span class="sxs-lookup"><span data-stu-id="c628d-288">If no match is found, show both PS and PCL drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-289">**GetCapabilitiesID**</span><span class="sxs-lookup"><span data-stu-id="c628d-289">**GetCapabilitiesID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-290">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-292">ID des capacités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c628d-292">Capabilities ID for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-293">**HomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="c628d-293">**HomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-294">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c628d-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-296">Répertoire racine de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c628d-296">The root directory for the computer.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-297">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c628d-297">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-298">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c628d-298">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c628d-300">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="c628d-300">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="c628d-301">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="c628d-301">The date the object was installed.</span></span> <span data-ttu-id="c628d-302">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="c628d-302">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c628d-303">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c628d-303">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c628d-304">**LicensingDescription**</span><span class="sxs-lookup"><span data-stu-id="c628d-304">**LicensingDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-305">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c628d-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-307">Brève description du mode de licence.</span><span class="sxs-lookup"><span data-stu-id="c628d-307">A brief description of the licensing mode.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-308">**LicensingName**</span><span class="sxs-lookup"><span data-stu-id="c628d-308">**LicensingName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-309">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c628d-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-311">Nom du mode de licence.</span><span class="sxs-lookup"><span data-stu-id="c628d-311">The name of the licensing mode.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-312">**LicensingType**</span><span class="sxs-lookup"><span data-stu-id="c628d-312">**LicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-313">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-315">Type de licence pour le mode serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="c628d-315">The licensing type for the specified server mode.</span></span>

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span data-ttu-id="c628d-316"><span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Terminal Server personnel** (0)</span><span class="sxs-lookup"><span data-stu-id="c628d-316"><span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Personal Terminal Server** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-317">Serveur hôte de session Bureau à distance personnel.</span><span class="sxs-lookup"><span data-stu-id="c628d-317">Personal RD Session Host server.</span></span>

</dd> <dt>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>

<span data-ttu-id="c628d-318"><span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Bureau à distance pour administration** (1)</span><span class="sxs-lookup"><span data-stu-id="c628d-318"><span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Remote Desktop for Administration** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-319">Bureau à distance pour l’administration.</span><span class="sxs-lookup"><span data-stu-id="c628d-319">Remote Desktop for Administration.</span></span>

</dd> <dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span data-ttu-id="c628d-320"><span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Par appareil** (2)</span><span class="sxs-lookup"><span data-stu-id="c628d-320"><span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Per Device** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-321">Par appareil.</span><span class="sxs-lookup"><span data-stu-id="c628d-321">Per Device.</span></span> <span data-ttu-id="c628d-322">Valide pour les serveurs d’applications.</span><span class="sxs-lookup"><span data-stu-id="c628d-322">Valid for application servers.</span></span>

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="c628d-323"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Par utilisateur** (3)</span><span class="sxs-lookup"><span data-stu-id="c628d-323"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-324">Par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c628d-324">Per User.</span></span> <span data-ttu-id="c628d-325">Valide pour les serveurs d’applications.</span><span class="sxs-lookup"><span data-stu-id="c628d-325">Valid for application servers.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c628d-326"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (4)</span><span class="sxs-lookup"><span data-stu-id="c628d-326"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-327">Non configuré.</span><span class="sxs-lookup"><span data-stu-id="c628d-327">Not Configured.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-328">**LimitedUserSessions**</span><span class="sxs-lookup"><span data-stu-id="c628d-328">**LimitedUserSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-329">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-330">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c628d-330">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c628d-331">Indique si la fonctionnalité permettant de limiter le nombre de sessions actives et inactives autorisées sur un serveur hôte de session Bureau à distance est activée.</span><span class="sxs-lookup"><span data-stu-id="c628d-331">Indicates whether the feature to limit the number of both active and inactive sessions that are allowed on an RD Session Host server is enabled.</span></span> <span data-ttu-id="c628d-332">Par exemple, vous souhaiterez peut-être définir **LimitedUserSessions** pour garantir la conformité de licence pour une application particulière installée sur le serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="c628d-332">For example, you may want to set **LimitedUserSessions** to guarantee license compliance for a particular application that is installed on the RD Session Host server.</span></span> <span data-ttu-id="c628d-333">Ou bien, vous souhaiterez peut-être limiter le nombre maximal de sessions sur un serveur hôte de session Bureau à distance dans une batterie de serveurs à charge équilibrée afin que le serveur ne soit pas surchargé en cas d’échec d’un autre serveur de la batterie.</span><span class="sxs-lookup"><span data-stu-id="c628d-333">Or, you may want to limit the maximum number of sessions on an RD Session Host server in a load-balanced farm so that the server will not be overloaded if another server in the farm fails.</span></span>

> [!Note]
>
> <span data-ttu-id="c628d-334">La session utilisée pour se connecter au serveur à des fins d’administration n’est pas affectée par **LimitedUserSessions**.</span><span class="sxs-lookup"><span data-stu-id="c628d-334">The session that is used to connect to the server for administrative purposes is not affected by **LimitedUserSessions**.</span></span>
>
> <span data-ttu-id="c628d-335">Dans une batterie de serveurs hôte de session Bureau à distance, si un utilisateur dépasse la limite de session, la session est dirigée vers un autre serveur par l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="c628d-335">In an RD Session Host server farm, if a user exceeds the session limit, the session will be directed to another server by RD Connection Broker load balancing.</span></span> <span data-ttu-id="c628d-336">Si le serveur est un serveur autonome, l’utilisateur ne sera pas en mesure de se connecter.</span><span class="sxs-lookup"><span data-stu-id="c628d-336">If the server is a stand-alone server, the user will not be able to connect.</span></span>
>
> <span data-ttu-id="c628d-337">En raison de la session utilisée pour se connecter au serveur à des fins administratives et de la synchronisation du nombre de sessions pendant le cycle d’ouverture de session, il est recommandé de définir **LimitedUserSessions** sur une valeur légèrement inférieure à la limite physique du nombre de sessions sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="c628d-337">Because of the session that is used to connect to the server for administrative purposes, and the timing of the enforcement of the number of sessions during the logon cycle, it is recommended that you set **LimitedUserSessions** to a value that is slightly lower that the physical limit for the number of sessions on a server.</span></span>
>
> <span data-ttu-id="c628d-338">La propriété **LimitedUserSessions** est valide uniquement si le service de rôle hôte de session Bureau à distance est installé.</span><span class="sxs-lookup"><span data-stu-id="c628d-338">The **LimitedUserSessions** property is only valid if the RD Session Host role service is installed.</span></span>

 

<dt>

<span data-ttu-id="c628d-339">0</span><span class="sxs-lookup"><span data-stu-id="c628d-339">0</span></span>
</dt> <dd>

<span data-ttu-id="c628d-340">La fonctionnalité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="c628d-340">The feature is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-341">1 ou plus</span><span class="sxs-lookup"><span data-stu-id="c628d-341">1 or greater</span></span>
</dt> <dd>

<span data-ttu-id="c628d-342">Une valeur supérieure ou égale au nombre maximal de sessions (actives et inactives) autorisées sur le serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="c628d-342">A value of one or greater represents the maximum number of sessions (both active and inactive) that are allowed on the RD Session Host server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-343">**Ouvertures**</span><span class="sxs-lookup"><span data-stu-id="c628d-343">**Logons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-344">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c628d-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-345">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c628d-345">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c628d-346">Spécifie si les nouvelles sessions sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="c628d-346">Specifies whether new sessions are allowed.</span></span> <span data-ttu-id="c628d-347">Ce paramètre n’affecte pas les paramètres existants.</span><span class="sxs-lookup"><span data-stu-id="c628d-347">This setting does not affect existing settings.</span></span>

<dt>

<span data-ttu-id="c628d-348">0</span><span class="sxs-lookup"><span data-stu-id="c628d-348">0</span></span>
</dt> <dd>

<span data-ttu-id="c628d-349">Les nouvelles sessions sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="c628d-349">New sessions are allowed.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-350">1</span><span class="sxs-lookup"><span data-stu-id="c628d-350">1</span></span>
</dt> <dd>

<span data-ttu-id="c628d-351">Les nouvelles sessions ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="c628d-351">New sessions are not allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-352">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c628d-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-353">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c628d-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-355">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="c628d-355">The name of the object.</span></span>

<span data-ttu-id="c628d-356">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c628d-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c628d-357">**NetworkFSSCatchAllWeight**</span><span class="sxs-lookup"><span data-stu-id="c628d-357">**NetworkFSSCatchAllWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-358">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-359">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c628d-359">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c628d-360">Spécifie le poids de partage de la charge réseau par défaut pour le trafic réseau de rattrapage.</span><span class="sxs-lookup"><span data-stu-id="c628d-360">Specifies the default network fair share weight for catch-all network traffic.</span></span> <span data-ttu-id="c628d-361">Les valeurs valides sont comprises entre 1 et 9.</span><span class="sxs-lookup"><span data-stu-id="c628d-361">Valid values are 1 to 9.</span></span>

<span data-ttu-id="c628d-362">**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c628d-362">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-363">**NetworkFSSLocalSystemWeight**</span><span class="sxs-lookup"><span data-stu-id="c628d-363">**NetworkFSSLocalSystemWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-364">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-364">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-365">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c628d-365">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c628d-366">Spécifie le poids de partage de la charge réseau par défaut pour un processus de système local.</span><span class="sxs-lookup"><span data-stu-id="c628d-366">Specifies the default network fair share weight for a local system processes.</span></span> <span data-ttu-id="c628d-367">Les valeurs valides sont comprises entre 1 et 9.</span><span class="sxs-lookup"><span data-stu-id="c628d-367">Valid values are 1 to 9.</span></span>

<span data-ttu-id="c628d-368">**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c628d-368">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-369">**NetworkFSSUserSessionWeight**</span><span class="sxs-lookup"><span data-stu-id="c628d-369">**NetworkFSSUserSessionWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-370">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-371">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c628d-371">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c628d-372">Spécifie le poids de partage de la charge réseau par défaut pour une session utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c628d-372">Specifies the default network fair share weight for a user session.</span></span> <span data-ttu-id="c628d-373">Les valeurs valides sont comprises entre 1 et 9.</span><span class="sxs-lookup"><span data-stu-id="c628d-373">Valid values are 1 to 9.</span></span>

<span data-ttu-id="c628d-374">**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c628d-374">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-375">**PolicySourceAllowTSConnections**</span><span class="sxs-lookup"><span data-stu-id="c628d-375">**PolicySourceAllowTSConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-376">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-376">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-378">Indique si la propriété **AllowTSConnections** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-378">Indicates whether the **AllowTSConnections** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c628d-379">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-379">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-380">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-380">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-381">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-381">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-382">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-382">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-383">**PolicySourceConfiguredLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="c628d-383">**PolicySourceConfiguredLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-384">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-384">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-385">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-386">Indique si les serveurs de licences retournés par la méthode [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) sont configurés par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-386">Indicates whether the license servers returned by the [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) method are configured by the server or by group policy.</span></span>

<span data-ttu-id="c628d-387">**Windows Server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c628d-387">**Windows Server 2008:** This property is not available.</span></span>

<dt>

<span data-ttu-id="c628d-388">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-388">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-389">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-389">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-390">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-390">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-391">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-391">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-392">**PolicySourceDeleteTempFolders**</span><span class="sxs-lookup"><span data-stu-id="c628d-392">**PolicySourceDeleteTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-393">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-393">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-395">Indique si la propriété **DeleteTempFolders** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-395">Indicates whether the **DeleteTempFolders** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c628d-396">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-396">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-397">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-397">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-398">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-398">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-399">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-399">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-400">**PolicySourceDirectConnectLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="c628d-400">**PolicySourceDirectConnectLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-401">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-401">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c628d-403">Qualificateurs : [ **déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c628d-403">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c628d-404">Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c628d-404">This property is not available.</span></span>

<span data-ttu-id="c628d-405">**Windows Server 2008 :** Indique si la propriété **DirectConnectLicenseServers** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-405">**Windows Server 2008:** Indicates whether the **DirectConnectLicenseServers** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c628d-406">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-406">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-407">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-407">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-408">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-408">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-409">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-409">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-410">**PolicySourceDisableForcibleLogoff**</span><span class="sxs-lookup"><span data-stu-id="c628d-410">**PolicySourceDisableForcibleLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-411">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-412">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-413">Cette propriété n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c628d-413">This property is not supported.</span></span>

<span data-ttu-id="c628d-414">**Windows Server 2008 :** Détermine si la propriété **DisableForcibleLogoff** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-414">**Windows Server 2008:** Determines whether the **DisableForcibleLogoff** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c628d-415">0</span><span class="sxs-lookup"><span data-stu-id="c628d-415">0</span></span>
</dt> <dd>

<span data-ttu-id="c628d-416">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-416">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-417">1</span><span class="sxs-lookup"><span data-stu-id="c628d-417">1</span></span>
</dt> <dd>

<span data-ttu-id="c628d-418">Stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-418">Group Policy.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-419">**PolicySourceEnableAutomaticReconnection**</span><span class="sxs-lookup"><span data-stu-id="c628d-419">**PolicySourceEnableAutomaticReconnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-420">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-420">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-422">Indique si la propriété **EnableAutomaticReconnection** est configurée par le serveur ou la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-422">Indicates whether the **EnableAutomaticReconnection** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="c628d-423">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-423">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-424">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-424">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-425">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-425">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-426">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-426">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="c628d-427">**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c628d-427">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-428">**PolicySourceEnableDFSS**</span><span class="sxs-lookup"><span data-stu-id="c628d-428">**PolicySourceEnableDFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-429">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-431">Indique si la propriété **EnableDFSS** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-431">Indicates whether the **EnableDFSS** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c628d-432">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-432">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-433">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-433">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-434">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-434">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-435">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-435">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="c628d-436">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c628d-436">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-437">**PolicySourceEnableRemoteDesktopMSI**</span><span class="sxs-lookup"><span data-stu-id="c628d-437">**PolicySourceEnableRemoteDesktopMSI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-438">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-439">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-440">Indique si la propriété **EnableRemoteDesktopMSI** est configurée par le serveur ou la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-440">Indicates whether the **EnableRemoteDesktopMSI** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="c628d-441">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-441">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-442">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-442">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-443">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-443">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-444">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-444">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="c628d-445">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c628d-445">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-446">**PolicySourceFallbackPrintDriverType**</span><span class="sxs-lookup"><span data-stu-id="c628d-446">**PolicySourceFallbackPrintDriverType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-447">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-447">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-448">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-449">Indique si la propriété **FallbackPrintDriverType** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-449">Indicates whether the **FallbackPrintDriverType** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c628d-450">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-450">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-451">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-451">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-452">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-452">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-453">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-453">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-454">**PolicySourceHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="c628d-454">**PolicySourceHomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-455">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-455">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-456">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-457">Indique si la propriété **HomeDirectory** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-457">Indicates whether the **HomeDirectory** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c628d-458">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-458">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-459">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-459">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-460">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-460">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-461">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-461">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-462">**PolicySourceLicensingType**</span><span class="sxs-lookup"><span data-stu-id="c628d-462">**PolicySourceLicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-463">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-463">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-464">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-465">Indique si la propriété **LicensingType** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-465">Indicates whether the **LicensingType** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c628d-466">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-466">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-467">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-467">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-468">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-468">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-469">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-469">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-470">**PolicySourceProfilePath**</span><span class="sxs-lookup"><span data-stu-id="c628d-470">**PolicySourceProfilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-471">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-472">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-473">Indique si la propriété **profilePath** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-473">Indicates whether the **ProfilePath** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c628d-474">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-474">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-475">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-475">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-476">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-476">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-477">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-477">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-478">**PolicySourceRedirectSmartCards**</span><span class="sxs-lookup"><span data-stu-id="c628d-478">**PolicySourceRedirectSmartCards**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-479">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-479">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-480">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-481">Indique si la propriété **RedirectSmartCards** est configurée par le serveur ou la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-481">Indicates whether the **RedirectSmartCards** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="c628d-482">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-482">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-483">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-483">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-484">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-484">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-485">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-485">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="c628d-486">**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c628d-486">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-487">**PolicySourceSingleSession**</span><span class="sxs-lookup"><span data-stu-id="c628d-487">**PolicySourceSingleSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-488">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-489">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-490">Indique si la propriété **SingleSession** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-490">Indicates whether the property **SingleSession** is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c628d-491">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-491">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-492">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-492">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-493">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-493">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-494">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-494">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-495">**PolicySourceTimeZoneRedirection**</span><span class="sxs-lookup"><span data-stu-id="c628d-495">**PolicySourceTimeZoneRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-496">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-497">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-498">Indique si la propriété **TimeZoneRedirection** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-498">Indicates whether the property **TimeZoneRedirection** is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c628d-499">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-499">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-500">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-500">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-501">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-501">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-502">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-502">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-503">**PolicySourceUseRDEasyPrintDriver**</span><span class="sxs-lookup"><span data-stu-id="c628d-503">**PolicySourceUseRDEasyPrintDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-504">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-504">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-505">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-506">Indique si la propriété **UseRDEasyPrintDriver** est configurée par le serveur ou la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-506">Indicates whether the **UseRDEasyPrintDriver** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="c628d-507">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-507">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-508">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-508">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-509">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-509">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-510">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-510">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="c628d-511">**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c628d-511">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-512">**PolicySourceUseTempFolders**</span><span class="sxs-lookup"><span data-stu-id="c628d-512">**PolicySourceUseTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-513">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-513">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-514">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-515">Indique si la propriété **UseTempFolders** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c628d-515">Indicates whether the **UseTempFolders** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c628d-516">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-516">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-517">Serveur</span><span class="sxs-lookup"><span data-stu-id="c628d-517">Server</span></span>

</dd> <dt>

<span data-ttu-id="c628d-518">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-518">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-519">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c628d-519">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-520">**PossibleLicensingTypes**</span><span class="sxs-lookup"><span data-stu-id="c628d-520">**PossibleLicensingTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-521">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-521">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-522">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c628d-523">Qualificateurs : [**bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), deux- [**tvalue**](/windows/desktop/WmiSdk/standard-qualifiers) ("Terminal Server personnel", "Bureau à distance pour l’administration", "par appareil", "par utilisateur", "non configuré")</span><span class="sxs-lookup"><span data-stu-id="c628d-523">Qualifiers: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("Personal Terminal Server", "Remote Desktop for Administration", "Per Device", "Per User", "Not Configured")</span></span>
</dt> </dl>

<span data-ttu-id="c628d-524">Masque de masque qui spécifie les types de licences disponibles.</span><span class="sxs-lookup"><span data-stu-id="c628d-524">A bitmask that specifies the licensing types that are available.</span></span> <span data-ttu-id="c628d-525">Il peut s’agir d’une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c628d-525">This can be a combination of one or more of the following values.</span></span>

<dt>

<span data-ttu-id="c628d-526">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-526">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-527">Les licences de serveur hôte de session Bureau à distance personnelles sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c628d-527">Personal RD Session Host server licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-528">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="c628d-528">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-529">Les licences Bureau à distance sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c628d-529">Remote Desktop licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-530">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="c628d-530">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-531">Les licences par périphérique sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c628d-531">Per device licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-532">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="c628d-532">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-533">Les licences par utilisateur sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c628d-533">Per user licenses are supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-534">**ProfilePath**</span><span class="sxs-lookup"><span data-stu-id="c628d-534">**ProfilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-535">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c628d-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-536">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-537">Chemin du profil de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c628d-537">Profile path for the computer.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-538">**RedirectSmartCards**</span><span class="sxs-lookup"><span data-stu-id="c628d-538">**RedirectSmartCards**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-539">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-539">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-540">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c628d-540">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c628d-541">Spécifie si la redirection des périphériques de carte à puce est autorisée dans une session à distance.</span><span class="sxs-lookup"><span data-stu-id="c628d-541">Specifies if redirection of smart card devices is allowed in a remote session.</span></span>

<dt>

<span data-ttu-id="c628d-542">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c628d-542">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-543">La redirection de périphérique de carte à puce n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="c628d-543">Smart card device redirection is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-544">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c628d-544">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c628d-545">La redirection de périphérique de carte à puce est autorisée.</span><span class="sxs-lookup"><span data-stu-id="c628d-545">Smart card device redirection is allowed.</span></span>

</dd> </dl>

<span data-ttu-id="c628d-546">**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c628d-546">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-547">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="c628d-547">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-548">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c628d-548">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-549">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c628d-550">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c628d-550">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c628d-551">Nom du serveur hôte de session Bureau à distance dont les propriétés sont intéressantes.</span><span class="sxs-lookup"><span data-stu-id="c628d-551">Name of the RD Session Host server whose properties are of interest.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-552">**SessionBrokerDrainMode**</span><span class="sxs-lookup"><span data-stu-id="c628d-552">**SessionBrokerDrainMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-553">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-553">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-554">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c628d-554">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c628d-555">Le mode de connexion de l’utilisateur du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="c628d-555">The RD Connection Broker user logon mode.</span></span>

<dt>

<span data-ttu-id="c628d-556">0</span><span class="sxs-lookup"><span data-stu-id="c628d-556">0</span></span>
</dt> <dd>

<span data-ttu-id="c628d-557">Autoriser toutes les connexions.</span><span class="sxs-lookup"><span data-stu-id="c628d-557">Allow all connections.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-558">1</span><span class="sxs-lookup"><span data-stu-id="c628d-558">1</span></span>
</dt> <dd>

<span data-ttu-id="c628d-559">Autoriser les reconnexions, mais empêcher les nouvelles ouvertures de session jusqu’à ce que le serveur soit redémarré.</span><span class="sxs-lookup"><span data-stu-id="c628d-559">Allow reconnections, but prevent new logons until the server is restarted.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-560">2</span><span class="sxs-lookup"><span data-stu-id="c628d-560">2</span></span>
</dt> <dd>

<span data-ttu-id="c628d-561">Autoriser les reconnexions, mais empêcher les nouvelles ouvertures de session.</span><span class="sxs-lookup"><span data-stu-id="c628d-561">Allow reconnections, but prevent new logons.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-562">**SingleSession**</span><span class="sxs-lookup"><span data-stu-id="c628d-562">**SingleSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-563">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-563">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-564">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-564">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-565">Spécifie si une ou plusieurs sessions Services Bureau à distance sont autorisées par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c628d-565">Specifies whether one or more Remote Desktop Services sessions are allowed per user.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="c628d-566"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="c628d-566"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-567">Plusieurs sessions sont autorisées par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c628d-567">More than one session is allowed per user.</span></span>

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="c628d-568"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="c628d-568"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-569">Une seule session est autorisée par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c628d-569">Only one session is allowed per user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-570">**État**</span><span class="sxs-lookup"><span data-stu-id="c628d-570">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-571">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c628d-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-572">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c628d-573">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="c628d-573">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="c628d-574">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c628d-574">Current status of the object.</span></span> <span data-ttu-id="c628d-575">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="c628d-575">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c628d-576">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="c628d-576">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c628d-577">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="c628d-577">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c628d-578">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="c628d-578">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c628d-579">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="c628d-579">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c628d-580">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c628d-580">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="c628d-581">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="c628d-581">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c628d-582">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="c628d-582">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c628d-583">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="c628d-583">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c628d-584">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="c628d-584">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c628d-585">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="c628d-585">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c628d-586">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="c628d-586">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c628d-587">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="c628d-587">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c628d-588">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="c628d-588">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-589">**TerminalServerMode**</span><span class="sxs-lookup"><span data-stu-id="c628d-589">**TerminalServerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-590">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-590">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-591">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-592">Mode de fonctionnement du serveur hôte de session Bureau à distance du service Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="c628d-592">The RD Session Host server operating mode of the Remote Desktop Services service.</span></span> <span data-ttu-id="c628d-593">Ce mode contrôle les stratégies de licence applicables, et indique si les fonctionnalités de compatibilité des applications sont activées.</span><span class="sxs-lookup"><span data-stu-id="c628d-593">This mode controls the licensing policies that are applicable as well as whether application-compatibility features are enabled.</span></span>

<dt>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>

<span data-ttu-id="c628d-594"><span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)</span><span class="sxs-lookup"><span data-stu-id="c628d-594"><span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-595">Le serveur fonctionne comme un serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="c628d-595">The server operates as an application server.</span></span>

</dd> <dt>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>

<span data-ttu-id="c628d-596"><span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)</span><span class="sxs-lookup"><span data-stu-id="c628d-596"><span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-597">La session est administrée à distance.</span><span class="sxs-lookup"><span data-stu-id="c628d-597">The session is administered remotely.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-598">**TimeZoneRedirection**</span><span class="sxs-lookup"><span data-stu-id="c628d-598">**TimeZoneRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-599">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-599">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-600">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-600">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-601">Spécifie si l’ordinateur client peut rediriger ses paramètres de fuseau horaire vers la session Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="c628d-601">Specifies whether the client computer can redirect its time zone settings to the Remote Desktop Services session.</span></span>

<dt>

<span data-ttu-id="c628d-602">0</span><span class="sxs-lookup"><span data-stu-id="c628d-602">0</span></span>
</dt> <dd>

<span data-ttu-id="c628d-603">La redirection est désactivée.</span><span class="sxs-lookup"><span data-stu-id="c628d-603">Redirection is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-604">1</span><span class="sxs-lookup"><span data-stu-id="c628d-604">1</span></span>
</dt> <dd>

<span data-ttu-id="c628d-605">La redirection est activée.</span><span class="sxs-lookup"><span data-stu-id="c628d-605">Redirection is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-606">**UseRDEasyPrintDriver**</span><span class="sxs-lookup"><span data-stu-id="c628d-606">**UseRDEasyPrintDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-607">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-607">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-608">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c628d-608">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c628d-609">Spécifie si le pilote d’imprimante pilote Easy Print pour les services Bureau à distance est utilisé en premier pour installer toutes les imprimantes du client.</span><span class="sxs-lookup"><span data-stu-id="c628d-609">Specifies whether the Remote Desktop Easy Print printer driver is used first to install all client printers.</span></span>

<dt>

<span data-ttu-id="c628d-610">0</span><span class="sxs-lookup"><span data-stu-id="c628d-610">0</span></span>
</dt> <dd>

<span data-ttu-id="c628d-611">Le serveur hôte de session Bureau à distance tente de trouver un pilote d’imprimante approprié pour installer l’imprimante cliente.</span><span class="sxs-lookup"><span data-stu-id="c628d-611">The RD Session Host server tries to find a suitable printer driver to install the client printer.</span></span> <span data-ttu-id="c628d-612">Si le serveur hôte de session Bureau à distance n’a pas de pilote d’imprimante qui correspond à l’imprimante cliente, le serveur tente d’utiliser le pilote pilote Easy Print pour les services Bureau à distance pour installer l’imprimante cliente.</span><span class="sxs-lookup"><span data-stu-id="c628d-612">If the RD Session Host server does not have a printer driver that matches the client printer, the server tries to use the Remote Desktop Easy Print driver to install the client printer.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-613">1</span><span class="sxs-lookup"><span data-stu-id="c628d-613">1</span></span>
</dt> <dd>

<span data-ttu-id="c628d-614">Le serveur hôte de session Bureau à distance tente d’abord d’utiliser le pilote d’imprimante pilote Easy Print pour les services Bureau à distance pour installer toutes les imprimantes clientes.</span><span class="sxs-lookup"><span data-stu-id="c628d-614">The RD Session Host server first tries to use the Remote Desktop Easy Print printer driver to install all client printers.</span></span> <span data-ttu-id="c628d-615">Si, pour une raison quelconque, le pilote d’imprimante pilote Easy Print pour les services Bureau à distance ne peut pas être utilisé, un pilote d’imprimante sur le serveur hôte de session Bureau à distance qui correspond à l’imprimante cliente est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c628d-615">If for any reason the Remote Desktop Easy Print printer driver cannot be used, a printer driver on the RD Session Host server that matches the client printer is used.</span></span>

</dd> </dl>

<span data-ttu-id="c628d-616">**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c628d-616">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="c628d-617">**UserPermission**</span><span class="sxs-lookup"><span data-stu-id="c628d-617">**UserPermission**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-618">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-618">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-619">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c628d-619">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c628d-620">Spécifie si chaque session utilisateur a une sécurité stricte ou souple.</span><span class="sxs-lookup"><span data-stu-id="c628d-620">Specifies if each user session has tight or relaxed security.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="c628d-621"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="c628d-621"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-622">La sécurité est parfaite.</span><span class="sxs-lookup"><span data-stu-id="c628d-622">Security is tight.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="c628d-623"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="c628d-623"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-624">La sécurité est assouplie.</span><span class="sxs-lookup"><span data-stu-id="c628d-624">Security is relaxed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c628d-625">**UseTempFolders**</span><span class="sxs-lookup"><span data-stu-id="c628d-625">**UseTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c628d-626">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c628d-626">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c628d-627">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c628d-627">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c628d-628">Spécifie si les répertoires temporaires sont créés et supprimés pour chaque session.</span><span class="sxs-lookup"><span data-stu-id="c628d-628">Specifies whether temporary directories are created and deleted on a per-session basis.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="c628d-629"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="c628d-629"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-630">Les répertoires temporaires ne sont pas créés et supprimés pour chaque session.</span><span class="sxs-lookup"><span data-stu-id="c628d-630">Temporary directories are not created and deleted for each session.</span></span> <span data-ttu-id="c628d-631">Un est créé pour la première session et jamais supprimé.</span><span class="sxs-lookup"><span data-stu-id="c628d-631">One is created for the first session and never deleted.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="c628d-632"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="c628d-632"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c628d-633">Des répertoires temporaires sont créés et supprimés pour chaque session.</span><span class="sxs-lookup"><span data-stu-id="c628d-633">Temporary directories are created and deleted for each session.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c628d-634">Notes</span><span class="sxs-lookup"><span data-stu-id="c628d-634">Remarks</span></span>

<span data-ttu-id="c628d-635">**Win32 \_ TerminalServiceSetting** est associé à [**Win32 \_ TerminalService**](win32-terminalservice.md) en tant que propriété de **paramètre** de l’Association [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="c628d-635">**Win32\_TerminalServiceSetting** is associated to [**Win32\_TerminalService**](win32-terminalservice.md) as the **Setting** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="c628d-636">[**Win32 \_ TerminalSetting**](win32-terminalsetting.md) est associé au [**\_ Terminal Win32**](win32-terminal.md) en tant que propriété de **paramètre** de l’Association [**Win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="c628d-636">[**Win32\_TerminalSetting**](win32-terminalsetting.md) is associated to [**Win32\_Terminal**](win32-terminal.md) as the **Setting** property of the [**Win32\_TerminalTerminalSetting**](win32-terminalterminalsetting.md) association.</span></span>

<span data-ttu-id="c628d-637">Pour se connecter à l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="c628d-637">To connect to the Root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="c628d-638">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="c628d-638">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="c628d-639">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de six.</span><span class="sxs-lookup"><span data-stu-id="c628d-639">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="c628d-640">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="c628d-640">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="c628d-641">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c628d-641">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c628d-642">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c628d-642">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c628d-643">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c628d-643">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c628d-644">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c628d-644">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c628d-645">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c628d-645">Requirements</span></span>



| <span data-ttu-id="c628d-646">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c628d-646">Requirement</span></span> | <span data-ttu-id="c628d-647">Valeur</span><span class="sxs-lookup"><span data-stu-id="c628d-647">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c628d-648">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c628d-648">Minimum supported client</span></span><br/> | <span data-ttu-id="c628d-649">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c628d-649">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c628d-650">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c628d-650">Minimum supported server</span></span><br/> | <span data-ttu-id="c628d-651">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c628d-651">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c628d-652">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c628d-652">Namespace</span></span><br/>                | <span data-ttu-id="c628d-653">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="c628d-653">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c628d-654">MOF</span><span class="sxs-lookup"><span data-stu-id="c628d-654">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c628d-655"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c628d-655"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c628d-656">DLL</span><span class="sxs-lookup"><span data-stu-id="c628d-656">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c628d-657"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c628d-657"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c628d-658">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c628d-658">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c628d-659">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="c628d-659">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="c628d-660">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="c628d-660">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="c628d-661">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="c628d-661">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="c628d-662">**\_TerminalServiceToSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="c628d-662">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dt>

[<span data-ttu-id="c628d-663">**\_TerminalTerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="c628d-663">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> <dt>

[<span data-ttu-id="c628d-664">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="c628d-664">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

