---
description: Inscrit les fournisseurs de consommateur d’événements avec WMI.
ms.assetid: 31ff43dc-dc70-4ba0-866f-37445912f837
ms.tgt_platform: multiple
title: Classe __EventConsumerProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 38552519221018735c3c7543d9a1f3f2d4b680e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867357"
---
# <a name="__eventconsumerproviderregistration-class"></a>\_\_EventConsumerProviderRegistration, classe

La classe système **\_ \_ EventConsumerProviderRegistration** enregistre les fournisseurs de consommateur d’événements avec WMI.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __EventConsumerProviderRegistration : __ProviderRegistration
{
  string         ConsumerClassNames[];
  __Provider REF provider;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ EventConsumerProviderRegistration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ EventConsumerProviderRegistration** possède les propriétés suivantes.

<dl> <dt>

**ConsumerClassNames**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Tableau de noms des classes de consommateur logiques prises en charge par le fournisseur de consommateur d’événements.

</dd> <dt>

**moteur**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ fournisseur**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès de l’objet au fournisseur. Cette propriété est héritée de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **\_ \_ EventConsumerProviderRegistration** est dérivée de [**\_ \_ ProviderRegistration**](--providerregistration.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_ProviderRegistration**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[Inscription d’un fournisseur de consommateur d’événements](registering-an-event-consumer-provider.md)
</dt> <dt>

[Écriture d’un fournisseur de consommateur d’événements](writing-an-event-consumer-provider.md)
</dt> </dl>

 

