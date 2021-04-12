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
# <a name="win32_terminalservicesetting-class"></a>\_Classe TerminalServiceSetting Win32

La classe WMI **\_ TerminalServiceSetting** WMI représente la configuration d’un serveur hôte de session Bureau à distance (hôte de session Bureau à distance). Les paramètres incluent des fonctionnalités telles que le mode serveur hôte de session Bureau à distance, la licence, le bureau actif, les autorisations, la suppression de dossiers temporaires et les répertoires temporaires pour les sessions.

La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique. Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.

## <a name="syntax"></a>Syntaxe

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

## <a name="members"></a>Membres

La classe **Win32 \_ TerminalServiceSetting** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TerminalServiceSetting** possède ces méthodes.



| Méthode                                                                                                                | Description                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDirectConnectLicenseServer**](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | Configure un nouveau serveur de licences dans l’entreprise.<br/>                                                                                                                  |
| [**AddLSToSpecifiedLicenseServerList**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | Ajoute le serveur de licences donné à la fin de la liste des serveurs de licences spécifiés.<br/>                                                                                  |
| [**CanAccessLicenseServer**](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | Détermine si le serveur hôte de session Bureau à distance est autorisé à demander des licences d’accès client Services Bureau à distance (CAL RDS) à partir d’un serveur de licences Bureau à distance.<br/> |
| [**ChangeMode**](win32-terminalservicesetting-changemode.md)                                                         | Définit le type de licence du serveur de licences Bureau à distance.<br/>                                                                                                       |
| [**CreateWinstation**](createwinstation-win32-terminalservicesetting.md)                                             | Crée une pile d’écouteurs basée sur la combinaison unique du nom d’écouteur et de la carte réseau.<br/>                                                                              |
| [**DeleteDirectConnectLicenseServer**](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | Supprime le serveur de licences spécifié de l’entreprise.<br/>                                                                                                           |
| [**EmptySpecifiedLicenseServerList**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | Supprime tous les serveurs de licences de la liste des serveurs de licences spécifiés.<br/>                                                                                             |
| [**FindLicenseServers**](findlicenseservers-win32-terminalservicesetting.md)                                         | Énumère tous les serveurs de licences Bureau à distance et la méthode de découverte.<br/>                                                                                   |
| [**GetDomain**](getdomain-win32-terminalservicesetting.md)                                                           | Récupère le nom du domaine auquel le serveur hôte de session Bureau à distance est membre.<br/>                                                                                    |
| [**GetGracePeriodDays**](getgraceperioddays-win32-terminalservicesetting.md)                                         | Récupère le nombre de jours restants dans la période de grâce du gestionnaire de licences des services Bureau à distance pour un serveur hôte de session Bureau à distance.<br/>                                                     |
| [**GetRegisteredLicenseServerList**](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | Obtient la liste des serveurs de licences inscrits.<br/>                                                                                                                        |
| [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Récupère la liste des serveurs de licences spécifiés.<br/>                                                                                                                    |
| [**GetTSLanaIds**](gettslanaids-win32-terminalservicesetting.md)                                                     | Obtient les ID et les descriptions de Services Bureau à distance cartes réseau.<br/>                                                                                          |
| [**GetTStoLSConnectivityStatus**](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | Détermine l’état de la connectivité entre Services Bureau à distance et un serveur de licences.<br/>                                                                            |
| [**GetWinstationDriverNames**](getwinstationdrivernames-win32-terminalservicesetting.md)                             | Récupère une liste de noms de pilote de station de noms.<br/>                                                                                                                        |
| [**PingLicenseServer**](pinglicenseserver-win32-terminalservicesetting.md)                                           | Exécute une commande ping sur le serveur de licences pour déterminer s’il s’agit d’un serveur de licences valide.<br/>                                                                                         |
| [**RemoveLSFromSpecifiedLicenseServerList**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | Supprime le serveur de licences donné de la liste des serveurs de licences spécifiés.<br/>                                                                                        |
| [**SetAllowTSConnections**](win32-terminalservicesetting-setallowtsconnections.md)                                   | Définit la propriété **AllowTSConnections** .<br/>                                                                                                                           |
| [**SetDisableForcibleLogoff**](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | Définit la propriété **DisableForcibleLogoff** .<br/>                                                                                                                        |
| [**SetFallbackPrintDriverType**](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | Définit la propriété **FallbackPrintDriverType** .<br/>                                                                                                                      |
| [**SetHomeDirectory**](win32-terminalservicesetting-sethomedirectory.md)                                             | Définit la propriété **HomeDirectory** .<br/>                                                                                                                                |
| [**SetPolicyPropertyName**](win32-terminalservicesetting-setpolicypropertyname.md)                                   | Définit l’une des propriétés suivantes : **DeleteTempFolders** ou **UseTempFolders**.<br/>                                                                                  |
| [**SetPrimaryLicenseServer**](setprimarylicenseserver-win32-terminalservicesetting.md)                               | Définit le serveur de licences donné comme première entrée de la liste des serveurs de licences spécifiés.<br/>                                                                          |
| [**SetProfilePath**](win32-terminalservicesetting-setprofilepath.md)                                                 | Définit la propriété **profilePath** .<br/>                                                                                                                                  |
| [**SetSingleSession**](win32-terminalservicesetting-setsinglesession.md)                                             | Définit la propriété **SingleSession** .<br/>                                                                                                                                |
| [**SetSpecifiedLicenseServerList**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Met à jour la liste des serveurs de licences spécifiés, en remplaçant tous les serveurs de licences spécifiés existants.<br/>                                                                    |
| [**SetTimeZoneRedirection**](win32-terminalservicesetting-settimezoneredirection.md)                                 | Définit la propriété **TimeZoneRedirection** .<br/>                                                                                                                          |
| [**UpdateDirectConnectLicenseServer**](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | Met à jour la liste des serveurs de licences de découverte.<br/>                                                                                                                      |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TerminalServiceSetting** a ces propriétés.

<dl> <dt>

**ActiveDesktop**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si Active Desktop est autorisé dans chaque session utilisateur.

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (0)


</dt> <dd>

Active Desktop n’est pas autorisé dans chaque session utilisateur.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (1)


</dt> <dd>

Active Desktop est autorisé dans chaque session utilisateur.

</dd> </dl>

</dd> <dt>

**AllowTSConnections**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si de nouvelles connexions Services Bureau à distance sont autorisées.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Les nouvelles connexions ne sont pas autorisées.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Les nouvelles connexions sont autorisées.

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Brève description (chaîne d’une ligne) de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DeleteTempFolders**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si les répertoires temporaires sont supprimés à la sortie.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

La suppression des répertoires temporaires est désactivée.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

La suppression des répertoires temporaires est activée.

</dd> </dl>

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DirectConnectLicenseServers**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Cette propriété n’est pas disponible.

**Windows Server 2008 :** Énumère la liste des serveurs de licences.

</dd> <dt>

**DisableForcibleLogoff**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Détermine si un administrateur connecté à la console peut être déconnecté de force.

<dt>

0
</dt> <dd>

L’administrateur peut être déconnecté de force.

</dd> <dt>

1
</dt> <dd>

L’administrateur ne peut pas être déconnecté de force.

</dd> </dl>

</dd> <dt>

**EnableAutomaticReconnection**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie s’il faut autoriser Bureau à distance clients de connexion à se reconnecter automatiquement aux sessions sur un serveur hôte de session Bureau à distance si la liaison réseau est temporairement perdue.

<dt>

0 (0x0)
</dt> <dd>

La reconnexion automatique est désactivée.

</dd> <dt>

1 (0x1)
</dt> <dd>

La reconnexion automatique est activée.

</dd> </dl>

**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.

</dd> <dt>

**EnableDFSS**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si la planification de partage de foire dynamique (DFSS) est activée ou désactivée. Il peut s’agir de l’une des valeurs suivantes.

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

<dt>

0
</dt> <dd>

DFSS est désactivé.

</dd> <dt>

1
</dt> <dd>

DFSS est activé.

</dd> </dl>

</dd> <dt>

**EnableDiskFSS**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si la planification du partage de disque est activée.

<dt>

0 (0x0)
</dt> <dd>

La planification de la répartition des disques est désactivée.

</dd> <dt>

1 (0x1)
</dt> <dd>

La planification de la répartition des disques est activée.

</dd> </dl>

**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.

</dd> <dt>

**EnableNetworkFSS**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si la planification de partage de la charge réseau est activée.

<dt>

0 (0x0)
</dt> <dd>

La planification de la répartition des réseaux est désactivée.

</dd> <dt>

1 (0x1)
</dt> <dd>

La planification de la répartition des réseaux est activée.

</dd> </dl>

**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.

</dd> <dt>

**EnableRemoteDesktopMSI**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le Bureau à distance MSI est activé ou désactivé.

<dt>

0 (0x0)
</dt> <dd>

Désactivé

</dd> <dt>

1 (0x1)
</dt> <dd>

activé

</dd> </dl>

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**FallbackPrintDriverType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le pilote d’imprimante à partir duquel effectuer le secours.

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**Pas de dirvers de secours = 0** (0)


</dt> <dd>

Aucun pilote de secours.

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Meilleure estimation = 1** (1)


</dt> <dd>

Meilleure hypothèse.

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Meilleure hypothèse, si aucune correspondance n’est trouvée dans PCL = 2** (2)


</dt> <dd>

Meilleure hypothèse. Si aucune correspondance n’est trouvée, vous pouvez revenir à Hewlett-Packard PCL (Printer Control Language).

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Meilleure hypothèse, si aucune correspondance n’est trouvée, de secours pour PS = 3** (3)


</dt> <dd>

Meilleure hypothèse. Si aucune correspondance n’est trouvée, basculez vers PostScript (PS).

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Meilleure hypothèse, si aucune correspondance n’est trouvée, afficher les pilotes PCL et PS = 4** (4)


</dt> <dd>

Meilleure hypothèse. Si aucune correspondance n’est trouvée, affichez les pilotes PS et PCL.

</dd> </dl>

</dd> <dt>

**GetCapabilitiesID**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

ID des capacités du fournisseur.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Répertoire racine de l’ordinateur.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Date à laquelle l’objet a été installé. L’absence d’une valeur n’indique pas que l’objet n’est pas installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**LicensingDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description du mode de licence.

</dd> <dt>

**LicensingName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du mode de licence.

</dd> <dt>

**LicensingType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de licence pour le mode serveur spécifié.

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Terminal Server personnel** (0)


</dt> <dd>

Serveur hôte de session Bureau à distance personnel.

</dd> <dt>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Bureau à distance pour administration** (1)


</dt> <dd>

Bureau à distance pour l’administration.

</dd> <dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Par appareil** (2)


</dt> <dd>

Par appareil. Valide pour les serveurs d’applications.

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Par utilisateur** (3)


</dt> <dd>

Par utilisateur. Valide pour les serveurs d’applications.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (4)


</dt> <dd>

Non configuré.

</dd> </dl>

</dd> <dt>

**LimitedUserSessions**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si la fonctionnalité permettant de limiter le nombre de sessions actives et inactives autorisées sur un serveur hôte de session Bureau à distance est activée. Par exemple, vous souhaiterez peut-être définir **LimitedUserSessions** pour garantir la conformité de licence pour une application particulière installée sur le serveur hôte de session Bureau à distance. Ou bien, vous souhaiterez peut-être limiter le nombre maximal de sessions sur un serveur hôte de session Bureau à distance dans une batterie de serveurs à charge équilibrée afin que le serveur ne soit pas surchargé en cas d’échec d’un autre serveur de la batterie.

> [!Note]
>
> La session utilisée pour se connecter au serveur à des fins d’administration n’est pas affectée par **LimitedUserSessions**.
>
> Dans une batterie de serveurs hôte de session Bureau à distance, si un utilisateur dépasse la limite de session, la session est dirigée vers un autre serveur par l’équilibrage de charge du Service Broker pour les connexions Bureau à distance. Si le serveur est un serveur autonome, l’utilisateur ne sera pas en mesure de se connecter.
>
> En raison de la session utilisée pour se connecter au serveur à des fins administratives et de la synchronisation du nombre de sessions pendant le cycle d’ouverture de session, il est recommandé de définir **LimitedUserSessions** sur une valeur légèrement inférieure à la limite physique du nombre de sessions sur un serveur.
>
> La propriété **LimitedUserSessions** est valide uniquement si le service de rôle hôte de session Bureau à distance est installé.

 

<dt>

0
</dt> <dd>

La fonctionnalité est désactivée.

</dd> <dt>

1 ou plus
</dt> <dd>

Une valeur supérieure ou égale au nombre maximal de sessions (actives et inactives) autorisées sur le serveur hôte de session Bureau à distance.

</dd> </dl>

</dd> <dt>

**Ouvertures**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si les nouvelles sessions sont autorisées. Ce paramètre n’affecte pas les paramètres existants.

<dt>

0
</dt> <dd>

Les nouvelles sessions sont autorisées.

</dd> <dt>

1
</dt> <dd>

Les nouvelles sessions ne sont pas autorisées.

</dd> </dl>

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l'objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**NetworkFSSCatchAllWeight**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie le poids de partage de la charge réseau par défaut pour le trafic réseau de rattrapage. Les valeurs valides sont comprises entre 1 et 9.

**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.

</dd> <dt>

**NetworkFSSLocalSystemWeight**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie le poids de partage de la charge réseau par défaut pour un processus de système local. Les valeurs valides sont comprises entre 1 et 9.

**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.

</dd> <dt>

**NetworkFSSUserSessionWeight**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie le poids de partage de la charge réseau par défaut pour une session utilisateur. Les valeurs valides sont comprises entre 1 et 9.

**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.

</dd> <dt>

**PolicySourceAllowTSConnections**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **AllowTSConnections** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceConfiguredLicenseServers**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si les serveurs de licences retournés par la méthode [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) sont configurés par le serveur ou par la stratégie de groupe.

**Windows Server 2008 :** Cette propriété n’est pas disponible.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceDeleteTempFolders**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **DeleteTempFolders** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceDirectConnectLicenseServers**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Cette propriété n’est pas disponible.

**Windows Server 2008 :** Indique si la propriété **DirectConnectLicenseServers** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceDisableForcibleLogoff**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété n'est pas prise en charge.

**Windows Server 2008 :** Détermine si la propriété **DisableForcibleLogoff** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0
</dt> <dd>

Serveur

</dd> <dt>

1
</dt> <dd>

Stratégie de groupe.

</dd> </dl>

</dd> <dt>

**PolicySourceEnableAutomaticReconnection**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **EnableAutomaticReconnection** est configurée par le serveur ou la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.

</dd> <dt>

**PolicySourceEnableDFSS**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **EnableDFSS** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**PolicySourceEnableRemoteDesktopMSI**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **EnableRemoteDesktopMSI** est configurée par le serveur ou la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.

</dd> <dt>

**PolicySourceFallbackPrintDriverType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **FallbackPrintDriverType** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceHomeDirectory**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **HomeDirectory** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceLicensingType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **LicensingType** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceProfilePath**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **profilePath** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceRedirectSmartCards**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **RedirectSmartCards** est configurée par le serveur ou la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.

</dd> <dt>

**PolicySourceSingleSession**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **SingleSession** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceTimeZoneRedirection**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **TimeZoneRedirection** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceUseRDEasyPrintDriver**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **UseRDEasyPrintDriver** est configurée par le serveur ou la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.

</dd> <dt>

**PolicySourceUseTempFolders**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **UseTempFolders** est configurée par le serveur ou par la stratégie de groupe.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PossibleLicensingTypes**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), deux- [**tvalue**](/windows/desktop/WmiSdk/standard-qualifiers) ("Terminal Server personnel", "Bureau à distance pour l’administration", "par appareil", "par utilisateur", "non configuré")
</dt> </dl>

Masque de masque qui spécifie les types de licences disponibles. Il peut s’agir d’une combinaison d’une ou plusieurs des valeurs suivantes.

<dt>

1 (0x1)
</dt> <dd>

Les licences de serveur hôte de session Bureau à distance personnelles sont prises en charge.

</dd> <dt>

2 (0X2)
</dt> <dd>

Les licences Bureau à distance sont prises en charge.

</dd> <dt>

4 (0x4)
</dt> <dd>

Les licences par périphérique sont prises en charge.

</dd> <dt>

8 (0x8)
</dt> <dd>

Les licences par utilisateur sont prises en charge.

</dd> </dl>

</dd> <dt>

**ProfilePath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin du profil de l’ordinateur.

</dd> <dt>

**RedirectSmartCards**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si la redirection des périphériques de carte à puce est autorisée dans une session à distance.

<dt>

0 (0x0)
</dt> <dd>

La redirection de périphérique de carte à puce n’est pas autorisée.

</dd> <dt>

1 (0x1)
</dt> <dd>

La redirection de périphérique de carte à puce est autorisée.

</dd> </dl>

**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nom du serveur hôte de session Bureau à distance dont les propriétés sont intéressantes.

</dd> <dt>

**SessionBrokerDrainMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Le mode de connexion de l’utilisateur du Service Broker pour les connexions Bureau à distance.

<dt>

0
</dt> <dd>

Autoriser toutes les connexions.

</dd> <dt>

1
</dt> <dd>

Autoriser les reconnexions, mais empêcher les nouvelles ouvertures de session jusqu’à ce que le serveur soit redémarré.

</dd> <dt>

2
</dt> <dd>

Autoriser les reconnexions, mais empêcher les nouvelles ouvertures de session.

</dd> </dl>

</dd> <dt>

**SingleSession**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si une ou plusieurs sessions Services Bureau à distance sont autorisées par utilisateur.

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)


</dt> <dd>

Plusieurs sessions sont autorisées par utilisateur.

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)


</dt> <dd>

Une seule session est autorisée par utilisateur.

</dd> </dl>

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

État actuel de l’objet. Divers États opérationnels et inopérationnels peuvent être définis. Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche). Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ». Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives. Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

<dt>



 (« OK »)


</dt> <dd></dd> <dt>



 (« Erreur »)


</dt> <dd></dd> <dt>



 (« Détérioré »)


</dt> <dd></dd> <dt>



 ("Inconnu")


</dt> <dd></dd> <dt>



 (« Échec prédit »)


</dt> <dd></dd> <dt>



 (« Démarrage »)


</dt> <dd></dd> <dt>



 (« Arrêt »)


</dt> <dd></dd> <dt>



 (« Service »)


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalServerMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Mode de fonctionnement du serveur hôte de session Bureau à distance du service Services Bureau à distance. Ce mode contrôle les stratégies de licence applicables, et indique si les fonctionnalités de compatibilité des applications sont activées.

<dt>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)


</dt> <dd>

Le serveur fonctionne comme un serveur d’applications.

</dd> <dt>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)


</dt> <dd>

La session est administrée à distance.

</dd> </dl>

</dd> <dt>

**TimeZoneRedirection**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si l’ordinateur client peut rediriger ses paramètres de fuseau horaire vers la session Services Bureau à distance.

<dt>

0
</dt> <dd>

La redirection est désactivée.

</dd> <dt>

1
</dt> <dd>

La redirection est activée.

</dd> </dl>

</dd> <dt>

**UseRDEasyPrintDriver**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si le pilote d’imprimante pilote Easy Print pour les services Bureau à distance est utilisé en premier pour installer toutes les imprimantes du client.

<dt>

0
</dt> <dd>

Le serveur hôte de session Bureau à distance tente de trouver un pilote d’imprimante approprié pour installer l’imprimante cliente. Si le serveur hôte de session Bureau à distance n’a pas de pilote d’imprimante qui correspond à l’imprimante cliente, le serveur tente d’utiliser le pilote pilote Easy Print pour les services Bureau à distance pour installer l’imprimante cliente.

</dd> <dt>

1
</dt> <dd>

Le serveur hôte de session Bureau à distance tente d’abord d’utiliser le pilote d’imprimante pilote Easy Print pour les services Bureau à distance pour installer toutes les imprimantes clientes. Si, pour une raison quelconque, le pilote d’imprimante pilote Easy Print pour les services Bureau à distance ne peut pas être utilisé, un pilote d’imprimante sur le serveur hôte de session Bureau à distance qui correspond à l’imprimante cliente est utilisé.

</dd> </dl>

**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible.

</dd> <dt>

**UserPermission**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si chaque session utilisateur a une sécurité stricte ou souple.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

La sécurité est parfaite.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

La sécurité est assouplie.

</dd> </dl>

</dd> <dt>

**UseTempFolders**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si les répertoires temporaires sont créés et supprimés pour chaque session.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Les répertoires temporaires ne sont pas créés et supprimés pour chaque session. Un est créé pour la première session et jamais supprimé.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Des répertoires temporaires sont créés et supprimés pour chaque session.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Notes

**Win32 \_ TerminalServiceSetting** est associé à [**Win32 \_ TerminalService**](win32-terminalservice.md) en tant que propriété de **paramètre** de l’Association [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md) .

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md) est associé au [**\_ Terminal Win32**](win32-terminal.md) en tant que propriété de **paramètre** de l’Association [**Win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md) .

Pour se connecter à l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet. Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**. Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de six.

L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Paramètre CIM**](cim-setting.md)
</dt> <dt>

[**\_Terminal Win32**](win32-terminal.md)
</dt> <dt>

[**\_TerminalService Win32**](win32-terminalservice.md)
</dt> <dt>

[**\_TerminalServiceToSetting Win32**](win32-terminalservicetosetting.md)
</dt> <dt>

[**\_TerminalTerminalSetting Win32**](win32-terminalterminalsetting.md)
</dt> <dt>

[**\_Paramètre CIM**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

