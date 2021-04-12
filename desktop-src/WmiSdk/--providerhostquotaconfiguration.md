---
description: Permet de définir des limites sur l’utilisation des ressources système par le processus hôte.
ms.assetid: 5f5ed1c6-bd1a-406d-a682-7a52059d9450
ms.tgt_platform: multiple
title: Classe __ProviderHostQuotaConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderHostQuotaConfiguration
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 443d66c8e508346444e98a92b341f1e7d67d8cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203161"
---
# <a name="__providerhostquotaconfiguration-class"></a>\_\_ProviderHostQuotaConfiguration, classe

La classe système **\_ \_ ProviderHostQuotaConfiguration** est une classe de configuration pour les processus des fournisseurs hôtes. Cette classe réside dans l’espace de noms racine et permet de définir des limites sur l’utilisation des ressources système par le processus hôte.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __ProviderHostQuotaConfiguration : __SystemClass
{
  uint32 ThreadsPerHost;
  uint32 HandlesPerHost;
  uint32 ProcessLimitAllHosts;
  uint64 MemoryPerHost;
  uint64 MemoryAllHosts;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ ProviderHostQuotaConfiguration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ ProviderHostQuotaConfiguration** possède les propriétés suivantes.

<dl> <dt>

**HandlesPerHost**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nombre de handles d’objets noyau que chaque hôte peut avoir.

</dd> <dt>

**MemoryAllHosts**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Quantité combinée de mémoire privée en octets qui peut être détenue par tous les ordinateurs hôtes.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**MemoryPerHost**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Quantité de mémoire privée qui peut être détenue par chaque hôte.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**ProcessLimitAllHosts**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nombre total de processus hôtes qui peuvent s’exécuter simultanément.

</dd> <dt>

**ThreadsPerHost**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nombre de threads appartenant à un hôte.

</dd> </dl>

## <a name="remarks"></a>Notes

Les propriétés qui représentent des limites peuvent être modifiées, mais étant donné que la classe est un singleton, tous les hôtes du fournisseur partagent les mêmes limites.

Les paramètres suivants sont utilisés lors de la configuration des limites de l’objet de tâche pour l’objet de travail hôte :

-   **MemoryAllHosts**
-   **MemoryPerHost**
-   **ProcessLimitAllHosts**
-   **ThreadsPerHost**

Le processus hôte interroge l’utilisation du handle et quitte le processus si le quota **HandlesPerHost** est violé. Les modifications apportées à ces valeurs prennent effet après le redémarrage de l’ordinateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

