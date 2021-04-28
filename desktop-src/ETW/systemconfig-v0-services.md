---
description: Classe SystemConfig_V0_Services-cette classe est la classe de type d’événement pour les événements de configuration de service.
ms.assetid: 1e6c2061-f1a2-4253-a0c4-4b45b2feceda
title: Classe SystemConfig_V0_Services
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Services
- SystemConfig_V0_Services.ServiceName
- SystemConfig_V0_Services.DisplayName
- SystemConfig_V0_Services.ProcessName
- SystemConfig_V0_Services.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: b69ca7cf4ee4e16a5fbcb6a5f10c659f713ab458
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105927"
---
# <a name="systemconfig_v0_services-class"></a>\_Classe SystemConfig v0 \_ services

Cette classe est la classe de type d’événement pour les événements de configuration de service.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_V0_Services : SystemConfig_V0
{
  char16 ServiceName[];
  char16 DisplayName[];
  char16 ProcessName[];
  uint32 ProcessId;
};
```

## <a name="members"></a>Membres

La classe **SystemConfig \_ v0 \_ services** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **SystemConfig \_ v0 \_ services** possède ces propriétés.

<dl> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (2), **Max** (256)
</dt> </dl>

Nom complet du service. Le nom est conservé dans le gestionnaire de contrôle des services. Toutefois, les comparaisons de noms complets ne respectent jamais pas la casse.

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (4)
</dt> </dl>

Identificateur du processus dans lequel le service s’exécute.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (3), **Max** (34)
</dt> </dl>

Nom du processus dans lequel le service s’exécute.

</dd> <dt>

**FormName**
</dt> <dd> <dl> <dt>

Type de données : tableau **char16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **WmiDataId** (1), **Max** (34)
</dt> </dl>

Identificateur unique du service. L’identificateur fournit une indication de la fonctionnalité fournie par le service.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemConfig \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 




