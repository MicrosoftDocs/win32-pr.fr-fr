---
description: 'Classe SystemConfig_Video : cette classe est la classe de type d’événement pour les événements de configuration vidéo.'
ms.assetid: ddb5924b-70d9-4693-bf68-0536c3c3fa8d
title: Classe SystemConfig_Video
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Video
- SystemConfig_Video.MemorySize
- SystemConfig_Video.XResolution
- SystemConfig_Video.YResolution
- SystemConfig_Video.BitsPerPixel
- SystemConfig_Video.VRefresh
- SystemConfig_Video.ChipType
- SystemConfig_Video.DACType
- SystemConfig_Video.AdapterString
- SystemConfig_Video.BiosString
- SystemConfig_Video.DeviceId
- SystemConfig_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 716194eb9ceb67b609f886482393795eaef2ef09
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105897"
---
# <a name="systemconfig_video-class"></a>\_Classe vidéo SystemConfig

Cette classe est la classe de type d’événement pour les événements de configuration vidéo.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_Video : SystemConfig
{
  uint32 MemorySize;
  uint32 XResolution;
  uint32 YResolution;
  uint32 BitsPerPixel;
  uint32 VRefresh;
  char16 ChipType[];
  char16 DACType[];
  char16 AdapterString[];
  char16 BiosString[];
  char16 DeviceId[];
  uint32 StateFlags;
};
```

## <a name="members"></a>Membres

La **classe \_ Video SystemConfig** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ Video SystemConfig** possède les propriétés suivantes.

<dl> <dt>

**AdapterString**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (8), **Max** (256), **format ("s")**
</dt> </dl>

Nom ou description de l’adaptateur.

</dd> <dt>

**BiosString**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (9), **Max** (256), **format ("s")**
</dt> </dl>

Nom du BIOS de la carte.

</dd> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (4)
</dt> </dl>

Nombre de bits utilisés pour afficher chaque pixel.

</dd> <dt>

**ChipType**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (6), **Max** (256), **format ("s")**
</dt> </dl>

Nom de la carte.

</dd> <dt>

**DACType**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (7), **Max** (256), **format ("s")**
</dt> </dl>

Nom de la puce de conversion numérique-analogique (DAC) de l’adaptateur.

</dd> <dt>

**DeviceId**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (10), **Max** (256), **format ("s")**
</dt> </dl>

Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.

</dd> <dt>

**MemorySize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (1)
</dt> </dl>

Quantité maximale de mémoire prise en charge, en octets.

</dd> <dt>

**StateFlags**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (11), **format ("x")**
</dt> </dl>

Indicateurs d’état de l’appareil. Il peut s’agir d’une combinaison raisonnable des éléments suivants.



| Valeur                                                                                                                                                                                                                                                                                        | Signification                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <dt>**Afficher \_ APPAREIL \_ attaché \_ au \_ Bureau**</dt> <dt>1 (0x1)</dt> </dl> | L’appareil fait partie du bureau.<br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <dt>**Afficher \_ \_ \_ Pilote de mise en miroir des appareils**</dt> <dt>8 (0x8)</dt> </dl>           | Représente un Pseudo-appareil utilisé pour mettre en miroir le dessin d’application pour se connecter à un ordinateur distant ou à d’autres fins. Un Pseudo-analyse invisible est associé à cet appareil. Par exemple, NetMeeting l’utilise.<br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <dt>**Afficher \_ \_MODESPRUNED d’appareil**</dt> <dt>134217728 (0x8000000)</dt> </dl>             | L’appareil a plus de modes d’affichage que la prise en charge de ses appareils de sortie.<br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <dt>**Afficher \_ \_ \_ Périphérique principal**</dt> de l’appareil <dt>4 (0x4)</dt> </dl>                 | Le bureau principal se trouve sur l’appareil. Pour un système avec une carte d’affichage unique, cette valeur est toujours définie. Pour un système avec plusieurs cartes d’affichage, un seul appareil peut avoir cet ensemble.<br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <dt>**Afficher \_ APPAREIL \_ amovible**</dt> <dt>32 (0x20)</dt> </dl>                               | L’appareil est amovible ; il ne peut pas être l’affichage principal.<br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <dt>**Afficher \_ PÉRIPHÉRIQUE \_ \_ compatible VGA**</dt> <dt>16 (0x10)</dt> </dl>               | L’appareil est compatible VGA.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

**VRefresh**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (5)
</dt> </dl>

Fréquence d’actualisation actuelle, en Hertz.

</dd> <dt>

**XResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (2)
</dt> </dl>

Nombre actuel de pixels horizontaux.

</dd> <dt>

**YResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (3)
</dt> </dl>

Nombre actuel de pixels verticaux.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




