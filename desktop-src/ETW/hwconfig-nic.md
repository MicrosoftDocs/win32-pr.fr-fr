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
ms.openlocfilehash: 1d9b82f8a97c1ca47734b5bb0a1db09167510978c53f86870df01f2acc59b2ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394723"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 




