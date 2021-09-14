---
description: représente un appareil connecté à un ordinateur exécutant sur un système d’exploitation Microsoft Windows qui peut produire une image imprimée ou du texte sur papier ou autre support.
ms.assetid: 58090e6a-8f13-4859-adb8-a7c6299d3efd
ms.tgt_platform: multiple
title: Win32_Printer, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer
- Win32_Printer.Reset
- Win32_Printer.SetPowerState
- Win32_Printer.Attributes
- Win32_Printer.Availability
- Win32_Printer.AvailableJobSheets
- Win32_Printer.AveragePagesPerMinute
- Win32_Printer.Capabilities
- Win32_Printer.CapabilityDescriptions
- Win32_Printer.Caption
- Win32_Printer.CharSetsSupported
- Win32_Printer.Comment
- Win32_Printer.ConfigManagerErrorCode
- Win32_Printer.ConfigManagerUserConfig
- Win32_Printer.CreationClassName
- Win32_Printer.CurrentCapabilities
- Win32_Printer.CurrentCharSet
- Win32_Printer.CurrentLanguage
- Win32_Printer.CurrentMimeType
- Win32_Printer.CurrentNaturalLanguage
- Win32_Printer.CurrentPaperType
- Win32_Printer.Default
- Win32_Printer.DefaultCapabilities
- Win32_Printer.DefaultCopies
- Win32_Printer.DefaultLanguage
- Win32_Printer.DefaultMimeType
- Win32_Printer.DefaultNumberUp
- Win32_Printer.DefaultPaperType
- Win32_Printer.DefaultPriority
- Win32_Printer.Description
- Win32_Printer.DetectedErrorState
- Win32_Printer.DeviceID
- Win32_Printer.Direct
- Win32_Printer.DoCompleteFirst
- Win32_Printer.DriverName
- Win32_Printer.EnableBIDI
- Win32_Printer.EnableDevQueryPrint
- Win32_Printer.ErrorCleared
- Win32_Printer.ErrorDescription
- Win32_Printer.ErrorInformation
- Win32_Printer.ExtendedDetectedErrorState
- Win32_Printer.ExtendedPrinterStatus
- Win32_Printer.Hidden
- Win32_Printer.HorizontalResolution
- Win32_Printer.InstallDate
- Win32_Printer.JobCountSinceLastReset
- Win32_Printer.KeepPrintedJobs
- Win32_Printer.LanguagesSupported
- Win32_Printer.LastErrorCode
- Win32_Printer.Local
- Win32_Printer.Location
- Win32_Printer.MarkingTechnology
- Win32_Printer.MaxCopies
- Win32_Printer.MaxNumberUp
- Win32_Printer.MaxSizeSupported
- Win32_Printer.MimeTypesSupported
- Win32_Printer.Name
- Win32_Printer.NaturalLanguagesSupported
- Win32_Printer.Network
- Win32_Printer.PaperSizesSupported
- Win32_Printer.PaperTypesAvailable
- Win32_Printer.Parameters
- Win32_Printer.PNPDeviceID
- Win32_Printer.PortName
- Win32_Printer.PowerManagementCapabilities
- Win32_Printer.PowerManagementSupported
- Win32_Printer.PrinterPaperNames
- Win32_Printer.PrinterState
- Win32_Printer.PrinterStatus
- Win32_Printer.PrintJobDataType
- Win32_Printer.PrintProcessor
- Win32_Printer.Priority
- Win32_Printer.Published
- Win32_Printer.Queued
- Win32_Printer.RawOnly
- Win32_Printer.SeparatorFile
- Win32_Printer.ServerName
- Win32_Printer.Shared
- Win32_Printer.ShareName
- Win32_Printer.SpoolEnabled
- Win32_Printer.StartTime
- Win32_Printer.Status
- Win32_Printer.StatusInfo
- Win32_Printer.SystemCreationClassName
- Win32_Printer.SystemName
- Win32_Printer.TimeOfLastReset
- Win32_Printer.UntilTime
- Win32_Printer.VerticalResolution
- Win32_Printer.WorkOffline
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48fc170cb3e85d44dc3e01140fe2c881a7ec975b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006538"
---
# <a name="win32_printer-class"></a>\_Classe d’imprimantes Win32

la [classe WMI](../wmisdk/retrieving-a-class.md) de l' **\_ imprimante Win32** représente un appareil connecté à un ordinateur qui s’exécute sur un système d’exploitation Microsoft Windows qui peut produire une image imprimée ou du texte sur papier ou autre support.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class Win32_Printer : CIM_Printer
{
  uint32   Attributes;
  uint16   Availability;
  string   AvailableJobSheets[];
  uint32   AveragePagesPerMinute;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  string   Comment;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  boolean  Default;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  uint32   DefaultPriority;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  Direct;
  boolean  DoCompleteFirst;
  string   DriverName;
  boolean  EnableBIDI;
  boolean  EnableDevQueryPrint;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint16   ExtendedDetectedErrorState;
  uint16   ExtendedPrinterStatus;
  boolean  Hidden;
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  boolean  KeepPrintedJobs;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  boolean  Local;
  string   Location;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  boolean  Network;
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   Parameters;
  string   PNPDeviceID;
  string   PortName;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   PrinterPaperNames[];
  uint32   PrinterState;
  uint16   PrinterStatus;
  string   PrintJobDataType;
  string   PrintProcessor;
  uint32   Priority;
  boolean  Published;
  boolean  Queued;
  boolean  RawOnly;
  string   SeparatorFile;
  string   ServerName;
  boolean  Shared;
  string   ShareName;
  boolean  SpoolEnabled;
  datetime StartTime;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  datetime UntilTime;
  uint32   VerticalResolution;
  boolean  WorkOffline;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ Printer** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La **classe \_ Printer Win32** possède ces méthodes.



| Méthode                                                                               | Description                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddPrinterConnection**](addprinterconnection-method-in-class-win32-printer.md)   | Ajoute une connexion à l’imprimante.<br/>                                                                                                                                                                      |
| [**CancelAllJobs**](cancelalljobs-method-in-class-win32-printer.md)                 | Annule tous les travaux.<br/>                                                                                                                                                                                      |
| [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class-win32-printer.md) | Retourne le descripteur de sécurité qui contrôle l’accès à l’imprimante.<br/>                                                                                                                                   |
| [**Suspendre**](pause-method-in-class-win32-printer.md)                                 | Pause la file d'attente à l'impression.<br/>                                                                                                                                                                                |
| [**PrintTestPage**](printtestpage-method-in-class-win32-printer.md)                 | Imprime une page de test.<br/>                                                                                                                                                                                    |
| [**RenamePrinter**](renameprinter-method-in-class-win32-printer.md)                 | Renomme une imprimante.<br/>                                                                                                                                                                                     |
| **Réinitialiser**                                                                            | Non implémenté. Pour plus d’informations sur l’implémentation de cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans l' [**\_ imprimante CIM**](cim-printer.md).<br/>                 |
| [**Sort**](resume-method-in-class-win32-printer.md)                               | Reprend la file d’attente à l’impression en pause.<br/>                                                                                                                                                                            |
| [**SetDefaultPrinter**](setdefaultprinter-method-in-class-win32-printer.md)         | Définit l’imprimante par défaut.<br/>                                                                                                                                                                              |
| **SetPowerState**                                                                    | Non implémenté. Pour plus d’informations sur l’implémentation de cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans l' [**\_ imprimante CIM**](cim-printer.md).<br/> |
| [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class-win32-printer.md) | Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès à l’imprimante.<br/>                                                                                                              |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ Printer** possède ces propriétés.

<dl> <dt>

**Attributs**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Bitmap d’attributs pour un périphérique d’impression basé sur Windows.

<dt>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**Imprimante \_ ATTRIBUT \_ mis en file d’attente** (1 (0x1))


</dt> <dd>

Mis en file d'attente.

Les travaux d’impression sont mis en mémoire tampon et mis en file d’attente.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**Imprimante \_ ATTRIBUT \_ direct** (2 (0X2))


</dt> <dd>

Direct

Document à envoyer directement à l’imprimante. Cette valeur est utilisée si les travaux d’impression ne sont pas mis en file d’attente correctement.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**Imprimante \_ ATTRIBUT \_ par défaut** (4 (0x4))


</dt> <dd>

Default

Imprimante par défaut sur un ordinateur.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**Imprimante \_ ATTRIBUT \_ Shared** (8 (0x8))


</dt> <dd>

Partagé

Disponible en tant que ressource réseau partagée.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**Imprimante \_ \_Réseau d’attributs** (16 (0x10))


</dt> <dd>

Réseau

Attaché à un réseau. Si les bits réseau et locaux sont tous deux définis, cela indique une imprimante réseau.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**Imprimante \_ ATTRIBUT \_ masqué** (32 (0x20))


</dt> <dd>

Hidden

Masqué pour certains utilisateurs sur le réseau.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**Imprimante \_ ATTRIBUT \_ local** (64 (0x40))


</dt> <dd>

Local

Connecté directement à un ordinateur. Si les bits réseau et locaux sont tous deux définis, cela indique une imprimante réseau.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**Imprimante \_ ATTRIBUT \_ ENABLEDEVQ** (128 (0x80))


</dt> <dd>

EnableDevQ

Activez la file d’attente sur l’imprimante si elle est disponible.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**Imprimante \_ ATTRIBUT \_ KEEPPRINTEDJOBS** (256 (0x100))


</dt> <dd>

KeepPrintedJobs

Le spouleur ne doit pas supprimer les documents une fois qu’ils sont imprimés.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**Imprimante \_ L’attribut se \_ \_ termine en \_ premier** (512 (0x200))


</dt> <dd>

DoCompleteFirst

Démarrer en premier les travaux qui se sont terminés.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**Imprimante \_ Travail d’attribut \_ \_ hors connexion** (1024 (0x400))


</dt> <dd>

WorkOffline

Met en file d’attente les travaux d’impression quand une imprimante n’est pas disponible.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**Imprimante \_ ATTRIBUT \_ Enable \_ BIDI** (2048 (0x800))


</dt> <dd>

EnableBIDI

Activez l’impression bidirectionnelle.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**Imprimante \_ ATTRIBUT \_ brut \_ uniquement** (4096 (0x1000))


</dt> <dd>

Autorisez uniquement les travaux de type de données bruts à être mis en file d’attente.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**Imprimante \_ ATTRIBUT \_ publié** (8192 (0x2000))


</dt> <dd>

Publié

Publié dans le service d’annuaire réseau.

</dd> </dl>

</dd> <dt>

**Disponibilité**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")
</dt> </dl>

Disponibilité et état de l’appareil.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)


</dt> <dd>

En cours d’exécution ou pleine puissance

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)


</dt> <dd>

L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)


</dt> <dd>

L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)


</dt> <dd>

L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)


</dt> <dd>

L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)


</dt> <dd>

L’appareil est suspendu.

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)


</dt> <dd>

Le périphérique n’est pas prêt.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)


</dt> <dd>

L’appareil n’est pas configuré.

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)


</dt> <dd>

L’appareil est calme.

</dd> </dl>

</dd> <dt>

**AvailableJobSheets**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. RequiredJobSheets")
</dt> </dl>

Tableau de toutes les feuilles de travail disponibles sur une imprimante. Peut également être utilisé pour décrire la bannière qu’une imprimante peut fournir au début de chaque travail, ou d’autres options spécifiées par l’utilisateur.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**AveragePagesPerMinute**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Vitesse d’impression, en nombre moyen de pages par minute, qu’une imprimante peut produire en sortie.

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md). CapabilityDescriptions "," CIM \_ PrintJob. finition "," CIM \_ printservice. Capabilities ")
</dt> </dl>

Tableau de fonctionnalités d’imprimante.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impression des couleurs** (2)


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impression recto-verso** (3)


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Classement** (5)


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Agrafage** (6)


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impression** de la transparence (7)


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Poinçon** (8)


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Couverture** (9)


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Liaison** (10)


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impression en noir et blanc** (11)


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un côté** (12)


</dt> <dd>

One-Sided

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bord long** recto-verso (13)


</dt> <dd>

Bord long Two-Sided

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bord à deux côtés** (14)


</dt> <dd>

Bord Two-Sided

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paysage** (16)


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Portrait inversé** (17)


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paysage inversé** (18)


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualité élevée** (19)


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualité normale** (20)


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualité faible** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**Capacités**»)
</dt> </dl>

Tableau de chaînes de forme libre qui fournissent des explications détaillées sur les fonctionnalités de l’imprimante indiquées dans le tableau des **fonctionnalités** . Chaque entrée de ce tableau est liée à une entrée du tableau de **fonctionnalités** qui se trouve dans le même index.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)
</dt> </dl>

Description succincte d’un objet : chaîne d’une ligne.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CharSetsSupported**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. CharSet"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Imprimante IETF-MIB. prtLocalizationCharacterSet ")
</dt> </dl>

Tableau des jeux de caractères disponibles pour la sortie. Les chaînes fournies dans cette propriété doivent être conformes à la sémantique et à la syntaxe spécifiées par la section 4.1.2 ("charset Parameters") dans la norme RFC 2046 (MIME part 2) et contenues dans le Registre du jeu de caractères IANA. Exemples : « UTF-8 », « US-ASCII » et « ISO-8859-1 ».

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**Commentaire**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Commentaire pour une file d’attente à l’impression.

Exemple : imprimante couleur

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Code d’erreur Configuration Manager Win32.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**  (0)


</dt> <dd>

L’appareil fonctionne correctement.

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.** (1)


</dt> <dd>

L’appareil n’est pas configuré correctement.

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.** (3)


</dt> <dd>

Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.** (4)


</dt> <dd>

L’appareil ne fonctionne pas correctement. L’un de ses pilotes ou le Registre est peut-être endommagé.

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**le pilote de cet appareil a besoin d’une ressource qui ne peut pas être gérée par Windows.** (5)


</dt> <dd>

le pilote de l’appareil requiert une ressource qui ne peut pas être gérée par Windows.

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**  (6)


</dt> <dd>

La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.** (7)


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.** (8)


</dt> <dd>

Le chargeur de pilote de l’appareil est manquant.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.** (9)


</dt> <dd>

L’appareil ne fonctionne pas correctement. Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.** (10)


</dt> <dd>

Impossible de démarrer l’appareil.

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.** (11)


</dt> <dd>

Échec de l’appareil.

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.** douze


</dt> <dd>

L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne pouvez pas vérifier les ressources de ce périphérique.** (13)


</dt> <dd>

Windows ne pouvez pas vérifier les ressources de l’appareil.

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.** (14)


</dt> <dd>

L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.** (15)


</dt> <dd>

L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.** (16)


</dt> <dd>

Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.** (17)


</dt> <dd>

L’appareil demande un type de ressource inconnu.

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.** (18)


</dt> <dd>

Les pilotes de périphérique doivent être réinstallés.

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.** (20)


</dt> <dd>

Le Registre est peut-être endommagé.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.** (21)


</dt> <dd>

Défaillance du système. Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel. Windows supprime l’appareil.

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.** (22)


</dt> <dd>

L’appareil est désactivé.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.** (23)


</dt> <dd>

Défaillance du système. Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.** (24)


</dt> <dd>

L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours d’installation sur cet appareil.** (25)


</dt> <dd>

Windows est toujours en cours de configuration de l’appareil.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours d’installation sur cet appareil.** (26)


</dt> <dd>

Windows est toujours en cours de configuration de l’appareil.

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.** (27)


</dt> <dd>

L’appareil n’a pas de configuration de journal valide.

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.** (28)


</dt> <dd>

Les pilotes de périphérique ne sont pas installés.

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.** (29)


</dt> <dd>

L’appareil est désactivé. Le microprogramme de l’appareil n’a pas fourni les ressources requises.

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.** (30)


</dt> <dd>

L’appareil utilise une ressource IRQ qu’un autre appareil utilise.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**cet appareil ne fonctionne pas correctement car Windows ne peut pas charger les pilotes requis pour cet appareil.** (31)


</dt> <dd>

L’appareil ne fonctionne pas correctement. Windows ne peut pas charger les pilotes de périphérique requis.

</dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée pour créer une instance. Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**CurrentCapabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**Capacités**»)
</dt> </dl>

Tableau de fonctionnalités d’imprimante actuellement utilisées. Une entrée de cette propriété doit également être listée dans le tableau **Capabilities** .

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impression des couleurs** (2)


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impression recto-verso** (3)


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Classement** (5)


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Agrafage** (6)


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impression** de la transparence (7)


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Poinçon** (8)


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Couverture** (9)


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Liaison** (10)


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impression en noir et blanc** (11)


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un côté** (12)


</dt> <dd>

One-Sided

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bord long** recto-verso (13)


</dt> <dd>

Bord long Two-Sided

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bord à deux côtés** (14)


</dt> <dd>

Bord Two-Sided

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paysage** (16)


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Portrait inversé** (17)


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paysage inversé** (18)


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualité élevée** (19)


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualité normale** (20)


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualité faible** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**CurrentCharSet**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**CharSetsSupported**")
</dt> </dl>

Jeu de caractères actuellement utilisé pour la sortie. Les chaînes fournies dans cette propriété doivent être conformes à la sémantique et à la syntaxe spécifiées par la section 4.1.2 ("charset Parameters") dans la norme RFC 2046 (MIME part 2) et contenues dans le Registre du jeu de caractères IANA. Exemples : « UTF-8 », « US-ASCII » et ISO-8859-1.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md). LanguagesSupported ","**\_ imprimante CIM**.**CurrentMimeType**")
</dt> </dl>

Langue de l’imprimante actuellement utilisée. La langue utilisée doit être indiquée dans la propriété **LanguagesSupported** .

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span id="PCL"></span><span id="pcl"></span>**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span id="PJL"></span><span id="pjl"></span>**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span id="PS"></span><span id="ps"></span>**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span id="IPDS"></span><span id="ipds"></span>**IPD** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpression** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Données de ligne** (15)


</dt> <dd>

LineData

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span id="MODCA"></span><span id="modca"></span>**MODCA** (16)


</dt> <dd>

DODCA

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span id="REGIS"></span><span id="regis"></span>**Regis** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span id="SCS"></span><span id="scs"></span>**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span id="PDS"></span><span id="pds"></span>**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span id="IGP"></span><span id="igp"></span>**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span id="WPS"></span><span id="wps"></span>**WPS** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span id="LN03"></span><span id="ln03"></span>**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span id="QUIC"></span><span id="quic"></span>**QUIC** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span id="CPAP"></span><span id="cpap"></span>**Pression positive** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Texte simple** (31)


</dt> <dd>

SimpleText

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span id="NPAP"></span><span id="npap"></span>**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span id="DOC"></span><span id="doc"></span>**Doc** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**impressionne** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatique** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span id="LIPS"></span><span id="lips"></span>**Lèvres** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Majuscules** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span id="EXCL"></span><span id="excl"></span>**Excl** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span id="LCDS"></span><span id="lcds"></span>**Écrans plats** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span id="XES"></span><span id="xes"></span>**X** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span id="MIME"></span><span id="mime"></span>**MIME** (47)


</dt> <dd></dd> <dt>

48
</dt> <dd>

XPS

</dd> <dt>

49
</dt> <dd>

HPGL2

</dd> <dt>

50
</dt> <dd>

PCLXL

</dd> </dl>

</dd> <dt>

**CurrentMimeType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**CurrentLanguage**")
</dt> </dl>

Type MIME actuellement utilisé si **currentLanguage** est un type MIME (valeur = 47).

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**CurrentNaturalLanguage**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**NaturalLanguagesSupported**")
</dt> </dl>

Langue actuellement utilisée par l’imprimante pour la gestion. La langue répertoriée ici doit également être répertoriée dans la propriété **NaturalLanguagesSupported** .

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**CurrentPaperType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**PaperTypesAvailable**")
</dt> </dl>

Type de papier utilisé par l’imprimante. Doit être exprimée sous la forme spécifiée par l’application d’impression de documents ISO/IEC 10175 (DPA), qui est résumée dans l’annexe C de la RFC 1759 (MIB de l’imprimante).

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**Par défaut**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’imprimante est l’imprimante par défaut.

</dd> <dt>

**DefaultCapabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**Capacités**»)
</dt> </dl>

Tableau des fonctionnalités d’imprimante utilisées par défaut. Chaque entrée du tableau **DefaultCapabilities** doit également être listée dans le tableau **Capabilities** .

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impression des couleurs** (2)


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impression recto-verso** (3)


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Classement** (5)


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Agrafage** (6)


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impression** de la transparence (7)


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Poinçon** (8)


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Couverture** (9)


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Liaison** (10)


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impression en noir et blanc** (11)


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un côté** (12)


</dt> <dd>

One-Sided

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bord long** recto-verso (13)


</dt> <dd>

Bord long Two-Sided

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bord à deux côtés** (14)


</dt> <dd>

Bord Two-Sided

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paysage** (16)


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Portrait inversé** (17)


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paysage inversé** (18)


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualité élevée** (19)


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualité normale** (20)


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualité faible** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**DefaultCopies**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de copies produites pour un travail, sauf indication contraire.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**DefaultLanguage**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md). LanguagesSupported ","**\_ imprimante CIM**.**DefaultMimeType**")
</dt> </dl>

Langue de l’imprimante par défaut. La langue répertoriée ici doit également être répertoriée dans la propriété **LanguagesSupported** .

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span id="PCL"></span><span id="pcl"></span>**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span id="PJL"></span><span id="pjl"></span>**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span id="PS"></span><span id="ps"></span>**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span id="IPDS"></span><span id="ipds"></span>**IPD** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpression** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Données de ligne** (15)


</dt> <dd>

LineData

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span id="MODCA"></span><span id="modca"></span>**MODCA** (16)


</dt> <dd>

DODCA

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span id="REGIS"></span><span id="regis"></span>**Regis** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span id="SCS"></span><span id="scs"></span>**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span id="PDS"></span><span id="pds"></span>**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span id="IGP"></span><span id="igp"></span>**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span id="WPS"></span><span id="wps"></span>**WPS** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span id="LN03"></span><span id="ln03"></span>**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span id="QUIC"></span><span id="quic"></span>**QUIC** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span id="CPAP"></span><span id="cpap"></span>**Pression positive** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Texte simple** (31)


</dt> <dd>

SimpleText

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span id="NPAP"></span><span id="npap"></span>**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span id="DOC"></span><span id="doc"></span>**Doc** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**impressionne** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatique** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span id="LIPS"></span><span id="lips"></span>**Lèvres** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Majuscules** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span id="EXCL"></span><span id="excl"></span>**Excl** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span id="LCDS"></span><span id="lcds"></span>**Écrans plats** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span id="XES"></span><span id="xes"></span>**X** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span id="MIME"></span><span id="mime"></span>**MIME** (47)


</dt> <dd></dd> <dt>

48
</dt> <dd>

XPS

</dd> <dt>

49
</dt> <dd>

HPGL2

</dd> <dt>

50
</dt> <dd>

PCLXL

</dd> </dl>

</dd> <dt>

**DefaultMimeType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**DefaultLanguage**")
</dt> </dl>

Type MIME en cours d’utilisation, si la valeur **DefaultLanguage** est un type MIME (valeur = 47).

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**DefaultNumberUp**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de pages de flux d’impression rendues par l’imprimante sur une feuille de support, sauf si une tâche le spécifie autrement.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**DefaultPaperType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**PaperTypesAvailable**")
</dt> </dl>

Type de papier utilisé par l’imprimante, à moins qu’un travail d’impression spécifie un type de papier différent. La chaîne doit être exprimée sous la forme spécifiée par l’application d’impression de documents ISO/IEC 1017 (DPA), qui est résumée dans l’annexe C de la [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (MIB de l’imprimante).

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**DefaultPriority**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Valeur de priorité par défaut assignée à chaque travail d’impression.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Description d’un objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DetectedErrorState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**ErrorInformation**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" MIB. \|Imprimante IETF-MIB. hrPrinterDetectedErrorState ")
</dt> </dl>

Informations sur l’erreur de l’imprimante.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

**Aucune erreur** (2)


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

**Papier faible** (3)


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

**Aucun papier** (4)


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

**Toner faible** (5)


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

**Aucun toner** (6)


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

**Porte ouverte** (7)


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

**Coincé** (8)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Hors connexion** (9)


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

**Service demandé** (10)


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

**Bac de sortie complet** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Identificateur unique de l’imprimante sur un système.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**Direct**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, le travail d’impression est envoyé directement à l’imprimante. Si la **valeur est false**, le travail d’impression est mis en attente.

</dd> <dt>

**DoCompleteFirst**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, l’imprimante démarre les travaux qui sont terminés. Si la **valeur est false**, l’imprimante démarre les travaux dans l’ordre dans lequel les travaux sont reçus.

</dd> <dt>

**DriverName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

nom du pilote d’imprimante Windows.

exemple : Windows pilote de télécopie

</dd> <dt>

**EnableBIDI**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, l’imprimante peut imprimer de manière bidirectionnelle.

</dd> <dt>

**EnableDevQueryPrint**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, l’imprimante conserve les documents dans la file d’attente lorsque les configurations du document et de l’imprimante ne correspondent pas.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** a été effacée.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Informations sur l’erreur enregistrée dans **LastErrorCode**, et informations sur les actions correctives qui peuvent être effectuées.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**ErrorInformation**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**DetectedErrorState**")
</dt> </dl>

Tableau d’informations supplémentaires pour l’état d’erreur actuel indiqué dans **DetectedErrorState**.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**ExtendedDetectedErrorState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Signale des informations d’erreur standard. Des informations supplémentaires doivent être enregistrées dans **DetectedErrorState**.

Les valeurs sont les suivantes :

<dt>

0 (0x0)
</dt> <dd>

Unknown

</dd> <dt>

1 (0x1)
</dt> <dd>

Autre

</dd> <dt>

2 (0X2)
</dt> <dd>

Aucune erreur

</dd> <dt>

3 (0x3)
</dt> <dd>

Niveau de papier faible

</dd> <dt>

4 (0x4)
</dt> <dd>

Plus de papier

</dd> <dt>

5 (0x5)
</dt> <dd>

Niveau de toner faible

</dd> <dt>

6 (0x6)
</dt> <dd>

Il n'y a plus d'encre

</dd> <dt>

7 (0x7)
</dt> <dd>

Capot ouvert

</dd> <dt>

8 (0x8)
</dt> <dd>

Bourrage papier

</dd> <dt>

9 (0x9)
</dt> <dd>

Entretien nécessaire

</dd> <dt>

10 (0xA)
</dt> <dd>

Bac de réception plein

</dd> <dt>

11 (0xB)
</dt> <dd>

Problème de papier

</dd> <dt>

12 (0xC)
</dt> <dd>

Impossible d’imprimer la page

</dd> <dt>

13 (0xD)
</dt> <dd>

Intervention de l’utilisateur requise

</dd> <dt>

14 (0xE)
</dt> <dd>

Mémoire insuffisante

</dd> <dt>

15 (0xF)
</dt> <dd>

Serveur inconnu

</dd> </dl>

</dd> <dt>

**ExtendedPrinterStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Informations d’État pour une imprimante qui diffèrent de celles spécifiées dans la propriété **Availability** .

<dt>

1 (0x1)
</dt> <dd>

Autre

</dd> <dt>

2 (0X2)
</dt> <dd>

Unknown

</dd> <dt>

3 (0x3)
</dt> <dd>

Idle

</dd> <dt>

4 (0x4)
</dt> <dd>

Impression

</dd> <dt>

5 (0x5)
</dt> <dd>

Préchauffage

</dd> <dt>

6 (0x6)
</dt> <dd>

Impression arrêtée

</dd> <dt>

7
</dt> <dd>

Hors connexion

</dd> <dt>

8 (0x8)
</dt> <dd>

Suspendu

</dd> <dt>

9 (0x9)
</dt> <dd>

Erreur

</dd> <dt>

10 (0xA)
</dt> <dd>

Busy

</dd> <dt>

11 (0xB)
</dt> <dd>

Non disponible

</dd> <dt>

12 (0xC)
</dt> <dd>

En attente

</dd> <dt>

13 (0xD)
</dt> <dd>

Traitement en cours

</dd> <dt>

14 (0xE)
</dt> <dd>

Initialisation

</dd> <dt>

15
</dt> <dd>

Économie d’énergie

</dd> <dt>

16 (0x10)
</dt> <dd>

Suppression en attente

</dd> <dt>

17 (0x11)
</dt> <dd>

E/s actives

</dd> <dt>

18 (0x12)
</dt> <dd>

Alimentation manuelle

</dd> </dl>

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, l’imprimante est masquée pour les utilisateurs du réseau.

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. HorizontalResolution"), [**unités**](../wmisdk/standard-qualifiers.md) ("pixels par pouce")
</dt> </dl>

Résolution horizontale de l’imprimante (en pixels par pouce).

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")
</dt> </dl>

Date et heure d’installation d’un objet. L’objet peut être installé sans qu’une valeur ne soit écrite dans cette propriété. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**JobCountSinceLastReset**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **compteur**
</dt> </dl>

Nombre de travaux d’impression depuis la dernière réinitialisation de l’imprimante.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**KeepPrintedJobs**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, le spouleur d’impression ne supprime pas les travaux terminés.

</dd> <dt>

**LanguagesSupported**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Imprimante IETF-MIB. prtInterpreterLangFamily "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md). MimeTypesSupported "," CIM \_ PrintJob. Language "," CIM \_ printservice. LanguagesSupported ")
</dt> </dl>

Tableau des langues d’impression prises en charge en mode natif.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span id="PCL"></span><span id="pcl"></span>**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span id="PJL"></span><span id="pjl"></span>**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span id="PS"></span><span id="ps"></span>**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span id="IPDS"></span><span id="ipds"></span>**IPD** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpression** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Données de ligne** (15)


</dt> <dd>

LineData

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span id="MODCA"></span><span id="modca"></span>**MODCA** (16)


</dt> <dd>

DODCA

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span id="REGIS"></span><span id="regis"></span>**Regis** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span id="SCS"></span><span id="scs"></span>**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span id="PDS"></span><span id="pds"></span>**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span id="IGP"></span><span id="igp"></span>**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span id="WPS"></span><span id="wps"></span>**WPS** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span id="LN03"></span><span id="ln03"></span>**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span id="QUIC"></span><span id="quic"></span>**QUIC** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span id="CPAP"></span><span id="cpap"></span>**Pression positive** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Texte simple** (31)


</dt> <dd>

SimpleText

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span id="NPAP"></span><span id="npap"></span>**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span id="DOC"></span><span id="doc"></span>**Doc** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**impressionne** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatique** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span id="LIPS"></span><span id="lips"></span>**Lèvres** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Majuscules** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span id="EXCL"></span><span id="excl"></span>**Excl** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span id="LCDS"></span><span id="lcds"></span>**Écrans plats** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span id="XES"></span><span id="xes"></span>**X** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span id="MIME"></span><span id="mime"></span>**MIME** (47)


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span id="XPS"></span><span id="xps"></span>**XPS** (48)


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span id="PCLXL"></span><span id="pclxl"></span>**Pclxl** (50)


</dt> <dd></dd> </dl>

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Dernier code d’erreur signalé par l’unité logique.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**Local**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, l’imprimante n’est pas attachée à un réseau. Si les propriétés **local** et **réseau** ont toutes les deux la valeur **true**, l’imprimante est une imprimante réseau.

</dd> <dt>

**Lieu**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Emplacement physique de l’imprimante.

Exemple : Bldg. 38, salle 1164

</dd> <dt>

**MarkingTechnology**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Imprimante IETF-MIB. prtMarkerMarkTech ")
</dt> </dl>

Marquage de la technologie utilisée par l’imprimante.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

**LED électrophotographique** (3)


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

**Laser électrophotographique** (4)


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

**Électrophotographique autre** (5)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

**Impact sur le déplacement de la matrice point-tête 9** (6)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

**Impact sur le déplacement de la matrice point-tête 24pin** (7)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

**Impact-déplacement de la matrice des points en-tête** (8)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

**Impact du déplacement de la tête en forme complète** (9)


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

**Bande d’impact** (10)


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

**Impact sur Other** (11)


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

**Jet d’encre aqueux** (12)


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

**Jet d’encre solide** (13)


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

**Autre encre** (14)


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

**Stylet** (15)


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

**Transfert thermique** (16)


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

**Sensibilité thermique** (17)


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

**Diffusion thermique** (18)


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

**Autre température** (19)


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

**Electroerosion** (20)


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

**Électrostatique** (21)


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

**Microfiche photographique** (22)


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

**Photocomposeuse photo** (23)


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

**Photographie autre** (24)


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

**Déposition d’ions** (25)


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

**eBeam** (26)


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

**Typesetter** (27)


</dt> <dd></dd> </dl>

</dd> <dt>

**MaxCopies**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. copies")
</dt> </dl>

Nombre maximal de copies que l’imprimante peut produire pour un seul travail.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**MaxNumberUp**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. NumberUp")
</dt> </dl>

Nombre maximal de pages de flux d’impression que l’imprimante peut afficher sur une feuille de support, par exemple un papier.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**MaxSizeSupported**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (« CIM \_ PrintJob. Jobs »), [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)
</dt> </dl>

Plus grande tâche en tant que flux d’octets, en kilo-octets, que l’imprimante peut accepter. La valeur 0 (zéro) indique qu’aucune limite n’est définie.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**MimeTypesSupported**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md). LanguagesSupported "," CIM \_ PrintJob. mimeTypes "," CIM \_ printservice. MimeTypesSupported ")
</dt> </dl>

Tableau d’explications détaillées sur les types MIME que l’imprimante prend en charge. Si des données sont fournies, la valeur 47 (« MIME ») doit être incluse dans la propriété **LanguagesSupported** .

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Nom de l’imprimante.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**NaturalLanguagesSupported**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Imprimante IETF-MIB. prtLocalizationLanguage "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (" CIM \_ PrintJob. NaturalLanguage ")
</dt> </dl>

Tableau de langues prises en charge pour les chaînes utilisées par l’imprimante pour la sortie des informations de gestion. Doit être conforme à la [norme RFC 1766](https://www.ietf.org/rfc/rfc1766.txt). Par exemple, « fr » est utilisé pour l’anglais.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**Réseau**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, l’imprimante est une imprimante réseau. Si les propriétés **local** et **réseau** ont toutes les deux la valeur **true**, l’imprimante est une imprimante réseau.

</dd> <dt>

**PaperSizesSupported**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau des types de papier pris en charge par l’imprimante.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span id="A"></span><span id="a"></span>**A** (2)


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span id="B"></span><span id="b"></span>**B** (3)


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span id="C"></span><span id="c"></span>**C** (4)


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span id="D"></span><span id="d"></span>**D** (5)


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span id="E"></span><span id="e"></span>**E** (6)


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Lettre** (7)


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Légal** (8)


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**Na-10x13-Envelope** (9)


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**Na-9x12-Envelope** (10)


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**Na-Number-10-enveloppe** (11)


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**Na-7x9-Envelope** (12)


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**Na-9x11-Envelope** (13)


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**Na-10x14-Envelope** (14)


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**Na-Number-9-enveloppe** (15)


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**Na-6x9-Envelope** (16)


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**Na-10x15-Envelope** (17)


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span id="A0"></span><span id="a0"></span>**A0** (18)


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span id="A1"></span><span id="a1"></span>**A1** (19)


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span id="A2"></span><span id="a2"></span>**A2** (20)


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span id="A3"></span><span id="a3"></span>**A3** (21)


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span id="A4"></span><span id="a4"></span>**A4** (22)


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span id="A5"></span><span id="a5"></span>**A5** (23)


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span id="A6"></span><span id="a6"></span>**A6** (24)


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span id="A7"></span><span id="a7"></span>**A7** (25)


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span id="A8"></span><span id="a8"></span>**A8** (26)


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span id="B0"></span><span id="b0"></span>**B0** (28)


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span id="B1"></span><span id="b1"></span>**B1** (29)


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span id="B2"></span><span id="b2"></span>**B2** (30)


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span id="B3"></span><span id="b3"></span>**B3** (31)


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span id="B4"></span><span id="b4"></span>**B4** (32)


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span id="B5"></span><span id="b5"></span>**B5** (33)


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span id="B6"></span><span id="b6"></span>**B6** (34)


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span id="B7"></span><span id="b7"></span>**B7** (35)


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span id="B8"></span><span id="b8"></span>**B8** (36)


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span id="B9"></span><span id="b9"></span>**B9** (37)


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span id="B10"></span><span id="b10"></span>**B10** (38)


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span id="C0"></span><span id="c0"></span>**C0** (39)


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span id="C1"></span><span id="c1"></span>**C1** (40)


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)


</dt> <dd>

C2

</dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span id="C4"></span><span id="c4"></span>**C4** (42)


</dt> <dd>

C3

</dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span id="C5"></span><span id="c5"></span>**C5** (43)


</dt> <dd>

C4

</dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span id="C6"></span><span id="c6"></span>**C6** (44)


</dt> <dd>

C5

</dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span id="C7"></span><span id="c7"></span>**C7** (45)


</dt> <dd>

C6

</dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span id="C8"></span><span id="c8"></span>**C8** (46)


</dt> <dd>

C7

</dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**Désignée ISO** (47)


</dt> <dd>

C8

</dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)


</dt> <dd>

ISO-Designated

</dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)


</dt> <dd>

JIS B0

</dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)


</dt> <dd>

JIS B1

</dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)


</dt> <dd>

JIS B2

</dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)


</dt> <dd>

JIS B3

</dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)


</dt> <dd>

JIS B4

</dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)


</dt> <dd>

JIS B5

</dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)


</dt> <dd>

JIS B6

</dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)


</dt> <dd>

JIS B7

</dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)


</dt> <dd>

JIS B8

</dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)


</dt> <dd>

JIS B9

</dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**Lettre na** (59)


</dt> <dd>

JIS B10

</dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**Na-Legal** (60)


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**B4-enveloppe** (61)


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**B5-enveloppe** (62)


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**C3-enveloppe** (63)


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**C4-enveloppe** (64)


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**C5-enveloppe** (65)


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**C6-enveloppe** (66)


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Enveloppe indiquée-long** (67)


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Monarch-enveloppe** (68)


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (69)


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Folio** (70)


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Facture** (71)


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Grand livre** (72)


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Papier Quarto** (73)


</dt> <dd></dd> </dl>

</dd> <dt>

**PaperTypesAvailable**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. RequiredPaperType", "CIM \_ printservice. PaperTypesAvailable"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Imprimante IETF-MIB. prtInputMediaName ")
</dt> </dl>

Tableau de types de papier actuellement disponibles sur l’imprimante. Chaque chaîne doit être exprimée dans le format spécifié par l’application d’impression des documents ISO/IEC 10175 (DPA), qui est résumée dans l’annexe C de la [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (MIB de l’imprimante). Toute taille de papier identifiée dans cette propriété doit également apparaître dans la propriété **PaperSizesSupported** .

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

Exemple : ISO-A4-couleur

</dd> <dt>

**Paramètres**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Paramètres facultatifs du processeur d’impression.

Exemple : « copies = 2 »

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Windows Identificateur d’appareil Plug-and-Play de l’unité logique.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

Exemple : \* PNP030b

</dd> <dt>

**PortName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Port utilisé pour transmettre des données à une imprimante. Si une imprimante est connectée à plusieurs ports, les noms de chaque port sont séparés par des virgules.

Exemple : LPT1 :, LPT2 :, LPT3 :

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.

Cette propriété est héritée de **CIM \_ LogicalDevice**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)


</dt> <dd>

Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)


</dt> <dd>

L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)


</dt> <dd>

La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge. Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée. Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)


</dt> <dd>

La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)


</dt> <dd>

Power-On chronométré pris en charge

La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, la puissance de l’appareil peut être gérée, ce qui signifie qu’il peut être mis en mode de suspension. La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**PrinterPaperNames**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de formats de papier pris en charge par l’imprimante. Les noms spécifiés par l’imprimante sont utilisés pour représenter les formats de papier pris en charge.

Exemple : B5 (JIS)

</dd> <dt>

**PrinterState**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

L’un des États possibles associés à cette imprimante. Cette propriété est obsolète. À la place de cette propriété, utilisez **PrinterStatus**.

<dt>

0
</dt> <dd>

Inactif-pour plus d’informations, consultez la section Notes ci-dessous.

</dd> <dt>

1
</dt> <dd>

Suspendu

</dd> <dt>

2
</dt> <dd>

Erreur

</dd> <dt>

3
</dt> <dd>

Suppression en attente

</dd> <dt>

4
</dt> <dd>

Bourrage papier

</dd> <dt>

5
</dt> <dd>

Papier sortant

</dd> <dt>

6
</dt> <dd>

Alimentation manuelle

</dd> <dt>

7
</dt> <dd>

Problème de papier

</dd> <dt>

8
</dt> <dd>

Hors connexion

</dd> <dt>

9
</dt> <dd>

E/s actives

</dd> <dt>

10
</dt> <dd>

Busy

</dd> <dt>

11
</dt> <dd>

Impression

</dd> <dt>

12
</dt> <dd>

Bac de réception plein

</dd> <dt>

13
</dt> <dd>

Non disponible

</dd> <dt>

14
</dt> <dd>

En attente

</dd> <dt>

15
</dt> <dd>

Traitement en cours

</dd> <dt>

16
</dt> <dd>

Initialisation

</dd> <dt>

17
</dt> <dd>

Préchauffage

</dd> <dt>

18
</dt> <dd>

Toner faible

</dd> <dt>

19
</dt> <dd>

Il n'y a plus d'encre

</dd> <dt>

20
</dt> <dd>

Page chargeur

</dd> <dt>

21
</dt> <dd>

Intervention de l’utilisateur requise

</dd> <dt>

22
</dt> <dd>

Mémoire insuffisante

</dd> <dt>

23
</dt> <dd>

Capot ouvert

</dd> <dt>

24
</dt> <dd>

Serveur \_ inconnu

</dd> <dt>

25
</dt> <dd>

Économie d’énergie

</dd> </dl>

</dd> <dt>

**PrinterStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Imprimante IETF-MIB. hrPrinterStatus ")
</dt> </dl>

Informations d’État pour une imprimante qui diffèrent de celles spécifiées dans la propriété de **disponibilité** de l’unité logique.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inactif** (3)


</dt> <dd>

Inactif-pour plus d’informations, consultez la section Notes ci-dessous.

</dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Impression** (4)


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Préchauffage** (5)


</dt> <dd>

Préchauffage

</dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Impression arrêtée** (6)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**PrintJobDataType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

type de données d’un travail d’impression en attente du périphérique d’impression Windows.

</dd> <dt>

**PrintProcessor**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nom du spouleur d’impression qui gère les travaux d’impression.

Exemple : SPOOLSS.DLL

</dd> <dt>

**Priorité**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Priorité de l’imprimante. Les travaux sur une imprimante de priorité supérieure sont planifiés en premier.

</dd> <dt>

**Publié**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, l’imprimante est publiée dans le service d’annuaire réseau.

</dd> <dt>

**Mis en file d'attente.**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, l’imprimante met en mémoire tampon et met en file d’attente les travaux d’impression.

</dd> <dt>

**RawOnly**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, l’imprimante accepte uniquement les données brutes à mettre en file d’attente.

</dd> <dt>

**SeparatorFile**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nom du fichier utilisé pour créer une page de séparation. Cette page est utilisée pour séparer les travaux d’impression envoyés à l’imprimante.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du serveur qui contrôle l’imprimante. Si cette chaîne est **null**, l’imprimante est contrôlée localement.

</dd> <dt>

**Partagé**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, l’imprimante est disponible en tant que ressource réseau partagée.

</dd> <dt>

**ShareName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

nom de partage du périphérique d’impression basé sur Windows.

Exemple : « \\ \\ PRINTSERVER1 \\ .

</dd> <dt>

**SpoolEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Cette propriété est obsolète. n’utilisez pas. Si la **valeur est true**, la mise en file d’attente est activée pour l’imprimante.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Date et heure auxquelles une imprimante peut commencer à imprimer un travail : si l’imprimante est limitée à une impression à des moments spécifiques. Cette valeur est exprimée sous la forme du temps écoulé depuis 12:00 AM GMT (heure de Greenwich).

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

État actuel de l’objet. Divers États opérationnels et inopérationnels peuvent être définis. Les États opérationnels sont les suivants : **OK**, **détérioré** et **prédit échec** (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche). Les États qui ne sont pas opérationnels sont les suivants : **erreur**, **démarrage**, **arrêt** et **service**. Cette dernière, **service**, peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives. Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni **OK** ni dans l’un des autres États.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Les valeurs sont notamment les suivantes :

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** (« OK »)


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erreur** (« erreur »)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Détérioré** (« détérioré »)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** ("inconnu")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Échec** prévu (« échec prédit »)


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Démarrage** en cours (« démarrage »)


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arrêt** en cours (« arrêt »)


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Service** (« service »)


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** (« stressed »)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Non **récupéré** (« non récupéré »)


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Aucun contact** (« aucun contact »)


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Communication perdue** (« inversée comm »)


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")
</dt> </dl>

État de l’unité logique. Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (**non applicable**) doit être utilisée.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Activé** (3)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Désactivé** (4)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicable** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nom du système d’étendue.

Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de la dernière réinitialisation de l’imprimante.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Date et heure auxquelles une imprimante peut imprimer la dernière tâche : si l’imprimante est limitée à une impression à des moments spécifiques. Cette valeur est exprimée sous la forme du temps écoulé depuis 12:00 AM GMT (heure de Greenwich).

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. HorizontalResolution"), [**unités**](../wmisdk/standard-qualifiers.md) ("pixels par pouce")
</dt> </dl>

Résolution verticale, en pixels par pouce, de l’imprimante.

Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).

</dd> <dt>

**WorkOffline**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, vous pouvez faire une mise en file d’attente des travaux d’impression sur l’ordinateur lorsque l’imprimante est hors connexion.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ Printer** est dérivée de l' [**\_ imprimante CIM**](cim-printer.md). avant d’appeler [**SWbemObject. \_ Put**](../wmisdk/swbemobject-put-.md) ou [**IWbemServices ::P utinstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) pour une instance d' **\_ imprimante Win32** , le privilège **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** pour Visual Basic et LoadDriver pour les monikers de script) doit être activé. Pour plus d’informations, consultez [**constantes de privilège**](../wmisdk/privilege-constants.md) et [exécution d’opérations privilégiées](../wmisdk/executing-privileged-operations.md). L’exemple de code VBScript suivant montre comment activer le privilège **SetLoadDriverPrivilege** dans le script.

pour travailler avec des clusters d’imprimantes MSCS, utilisez l’assembly prnadmin.dll ou l’espace de noms [System. printing](/dotnet/api/system.printing) .NET Framework.


```VB
Set objPrinter = GetObject("winmgmts:{impersonationLevel=Impersonate,(LoadDriver)}!//./Root/CIMv2:Win32_Printer")
```



Windows utilise les informations d’identification de l’utilisateur qui exécute le script pour déterminer les imprimantes disponibles. Par conséquent, si vous exécutez un script à distance, vous ne pourrez peut-être accéder qu’aux imprimantes disponibles pour votre compte d’utilisateur sur ce système distant.

Vous ne pouvez pas utiliser la classe d' **\_ imprimante Win32** pour les imprimantes sur un cluster d’impression MSCS. au lieu de cela, vous devrez peut-être utiliser l’outil PrinterAdmin (PrnAdmin.dll) ou l’espace de noms [System. printing](/dotnet/api/system.printing) .NET Framework.

> [!Note]  
> Si vous récupérez **PrinterStatus** = 3 ou **PrinterState** = 0, il se peut que le pilote d’imprimante n’alimente pas correctement les informations dans WMI. WMI récupère les informations de l’imprimante à partir du processus de spoolsv.exe. Il est possible que le pilote d’imprimante ne signale pas son état au spouleur. Dans ce cas, **l' \_ imprimante Win32** signale l’imprimante comme étant **inactive**.

 

## <a name="examples"></a>Exemples

l’exemple [PS créer un dessin de Configuration d’ordinateur à l’aide de Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sur la galerie TechNet utilise l' **\_ imprimante Win32** pour interagir avec Visio modèle automation afin de créer un Visio dessin.

Le [script PowerShell Remote PC info](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) utilise un certain nombre de classes, y compris **Win32 \_ Printer**, pour récupérer des informations sur un ordinateur distant.

L’exemple de code PowerShell suivant montre comment déterminer l’imprimante par défaut de l’ordinateur local.


```PowerShell
Get-WmiObject win32_printer | %{if ($_.default) {$_}}
```



L’exemple de code VBScript suivant décrit comment récupérer des statistiques d’imprimante à partir des instances d’une **\_ imprimante Win32**.


```VB
Set PrinterSet = GetObject("winmgmts:").InstancesOf ("Win32_Printer")
If (PrinterSet.Count = 0 ) Then WScript.Echo "No Printers Installed!"
for each Printer in PrinterSet
   if Printer.PrinterStatus = 3 then WScript.Echo Printer.Name & Chr(13) & "Status:  Idle"
   if Printer.PrinterStatus = 4 then WScript.Echo Printer.Name & Chr(13) & "Status:  Printing"
   
next
```



L’exemple de code perl suivant décrit comment récupérer des statistiques d’imprimante à partir des instances d’une **\_ imprimante Win32**.


```
use strict;
use Win32::OLE;

my $PrinterSet;

eval { $PrinterSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf ("Win32_Printer"); };
unless($@)
{
   if ($PrinterSet->{Count} == 0) 
   {
      print "No Printers Installed!\n";
   }

   foreach my $PrinterInst (in $PrinterSet)
   {
      if ($PrinterInst->{PrinterStatus} == 3) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Idle\n";
      }
      if ($PrinterInst->{PrinterStatus} == 4) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Printing\n";
      }
   }
}
else
{
   print STDERR Win32::OLE->LastError, "\n";
}
```



L’exemple de code VBScript suivant montre comment obtenir le nom de l’imprimante par défaut d’un ordinateur.


```VB
strComputer = "."
Set objWMIService = GetObject( "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colInstalledPrinters =  objWMIService.ExecQuery ("Select * from Win32_Printer")
For Each objPrinter in colInstalledPrinters

    If objPrinter.Default = "True" Then 
      Wscript.Echo "Name: " & objPrinter.Name
    End If
Next
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Imprimante CIM**](cim-printer.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> <dt>

[Tâches WMI : imprimantes et impression](../wmisdk/wmi-tasks--printers-and-printing.md)
</dt> </dl>

 

 
