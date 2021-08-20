---
description: Utilisé pour signaler des informations d’État ou d’erreur en réponse à une commande de détection de requête SCSI.
ms.assetid: 43B2FE98-1468-4457-AB7D-3038C16E20B6
title: Structure de SENSE_DATA (SCSI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SENSE_DATA
api_type:
- HeaderDef
api_location:
- Scsi.h
ms.openlocfilehash: 2f6b3bd9fd4353e396bc7fe4ff7273e598704d1348062fec1c2f64aed9380686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075952"
---
# <a name="sense_data-structure"></a>Structure de données de sens \_

Utilisé pour signaler des informations d’État ou d’erreur en réponse à une commande de **détection de requête** SCSI.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _SENSE_DATA {
  UCHAR  ErrorCode  :7;
  UCHAR  Valid  :1;
  UCHAR  SegmentNumber;
  UCHAR  SenseKey  :4;
  UCHAR  Reserved  :1;
  UCHAR  IncorrectLength  :1;
  UCHAR  EndOfMedia  :1;
  UCHAR  FileMark  :1;
  UCHAR  Information[4];
  UCHAR  AdditionalSenseLength;
  UCHAR  CommandSpecificInformation[4];
  UCHAR  AdditionalSenseCode;
  UCHAR  AdditionalSenseCodeQualifier;
  UCHAR  FieldReplaceableUnitCode;
  UCHAR  SenseKeySpecific[3];
} SENSE_DATA, *PSENSE_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**ErrorCode**
</dt> <dd>

Type de rapport.



| Valeur                                                                           | Signification                     |
|---------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>0x70</dt> </dl> | Erreurs en cours.<br/>  |
| <dl> <dt>0x71</dt> </dl> | Erreurs différées.<br/> |



 

</dd> <dt>

**Valide**
</dt> <dd>

1 si le champ d' **information** est défini dans une norme ; dans le cas contraire, le champ d' **information** est spécifique au fournisseur et n’est pas défini par une norme.

</dd> <dt>

**SegmentNumber**
</dt> <dd>

Obsolète.

</dd> <dt>

**SenseKey**
</dt> <dd>

Indique la catégorie de l’erreur.

<dl> <dt>

<span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**Aucun sens** (0x0)
</dt> <dt>

<span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Erreur Récupérée** (0x1)
</dt> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (0X2)
</dt> <dt>

<span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Erreur moyenne** (0x3)
</dt> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Erreur matérielle** (0x4)
</dt> <dt>

<span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Demande non conforme** (0x5)
</dt> <dt>

<span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Attention** sur l’unité (0x6)
</dt> <dt>

<span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Protection des données** (0x7)
</dt> <dt>

<span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Erreur du microprogramme** (0x9)
</dt> <dt>

<span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Commande abandonnée** (0xB)
</dt> <dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Égal** à (0xc)
</dt> <dt>

<span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Dépassement de volume** (0xD)
</dt> <dt>

<span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Comparaison** inversée (0xE)
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Réservé.

</dd> <dt>

**IncorrectLength**
</dt> <dd>

1 si la longueur de bloc logique demandée ne correspond pas à la longueur de bloc logique des données sur le support.

</dd> <dt>

**EndOfMedia**
</dt> <dd>

1 si un appareil à accès séquentiel a atteint la fin du support ou si une imprimante n’est plus à blanc.

</dd> <dt>

**Marque**
</dt> <dd>

1 si la commande active a atteint un SETMARK ou un. Valide uniquement pour les appareils à accès séquentiel.

</dd> <dt>

**Informations**
</dt> <dd>

Données spécifiques à un type d’appareil ou à une commande.

</dd> <dt>

**AdditionalSenseLength**
</dt> <dd>

Longueur, en octets, du reste de la structure. Longueur totale moins 7.

</dd> <dt>

**CommandSpecificInformation**
</dt> <dd>

Données spécifiques à la commande. Les valeurs sont définies dans la norme de commande appropriée.

</dd> <dt>

**AdditionalSenseCode**
</dt> <dd>

Code spécifique à l’appareil qui décrit l’erreur signalée dans le champ **SenseKey** .

</dd> <dt>

**AdditionalSenseCodeQualifier**
</dt> <dd>

Peut contenir des détails supplémentaires sur le champ **AdditionalSenseCode** .

</dd> <dt>

**FieldReplaceableUnitCode**
</dt> <dd>

Informations spécifiques au fournisseur sur le composant associé à ces données de sens.

</dd> <dt>

**SenseKeySpecific**
</dt> <dd>

Le contenu et le format des informations spécifiques à la clé de détection sont déterminés par la valeur du champ **SenseKey** .

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour plus d’informations sur le format de données de sens, consultez [commande SCSI Request sens](https://wikipedia.org/wiki/SCSI_command) ( https://wikipedia.org/wiki/SCSI_command) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>SCSI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Transfert de cible iSCSI](/powershell/module/iscsi)
</dt> <dt>

[\_transfert \_ direct via \_ le SCSI](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 




