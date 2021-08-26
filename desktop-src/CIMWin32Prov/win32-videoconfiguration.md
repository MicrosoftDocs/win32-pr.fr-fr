---
description: La \_ classe VideoConfiguration Win32 n’est pas active. Elle ne retourne pas d’instances, car il n’existe aucun fournisseur qui la sauvegarde.
ms.assetid: 8dd15e8a-ff9b-4e75-bae9-8c80548301ab
ms.tgt_platform: multiple
title: Classe Win32_VideoConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoConfiguration
- Win32_VideoConfiguration.Caption
- Win32_VideoConfiguration.Description
- Win32_VideoConfiguration.SettingID
- Win32_VideoConfiguration.ActualColorResolution
- Win32_VideoConfiguration.AdapterChipType
- Win32_VideoConfiguration.AdapterCompatibility
- Win32_VideoConfiguration.AdapterDACType
- Win32_VideoConfiguration.AdapterDescription
- Win32_VideoConfiguration.AdapterRAM
- Win32_VideoConfiguration.AdapterType
- Win32_VideoConfiguration.BitsPerPixel
- Win32_VideoConfiguration.ColorPlanes
- Win32_VideoConfiguration.ColorTableEntries
- Win32_VideoConfiguration.DeviceSpecificPens
- Win32_VideoConfiguration.DriverDate
- Win32_VideoConfiguration.HorizontalResolution
- Win32_VideoConfiguration.InfFilename
- Win32_VideoConfiguration.InfSection
- Win32_VideoConfiguration.InstalledDisplayDrivers
- Win32_VideoConfiguration.MonitorManufacturer
- Win32_VideoConfiguration.MonitorType
- Win32_VideoConfiguration.Name
- Win32_VideoConfiguration.PixelsPerXLogicalInch
- Win32_VideoConfiguration.PixelsPerYLogicalInch
- Win32_VideoConfiguration.RefreshRate
- Win32_VideoConfiguration.ScanMode
- Win32_VideoConfiguration.ScreenHeight
- Win32_VideoConfiguration.ScreenWidth
- Win32_VideoConfiguration.SystemPaletteEntries
- Win32_VideoConfiguration.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d951a8927458fa12398682ce63963dd71949d70e4db3a426dfc93ad14c78bf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922619"
---
# <a name="win32_videoconfiguration-class"></a>\_Classe VideoConfiguration Win32

La **classe \_ VideoConfiguration Win32** n’est pas active. Elle ne retourne pas d’instances, car il n’existe aucun fournisseur qui la sauvegarde.

La **classe \_ VideoConfiguration Win32** représente une configuration d’un sous-système vidéo. Cette classe a été dépréciée en faveur des propriétés contenues dans les classes [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md)et [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[DEPRECATED, UUID("{8502C4ED-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_VideoConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  uint32   ActualColorResolution;
  string   AdapterChipType;
  string   AdapterCompatibility;
  string   AdapterDACType;
  string   AdapterDescription;
  uint32   AdapterRAM;
  string   AdapterType;
  uint32   BitsPerPixel;
  uint32   ColorPlanes;
  uint32   ColorTableEntries;
  uint32   DeviceSpecificPens;
  datetime DriverDate;
  uint32   HorizontalResolution;
  string   InfFilename;
  string   InfSection;
  string   InstalledDisplayDrivers;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  uint32   RefreshRate;
  string   ScanMode;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  uint32   SystemPaletteEntries;
  uint32   VerticalResolution;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ VideoConfiguration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ VideoConfiguration** a ces propriétés.

<dl> <dt>

**ActualColorResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| COLORRES"), [**unités**](../wmisdk/standard-qualifiers.md) (« bits par pixel »)
</dt> </dl>

Indique la profondeur de couleur actuelle de l’affichage vidéo.

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**AdapterChipType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \\ \\ info \| ChipType")
</dt> </dl>

Contient le nom de la puce de l’adaptateur.

Exemple : S3

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**AdapterCompatibility**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](../wmisdk/standard-wmi-qualifiers.md), [**clé**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

Spécifie le nom du fabricant de l’adaptateur. Ce nom peut être utilisé pour comparer la compatibilité de cet appareil avec les besoins du système informatique.

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**AdapterDACType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \\ \\ info \| DACType")
</dt> </dl>

Indique le nom du processeur numérique-analogique (DAC) utilisé dans l’adaptateur.

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**AdapterDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

Contient une description ou un nom descriptif de la carte vidéo.

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**AdapterRAM**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \\ \\ info \| VideoMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Indique la taille de la mémoire de la carte vidéo.

Exemple : 16777216

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**AdapterType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ description \\ \\ System \\ \\ DisplayController \\ \\ 0 \\ \\ identifier")
</dt> </dl>

Indique le type de carte vidéo.

Jeu de caractères : alphanumérique

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL")
</dt> </dl>

Indique le nombre réel de bits par pixel représentant l’affichage. Elle peut être mise à l’échelle vers le paramètre vidéo actuel (représenté par la propriété ActualColorResolution) de l’utilisateur.

Exemple : 8

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Courte description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**ColorPlanes**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api des \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| ")
</dt> </dl>

Indique le nombre actuel de plans de couleurs utilisés dans l’affichage vidéo. Un plan de couleur est une autre façon de représenter les couleurs des pixels ; au lieu d’affecter une seule valeur RVB à chaque pixel, les plans de couleurs séparent le graphique dans chacun des composants de couleur primaire (rouge vert bleu) et les stockent dans leurs propres plans. Cela permet d’obtenir une plus grande profondeur de couleurs sur les systèmes vidéo 8 et 16 bits. Les systèmes graphiques présentent un bitwidth suffisamment grand pour stocker les informations de profondeur de couleur, ce qui rend nécessaire un seul plan de couleurs.

Exemple : 1

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**ColorTableEntries**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS")
</dt> </dl>

Indique le nombre d’index de couleur dans une table de couleurs pour un affichage vidéo. Cette propriété est utilisée si l’appareil a une profondeur de couleur inférieure ou égale à 8 bits par pixel. Pour les appareils dont la profondeur de couleur est supérieure, la valeur-1 est retournée.

Exemple : 256

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**DeviceSpecificPens**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS")
</dt> </dl>

Indique le nombre actuel de stylets spécifiques à l’appareil. La valeur 0xFFFFFFFF signifie que l’appareil ne prend pas en charge les stylets. Les stylets permettent de dessiner des lignes et des theborders d’objets polygones.

Exemple : 3

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**DriverDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \\ \\ AdapterDescription \| DriverDate")
</dt> </dl>

Indique la date et l’heure d’installation du pilote vidéo actuel.

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES")
</dt> </dl>

Indique le nombre actuel de pixels dans le sens horizontal (axe X) de l’affichage.

Exemple : 1024

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**InfFilename**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \| InfPath")
</dt> </dl>

Spécifie le chemin d’accès au fichier. inf du pilote vidéo.

exemple : C : \\ Windows \\ les \\ pilotes System32

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**InfSection**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \| InfSection")
</dt> </dl>

Indique la section du fichier. inf où se trouvent les informations de vidéo Win32.

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**InstalledDisplayDrivers**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \\ \\ Defaule \| DRV")
</dt> </dl>

Indique le nom du pilote vidéo installé.

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**MonitorManufacturer**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

Indique le nom du fabricant du périphérique d’affichage.

Exemple : NEC

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**Active Directory**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ description \\ \\ System \\ \\ MonitorPeripheral \\ \\ 0 \| identifier")
</dt> </dl>

Indique le nom du modèle du périphérique d’affichage.

Exemple : NEC 5FGp

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](../wmisdk/standard-wmi-qualifiers.md), [**clé**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)
</dt> </dl>

Contient un nom d’identification pour la classe de configuration vidéo.

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**PixelsPerXLogicalInch**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSX")
</dt> </dl>

Indique le nombre de pixels par pouce logique le long de l’axe X (sens horizontal) de l’affichage.

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**PixelsPerYLogicalInch**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSY")
</dt> </dl>

Indique le nombre de pixels par pouce logique le long de l’axe Y (direction verticale) de l’affichage.

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**RefreshRate**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VREFRESH")
</dt> </dl>

Indique la fréquence d’actualisation de la configuration vidéo. Une valeur de 0 ou 1 indique qu’une fréquence par défaut est utilisée.

Exemple : 72

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**ScanMode**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| Device0 \| DefaultSettings. entrelacé")
</dt> </dl>

Indique si le périphérique d’affichage est entrelacé.

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

<dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

**Non entrelacé** (« non entrelacé »)


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

**Entrelacé** (« entrelacé »)


</dt> <dd></dd> </dl>

</dd> <dt>

**ScreenHeight**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTSIZE"), [**unités**](../wmisdk/standard-qualifiers.md) ("millimètres")
</dt> </dl>

Spécifie la hauteur de l’écran physique.

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**Largeur**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZSIZE"), [**unités**](../wmisdk/standard-qualifiers.md) ("millimètres")
</dt> </dl>

Spécifie la largeur de l’écran physique.

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificateur par lequel l’objet actuel est connu.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**SystemPaletteEntries**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| SIZEPALETTE")
</dt> </dl>

Indique le nombre actuel d’entrées d’index de couleurs réservées à l’utilisation du système. Cette valeur est uniquement valide pour les paramètres d’affichage qui utilisent une palette indexée. Les palettes indexées ne sont pas utilisées pour les profondeurs de couleurs supérieurs à 8 bits par pixel. Si la profondeur de couleur est supérieure à 8 bits par pixel, cette valeur est définie sur **null**.

Exemple : 20

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES")
</dt> </dl>

Indique le nombre actuel de pixels dans le sens vertical (axe Y) de l’affichage.

Exemple : 768

Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Paramètre CIM**](cim-setting.md)
</dt> </dl>

 

 
