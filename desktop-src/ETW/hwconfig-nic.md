---
description: La \_ classe de carte réseau HWConfig est la classe de type d’événement pour les événements de configuration de carte d’interface réseau. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: e544a27b-17f8-402c-9c92-578cf2a38ca8
title: Classe HWConfig_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_NIC
- HWConfig_NIC.NICName
api_type:
- NA
api_location: ''
ms.openlocfilehash: df3897c67ed65eeec5ace49dac1088ca35223a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035098"
---
# <a name="hwconfig_nic-class"></a>\_Classe de carte réseau HWConfig

La classe de **\_ carte réseau HWConfig** est la classe de type d’événement pour les événements de configuration de carte d’interface réseau.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(13), EventTypeName("NIC")]
class HWConfig_NIC : HWConfig
{
  string NICName;
};
```

## <a name="members"></a>Membres

La classe de **\_ carte réseau HWConfig** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ carte réseau HWConfig** a ces propriétés.

<dl> <dt>

NICName
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), StringTermination ("NullTerminated"), format ("w")
</dt> </dl>

Nom de la carte d’interface réseau.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 




