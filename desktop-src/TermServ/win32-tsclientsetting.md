---
title: Classe Win32_TSClientSetting
description: Définit les paramètres de configuration pour la \_ classe de terminal Win32 associée à la stratégie de connexion.
ms.assetid: 438baf22-adc2-410e-bf9b-4b17a05c5ce4
ms.tgt_platform: multiple
keywords:
- Win32_TSClientSetting de la classe Services Bureau à distance
- Win32_TSClientSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSClientSetting
- Win32_TSClientSetting.Caption
- Win32_TSClientSetting.Description
- Win32_TSClientSetting.InstallDate
- Win32_TSClientSetting.Name
- Win32_TSClientSetting.Status
- Win32_TSClientSetting.TerminalName
- Win32_TSClientSetting.ConnectionPolicy
- Win32_TSClientSetting.ConnectClientDrivesAtLogon
- Win32_TSClientSetting.ConnectPrinterAtLogon
- Win32_TSClientSetting.DefaultToClientPrinter
- Win32_TSClientSetting.PolicySourceDefaultToClientPrinter
- Win32_TSClientSetting.WindowsPrinterMapping
- Win32_TSClientSetting.PolicySourceWindowsPrinterMapping
- Win32_TSClientSetting.LPTPortMapping
- Win32_TSClientSetting.PolicySourceLPTPortMapping
- Win32_TSClientSetting.COMPortMapping
- Win32_TSClientSetting.PolicySourceCOMPortMapping
- Win32_TSClientSetting.DriveMapping
- Win32_TSClientSetting.PolicySourceDriveMapping
- Win32_TSClientSetting.AudioMapping
- Win32_TSClientSetting.PolicySourceAudioMapping
- Win32_TSClientSetting.ClipboardMapping
- Win32_TSClientSetting.PolicySourceClipboardMapping
- Win32_TSClientSetting.ColorDepthPolicy
- Win32_TSClientSetting.PolicySourceColorDepthPolicy
- Win32_TSClientSetting.ColorDepth
- Win32_TSClientSetting.PolicySourceColorDepth
- Win32_TSClientSetting.MaxMonitors
- Win32_TSClientSetting.MaxXResolution
- Win32_TSClientSetting.MaxYResolution
- Win32_TSClientSetting.PolicySourceMaxMonitors
- Win32_TSClientSetting.PolicySourceMaxResolution
- Win32_TSClientSetting.PNPRedirection
- Win32_TSClientSetting.PolicySourcePNPRedirection
- Win32_TSClientSetting.AudioCaptureRedir
- Win32_TSClientSetting.PolicySourceAudioCaptureRedir
- Win32_TSClientSetting.VideoPlaybackRedir
- Win32_TSClientSetting.PolicySourceVideoPlaybackRedir
- Win32_TSClientSetting.AllowDwm
- Win32_TSClientSetting.PolicySourceAllowDwm
- Win32_TSClientSetting.PolicyAdvancedRemoteAppGraphics
- Win32_TSClientSetting.AdvancedRemoteAppGraphics
- Win32_TSClientSetting.RemoteSessionProfile
- Win32_TSClientSetting.PolicySourceRemoteSessionProfile
- Win32_TSClientSetting.AVC444ModePreferred
- Win32_TSClientSetting.PolicySourceAvc444ModePreferred
- Win32_TSClientSetting.EncodeImageQuality
- Win32_TSClientSetting.PolicySourceEncodeImageQuality
- Win32_TSClientSetting.HardwareGraphicsAdapter
- Win32_TSClientSetting.PolicySourceHardwareGraphicsAdapter
- Win32_TSClientSetting.SelectTransport
- Win32_TSClientSetting.PolicySourceSelectTransport
- Win32_TSClientSetting.SelectNetworkDetect
- Win32_TSClientSetting.PolicySourceSelectNetworkDetect
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff3e4eb9d99288914fb6d4e9a6e2d22aa38689cdc6b60f227e7e5ba2e0c5323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349363"
---
# <a name="win32_tsclientsetting-class"></a>\_Classe TSClientSetting Win32

La classe WMI **Win32 \_ TSClientSetting** définit des paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) associée à la stratégie de connexion.

La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique. Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_WIN32_TSCLIENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSClientSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ConnectionPolicy;
  uint32   ConnectClientDrivesAtLogon;
  uint32   ConnectPrinterAtLogon;
  uint32   DefaultToClientPrinter;
  uint32   PolicySourceDefaultToClientPrinter;
  uint32   WindowsPrinterMapping;
  uint32   PolicySourceWindowsPrinterMapping;
  uint32   LPTPortMapping;
  uint32   PolicySourceLPTPortMapping;
  uint32   COMPortMapping;
  uint32   PolicySourceCOMPortMapping;
  uint32   DriveMapping;
  uint32   PolicySourceDriveMapping;
  uint32   AudioMapping;
  uint32   PolicySourceAudioMapping;
  uint32   ClipboardMapping;
  uint32   PolicySourceClipboardMapping;
  uint32   ColorDepthPolicy;
  uint32   PolicySourceColorDepthPolicy;
  uint32   ColorDepth;
  uint32   PolicySourceColorDepth;
  uint32   MaxMonitors;
  uint32   MaxXResolution;
  uint32   MaxYResolution;
  uint32   PolicySourceMaxMonitors;
  uint32   PolicySourceMaxResolution;
  uint32   PNPRedirection;
  uint32   PolicySourcePNPRedirection;
  uint32   AudioCaptureRedir;
  uint32   PolicySourceAudioCaptureRedir;
  uint32   VideoPlaybackRedir;
  uint32   PolicySourceVideoPlaybackRedir;
  uint32   AllowDwm;
  uint32   PolicySourceAllowDwm;
  uint32   PolicyAdvancedRemoteAppGraphics;
  uint32   AdvancedRemoteAppGraphics;
  uint32   RemoteSessionProfile;
  uint32   PolicySourceRemoteSessionProfile;
  uint32   AVC444ModePreferred;
  uint32   PolicySourceAvc444ModePreferred;
  uint32   EncodeImageQuality;
  uint32   PolicySourceEncodeImageQuality;
  uint32   HardwareGraphicsAdapter;
  uint32   PolicySourceHardwareGraphicsAdapter;
  uint32   SelectTransport;
  uint32   PolicySourceSelectTransport;
  uint32   SelectNetworkDetect;
  uint32   PolicySourceSelectNetworkDetect;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSClientSetting** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSClientSetting** possède ces méthodes.



| Méthode                                                                   | Description                                                                                                                                                  |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConnectionSettings**](win32-tsclientsetting-connectionsettings.md)   | Définit les propriétés **ConnectClientDrivesAtLogon**, **ConnectPrinterAtLogon** et **DefaultToClientPrinter** de cette classe.<br/>                      |
| [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md)                 | Non pris en charge.<br/> **Windows 7 et Windows Server 2008 R2 :** Définit la propriété **AllowDwm** .<br/>                                               |
| [**SetClientProperty**](win32-tsclientsetting-setclientproperty.md)     | Définit la propriété **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping** ou **WindowsPrinterMapping** .<br/> |
| [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md)             | Définit la propriété **ColorDepth** .<br/>                                                                                                                 |
| [**SetColorDepthPolicy**](win32-tsclientsetting-setcolordepthpolicy.md) | Définit la propriété **ColorDepthPolicy** .<br/>                                                                                                           |
| [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md)           | Définit la propriété **MaxMonitors** .<br/>                                                                                                                |
| [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md)     | Définit la propriété **MaxXResolution** .<br/>                                                                                                             |
| [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md)     | Définit la propriété **MaxYResolution** .<br/>                                                                                                             |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSClientSetting** a ces propriétés.

<dl> <dt>

**AdvancedRemoteAppGraphics**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

spécifie s’il faut activer advanced RemoteFX graphics pour RemoteApp.

**Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** cette propriété n’est pas disponible avant Windows Server 2012 R2 et Windows 8.1.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Les graphiques avancés sont désactivés.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Les graphiques avancés sont activés.

</dd> </dl>

</dd> <dt>

**AllowDwm**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété n’est pas disponible.

* * Windows 7 et Windows Server 2008 R2 : * *

Spécifie s’il faut activer ou désactiver la composition du Bureau à distance. Zéro désactive la composition du Bureau à distance et une valeur différente de zéro le permet.

Utilisez la méthode [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) pour modifier cette propriété.

</dd> <dt>

**AudioCaptureRedir**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie s’il faut autoriser la redirection de capture audio.

**Windows Server 2008 et Windows Vista :** cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**AudioMapping**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si le mappage audio est désactivé ou activé.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Le mappage audio est activé.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Le mappage audio est désactivé.

</dd> </dl>

</dd> <dt>

**AVC444ModePreferred**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si le mode AVC444 est préféré.

**Windows 8.1, Windows Server 2012 r2, Windows 8, Windows Server 2012, Windows 7, Windows server 2008 r2, Windows Vista et Windows server 2008 :** cette propriété n’est pas disponible avant Windows 10 ou Windows Server 2016.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

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

**ClipboardMapping**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si le mappage du presse-papiers est désactivé ou activé.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Le mappage du presse-papiers est activé.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Le mappage du presse-papiers est désactivé.

</dd> </dl>

</dd> <dt>

**La**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie la profondeur de couleur. Pour connaître les valeurs possibles, consultez la méthode [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) .

<dt>

<span id="8_bit"></span><span id="8_BIT"></span>

<span id="8_bit"></span><span id="8_BIT"></span>**8 bits** (1)


</dt> <dd></dd> <dt>

<span id="15_bit"></span><span id="15_BIT"></span>

<span id="15_bit"></span><span id="15_BIT"></span>**15 bits** (2)


</dt> <dd></dd> <dt>

<span id="16_bit"></span><span id="16_BIT"></span>

<span id="16_bit"></span><span id="16_BIT"></span>**16 bits** (3)


</dt> <dd></dd> <dt>

<span id="24_bit"></span><span id="24_BIT"></span>

<span id="24_bit"></span><span id="24_BIT"></span>**24 bits** (4)


</dt> <dd></dd> <dt>

<span id="32_bit"></span><span id="32_BIT"></span>

<span id="32_bit"></span><span id="32_BIT"></span>**32 bits** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**ColorDepthPolicy**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie s’il faut remplacer le paramètre de couleur maximal de l’utilisateur.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Ne remplacez pas la stratégie de l’utilisateur.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Remplacez la stratégie de l’utilisateur.

</dd> </dl>

</dd> <dt>

**COMPortMapping**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si le mappage de port COM est désactivé ou activé.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Le mappage de port COM est activé.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Le mappage de port COM est désactivé.

</dd> </dl>

</dd> <dt>

**ConnectClientDrivesAtLogon**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si les lecteurs du client sont connectés automatiquement au cours du processus d’ouverture de session.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Les lecteurs ne sont pas automatiquement connectés.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Les lecteurs seront automatiquement connectés.

</dd> </dl>

</dd> <dt>

**ConnectionPolicy**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

La stratégie utilisée par le serveur pour récupérer les paramètres de connexion utilisateur.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Par utilisateur** (0)


</dt> <dd>

Les paramètres de connexion de l’utilisateur sont activés.

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Serveur-override** (1)


</dt> <dd>

Les paramètres de connexion de l’utilisateur sont remplacés par le serveur.

</dd> </dl>

</dd> <dt>

**ConnectPrinterAtLogon**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si toutes les imprimantes locales mappées du client seront connectées automatiquement au cours du processus d’ouverture de session.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Les imprimantes locales ne seront pas connectées automatiquement.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Les imprimantes locales seront automatiquement connectées.

</dd> </dl>

</dd> <dt>

**DefaultToClientPrinter**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si les travaux d’impression sont envoyés automatiquement à l’imprimante locale du client.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Les travaux d’impression ne sont pas envoyés automatiquement à l’imprimante locale du client.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Les travaux d’impression doivent être envoyés automatiquement à l’imprimante locale du client.

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

**DriveMapping**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si le mappage de lecteur est désactivé ou activé.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Le mappage de lecteur est activé.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Le mappage de lecteur est désactivé.

</dd> </dl>

</dd> <dt>

**EncodeImageQuality**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie la qualité de l’image pour l’expérience RDP.

**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.

<dt>

<span id="lossless"></span><span id="LOSSLESS"></span>

**sans perte** (1)


</dt> <dd></dd> <dt>

<span id="high"></span><span id="HIGH"></span>

**élevé** (2)


</dt> <dd></dd> <dt>

<span id="medium"></span><span id="MEDIUM"></span>

**moyenne** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HardwareGraphicsAdapter**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si le serveur hôte de session Bureau à distance utilise le convertisseur graphique matériel comme adaptateur par défaut.

**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

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

**LPTPortMapping**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si le mappage de port LPT est désactivé ou activé.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Le mappage de port LPT est activé.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Le mappage de port LPT est désactivé.

</dd> </dl>

</dd> <dt>

**MaxMonitors**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre maximal de moniteurs pris en charge par le serveur. Utilisez la méthode [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) pour modifier cette propriété.

**Windows Server 2008 et Windows Vista :** cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.

</dd> <dt>

**MaxXResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Résolution maximale X prise en charge par le serveur. Utilisez la méthode [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) pour modifier cette propriété.

**Windows Server 2008 et Windows Vista :** cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.

</dd> <dt>

**MaxYResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Résolution Y maximale prise en charge par le serveur. Utilisez la méthode [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) pour modifier cette propriété.

**Windows Server 2008 et Windows Vista :** cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.

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

**PNPRedirection**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie s’il faut autoriser Plug-and-Play redirection.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Autorisez la redirection de Plug-and-Play.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

N’autorisez pas la redirection de Plug-and-Play.

</dd> </dl>

</dd> <dt>

**PolicyAdvancedRemoteAppGraphics**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **AdvancedRemoteAppGraphics** est configurée par le serveur ou la stratégie de groupe.

**Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** cette propriété n’est pas disponible avant Windows Server 2012 R2 et Windows 8.1.

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

**PolicySourceAllowDwm**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété n’est pas disponible.

* * Windows 7 et Windows Server 2008 R2 : * *

Indique si la propriété **AllowDwm** est configurée par le serveur ou la stratégie de groupe.

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

**PolicySourceAudioCaptureRedir**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **AudioCaptureRedir** est configurée par le serveur ou la stratégie de groupe.

**Windows Server 2008 et Windows Vista :** cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.

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

**PolicySourceAudioMapping**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **AudioMapping** est configurée par le serveur, la stratégie de groupe ou par défaut.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2 (0X2)
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**PolicySourceAvc444ModePreferred**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique comment la propriété **AVC444ModePreferredis** est configurée.

**Windows 8.1, Windows Server 2012 r2, Windows 8, Windows Server 2012, Windows 7, Windows server 2008 r2, Windows Vista et Windows server 2008 :** cette propriété n’est pas disponible avant Windows 10 ou Windows Server 2016.

<dt>

0
</dt> <dd>

Serveur

</dd> <dt>

1
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceClipboardMapping**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **ClipboardMapping** est configurée par le serveur, la stratégie de groupe ou par défaut.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2 (0X2)
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**PolicySourceColorDepth**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **ColorDepth** est configurée par le serveur, la stratégie de groupe ou par défaut.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2 (0X2)
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**PolicySourceColorDepthPolicy**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **ColorDepthPolicy** est configurée par le serveur, la stratégie de groupe ou par défaut.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2 (0X2)
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**PolicySourceCOMPortMapping**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **COMPortMapping** est configurée par le serveur, la stratégie de groupe ou par défaut.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2 (0X2)
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**PolicySourceDefaultToClientPrinter**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **DefaultToClientPrinter** est configurée par le serveur, la stratégie de groupe ou par défaut.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2 (0X2)
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**PolicySourceDriveMapping**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **DriveMapping** est configurée par le serveur, la stratégie de groupe ou par défaut.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2 (0X2)
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**PolicySourceEncodeImageQuality**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique la configuration de **EncodeImageQualityi** .

**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.

<dt>

0
</dt> <dd>

Serveur

</dd> <dt>

1
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceHardwareGraphicsAdapter**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique la configuration de **HardwareGraphicsAdapter** .

**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.

<dt>

0
</dt> <dd>

Serveur

</dd> <dt>

1
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceLPTPortMapping**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **LPTPortMapping** est configurée par le serveur, la stratégie de groupe ou par défaut.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2 (0X2)
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**PolicySourceMaxMonitors**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **MaxMonitors** est configurée par le serveur, la stratégie de groupe ou par défaut.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2 (0X2)
</dt> <dd>

Default

</dd> </dl>

**Windows Server 2008 et Windows Vista :** cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.

</dd> <dt>

**PolicySourceMaxResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si les propriétés **MaxXResolution** et **MaxYResolution** sont configurées par le serveur, la stratégie de groupe ou par défaut.

**Windows Server 2008 et Windows Vista :** cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2 (0X2)
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**PolicySourcePNPRedirection**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **PNPRedirection** est configurée par le serveur ou par la stratégie de groupe.

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

**PolicySourceRemoteSessionProfile**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique la configuration de **RemoteSessionProfile** .

**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.

<dt>

0
</dt> <dd>

Serveur

</dd> <dt>

1
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceSelectNetworkDetect**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique comment la propriété **SelectNetworkDetect** est configurée.

**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.

<dt>

0
</dt> <dd>

Serveur

</dd> <dt>

1
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceSelectTransport**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique comment la propriété **SelectTransport** est configurée.

**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.

<dt>

0
</dt> <dd>

Serveur

</dd> <dt>

1
</dt> <dd>

Stratégie de groupe

</dd> </dl>

</dd> <dt>

**PolicySourceVideoPlaybackRedir**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **VideoPlaybackRedir** est configurée par le serveur ou la stratégie de groupe.

**Windows Server 2008 et Windows Vista :** cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.

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

**PolicySourceWindowsPrinterMapping**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la propriété **WindowsPrinterMapping** est configurée par le serveur, la stratégie de groupe ou par défaut.

<dt>

0 (0x0)
</dt> <dd>

Serveur

</dd> <dt>

1 (0x1)
</dt> <dd>

Stratégie de groupe

</dd> <dt>

2 (0X2)
</dt> <dd>

Default

</dd> </dl>

</dd> <dt>

**RemoteSessionProfile**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie le profil pour l’expérience RDP.

**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.

<dt>

<span id="scale"></span><span id="SCALE"></span>

**échelle** (1)


</dt> <dd></dd> <dt>

<span id="experience"></span><span id="EXPERIENCE"></span>

**expérience** (2)


</dt> <dd></dd> <dt>

<span id="bandwidth"></span><span id="BANDWIDTH"></span>

**bande passante** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**SelectNetworkDetect**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si la détection réseau est utilisée.

**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.

<dt>

0
</dt> <dd>

utilisé au moment de la connexion et dans un état stable.

</dd> <dt>

1
</dt> <dd>

désactivé au moment de la connexion

</dd> <dt>

2
</dt> <dd>

désactivé dans un état stable

</dd> <dt>

3
</dt> <dd>

désactivé au moment de la connexion et dans un état stable.

</dd> </dl>

</dd> <dt>

**SelectTransport**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie les protocoles de transport qui peuvent être utilisés pour l’accès RDP au serveur.

**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.

<dt>

0
</dt> <dd>

Utilisez à la fois UDP et TCP.

</dd> <dt>

1
</dt> <dd>

Utilisez uniquement TCP.

</dd> <dt>

2
</dt> <dd>

Utilisez le protocole UDP ou TCP.

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

**TerminalName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du terminal.

Cette propriété est héritée de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).

</dd> <dt>

**VideoPlaybackRedir**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie s’il faut autoriser la redirection de lecture vidéo.

**Windows Server 2008 et Windows Vista :** cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**WindowsPrinterMapping**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si le mappage de l’imprimante est désactivé ou activé pour la fenêtre du client.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Le mappage d’imprimante est activé.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Le mappage d’imprimante est désactivé.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Remarques

Sachez qu’une station de fenêtre associée à la session de console ne peut pas accéder aux méthodes et aux propriétés de cette classe. Si vous tentez de le faire en spécifiant « console » comme valeur de la propriété **TerminalName** , les méthodes de cet objet retournent **WBEM \_ E \_ non \_ pris en charge**. Ce code d’erreur est également retourné si une station Windows tente d’appeler des méthodes de cet objet pour ajouter ou modifier les propriétés de sécurité des comptes LocalSystem, LocalService ou NetworkService.

Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet. Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**. pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « pktPrivacy », avec une valeur de six.

l’exemple VBScript (Visual Basic scripting Edition) suivant montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Terminal Win32**](win32-terminal.md)
</dt> <dt>

[**\_TerminalSetting Win32**](win32-terminalsetting.md)
</dt> <dt>

[**\_Paramètre CIM**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

