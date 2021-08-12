---
description: utilisé pour inscrire des fournisseurs d’événements avec Windows Management Instrumentation (WMI).
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: Classe __EventProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: ce973f05aec0a1c859598c558ef8c2cc637a8faec22fd1d7f2ad2aaf383bd201
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557943"
---
# <a name="__eventproviderregistration-class"></a>\_\_EventProviderRegistration, classe

la classe système **\_ \_ EventProviderRegistration** est utilisée pour enregistrer des fournisseurs d’événements avec Windows Management Instrumentation (WMI).

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ EventProviderRegistration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ EventProviderRegistration** possède les propriétés suivantes.

<dl> <dt>

**EventQueryList**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

une ou plusieurs requêtes WQL (Windows Management Instrumentation Query Language) qui décrivent les événements pris en charge par le fournisseur d’événements.

</dd> <dt>

**moteur**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ fournisseur**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès de l’objet au fournisseur d’événements. Cette propriété est héritée de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

Seuls les administrateurs peuvent inscrire ou supprimer un fournisseur d’événements en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et [**\_ \_ EventProviderRegistration**](--eventconsumerproviderregistration.md). La classe **\_ \_ EventProviderRegistration** est dérivée de [**\_ \_ ProviderRegistration**](--providerregistration.md).

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

[Inscription d’un fournisseur d’événements](registering-an-event-provider.md)
</dt> <dt>

[Écriture d’un fournisseur d’événements](writing-an-event-provider.md)
</dt> </dl>

 

