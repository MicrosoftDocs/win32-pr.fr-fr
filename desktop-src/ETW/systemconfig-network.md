---
description: Cette classe est la classe de type d’événement pour les événements réseau. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: afa994ef-dd1c-4909-a6cd-7021be4fff40
title: Classe SystemConfig_Network
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Network
- SystemConfig_Network.TcbTablePartitions
- SystemConfig_Network.MaxHashTableSize
- SystemConfig_Network.MaxUserPort
- SystemConfig_Network.TcpTimedWaitDelay
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6b196e8c1ad5a997642cc48491e9d1a4b5e73bc26db71d5ea5258f7cf162a00a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069689"
---
# <a name="systemconfig_network-class"></a>\_Classe de réseau SystemConfig

Cette classe est la classe de type d’événement pour les événements réseau.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(17), EventTypeName("Network")]
class SystemConfig_Network : SystemConfig
{
  uint32 TcbTablePartitions;
  uint32 MaxHashTableSize;
  uint32 MaxUserPort;
  uint32 TcpTimedWaitDelay;
};
```

## <a name="members"></a>Membres

La classe de **\_ réseau SystemConfig** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ réseau SystemConfig** a ces propriétés.

<dl> <dt>

**MaxHashTableSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2)
</dt> </dl>

Taille de la table de hachage dans laquelle les blocs de contrôle TCP (TCBs) sont stockés. Le protocole TCP stocke les blocs de contrôle dans une table de hachage afin qu’il puisse les trouver très rapidement.

</dd> <dt>

**MaxUserPort**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3)
</dt> </dl>

Le numéro de port le plus élevé que TCP peut attribuer lorsqu’une application demande un port utilisateur disponible à partir du système. En règle générale, les ports éphémères (ceux utilisés brièvement) sont alloués aux numéros de port 1024 à 5000.

La valeur du numéro de port utilisateur le plus élevé que TCP peut attribuer est contrôlée par un paramètre du Registre. Pour plus d’informations, consultez [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).

</dd> <dt>

**TcbTablePartitions**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1)
</dt> </dl>

Nombre de partitions dans la table des blocs de contrôle de transport. Le partitionnement de la table de blocs de contrôle de transport minimise la contention pour l’accès aux tables. Cela s’avère particulièrement utile sur les systèmes multiprocesseurs.

</dd> <dt>

**TcpTimedWaitDelay**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4)
</dt> </dl>

Temps qui doit s’écouler avant que TCP puisse libérer une connexion fermée et réutiliser ses ressources. Cet intervalle entre la clôture et la mise en version est connu sous le nom d' \_ État d’attente ou d’état 2MSL. Pendant ce temps, la connexion peut être rouverte à un coût plus faible pour le client et le serveur que lors de l’établissement d’une nouvelle connexion.

La norme RFC 793 publiée par l’IETF requiert que TCP maintienne une connexion fermée pendant un intervalle au moins égale à deux fois la durée de vie maximale du segment (2MSL) du réseau. Lorsqu’une connexion est libérée, sa paire de sockets et le bloc de contrôle TCP (TCB) peuvent être utilisés pour prendre en charge une autre connexion. Par défaut, le langage MSL est défini sur 120 secondes, et la valeur de cette entrée est égale à 2 MSLs, soit 4 minutes. Pour plus d’informations, consultez la [RFC 793](https://tools.ietf.org/html/rfc973).

La réduction de la valeur de cette entrée à l’aide d’un paramètre du registre permet à TCP de libérer des connexions fermées plus rapidement, ce qui fournit davantage de ressources pour les nouvelles connexions. Toutefois, si la valeur est trop faible, TCP peut libérer des ressources de connexion avant que la connexion ne soit terminée, ce qui nécessite que le serveur utilise des ressources supplémentaires pour rétablir la connexion.

En règle générale, TCP ne libère pas les connexions fermées tant que la valeur de cette entrée n’a pas expiré. Toutefois, TCP peut libérer des connexions avant que cette valeur n’expire s’il ne manque pas de blocs de contrôle TCP (TCBs). Le nombre de TCBs créés par le système est contrôlé par un paramètre du Registre. Pour plus d’informations, consultez [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 
