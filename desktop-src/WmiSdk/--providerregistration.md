---
description: Sert de classe parente pour les classes d’inscription de différents types de fournisseurs.
ms.assetid: 1e5d95cb-0961-4be8-b80a-37b598c9ccfe
ms.tgt_platform: multiple
title: Classe __ProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 21947e2095577651412569737eaa135218519b7962fae7a1c96b6827833b37c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110311"
---
# <a name="__providerregistration-class"></a>\_\_ProviderRegistration, classe

La classe système abstraite **\_ \_ ProviderRegistration** sert de classe parente pour les classes d’inscription de différents types de fournisseurs.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract]
class __ProviderRegistration : __SystemClass
{
  __Provider REF provider;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ ProviderRegistration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ ProviderRegistration** possède les propriétés suivantes.

<dl> <dt>

**moteur**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ fournisseur**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance du [**\_ \_ fournisseur**](--provider.md) représentant le chemin d’accès de l’objet au fournisseur.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **\_ \_ ProviderRegistration** est dérivée de [**\_ \_ SystemClass**](--systemclass.md), qui n’a pas de propriétés.

Les instances de la classe système **\_ \_ ProviderRegistration** ne sont jamais créées. Les classes que les fournisseurs utilisent pour créer des instances pour l’inscription dérivent directement ou indirectement de cette classe. Il s'agit des classes suivantes :

[**\_\_ClassProviderRegistration**](--classproviderregistration.md)

[**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)

[**\_\_EventProviderRegistration**](--eventproviderregistration.md)

[**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)

[**\_\_MethodProviderRegistration**](--methodproviderregistration.md)

[**\_\_ObjectProviderRegistration**](--objectproviderregistration.md)

[**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)

Seuls les administrateurs peuvent inscrire ou supprimer un fournisseur en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et en l’inscrivant.

## <a name="requirements"></a>Conditions requises



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
</dt> <dt>

[Inscription d’un fournisseur](registering-a-provider.md)
</dt> </dl>

 

