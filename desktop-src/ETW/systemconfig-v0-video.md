---
description: 'Classe SystemConfig_V0_Video : cette classe est la classe de type d’événement pour les événements de configuration vidéo.'
ms.assetid: 06aab3a3-a55e-4eb8-897a-2ad8349e5900
title: Classe SystemConfig_V0_Video
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Video
- SystemConfig_V0_Video.MemorySize
- SystemConfig_V0_Video.XResolution
- SystemConfig_V0_Video.YResolution
- SystemConfig_V0_Video.BitsPerPixel
- SystemConfig_V0_Video.VRefresh
- SystemConfig_V0_Video.ChipType
- SystemConfig_V0_Video.DACType
- SystemConfig_V0_Video.AdapterString
- SystemConfig_V0_Video.BiosString
- SystemConfig_V0_Video.DeviceId
- SystemConfig_V0_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7121d56d2acf0890a75bccdaf397f184c8780f1f1d3152d3ce2ea4db7781ecaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151368"
---
# <a name="systemconfig_v0_video-class"></a>\_ \_ Classe vidéo SystemConfig v0

Cette classe est la classe de type d’événement pour les événements de configuration vidéo.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_V0_Video : SystemConfig_V0
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

La **classe \_ \_ vidéo SystemConfig v0** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ vidéo SystemConfig v0** possède ces propriétés.

<dl> <dt>

**AdapterString**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (8), **Max** (256)
</dt> </dl>

Nom ou description de l’adaptateur.

</dd> <dt>

**BiosString**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (9), **Max** (256)
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

Qualificateurs : **WmiDataId** (6), **Max** (256)
</dt> </dl>

Nom de la carte.

</dd> <dt>

**DACType**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (7), **Max** (256)
</dt> </dl>

Nom de la puce de conversion numérique-analogique (DAC) de l’adaptateur.

</dd> <dt>

**DeviceId**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (10), **Max** (256)
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

Qualificateurs : **WmiDataId** (11)
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
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemConfig \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 




