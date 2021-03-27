---
description: Cette classe est la classe de type d’événement pour les événements de configuration de l’alimentation. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 7065b0b0-9a1d-4fce-a494-5762d5efb239
title: Classe SystemConfig_Power
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Power
- SystemConfig_Power.s1
- SystemConfig_Power.s2
- SystemConfig_Power.s3
- SystemConfig_Power.s4
- SystemConfig_Power.s5
- SystemConfig_Power.Pad1
- SystemConfig_Power.Pad2
- SystemConfig_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: d27586451f944ac9c94e9ec2d204035c21f37679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972110"
---
# <a name="systemconfig_power-class"></a>\_Classe SystemConfig Power

Cette classe est la classe de type d’événement pour les événements de configuration de l’alimentation.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_Power : SystemConfig
{
  uint8 s1;
  uint8 s2;
  uint8 s3;
  uint8 s4;
  uint8 s5;
  uint8 Pad1;
  uint8 Pad2;
  uint8 Pad3;
};
```

## <a name="members"></a>Membres

La classe **SystemConfig \_ Power** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ d’alimentation SystemConfig** a ces propriétés.

<dl> <dt>

Pad1
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (6)
</dt> </dl>

Non utilisé.

</dd> <dt>

Pad2
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (7)
</dt> </dl>

Non utilisé.

</dd> <dt>

Pad3
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (8)
</dt> </dl>

Non utilisé.

</dd> <dt>

s1
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1)
</dt> </dl>

True indique que le système prend en charge l’état de veille S1.

</dd> <dt>

s2
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2)
</dt> </dl>

True indique que le système prend en charge l’état de veille S2.

</dd> <dt>

s3
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3)
</dt> </dl>

True indique que le système prend en charge l’état de veille S3.

</dd> <dt>

S4
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4)
</dt> </dl>

True indique que le système prend en charge l’état de veille S4.

</dd> <dt>

S5
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (5)
</dt> </dl>

La valeur true indique que le système prend en charge l’état de veille S5.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




