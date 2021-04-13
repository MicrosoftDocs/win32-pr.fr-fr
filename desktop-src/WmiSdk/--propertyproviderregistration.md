---
description: Inscrit les fournisseurs de propriétés dans WMI.
ms.assetid: 24792884-3fb9-4974-83d5-1c5fc1fa72a1
ms.tgt_platform: multiple
title: Classe __PropertyProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderRegistration
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6d618a62eab4ba799a2d0e152763fcef6567fd42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529307"
---
# <a name="__propertyproviderregistration-class"></a>\_\_PropertyProviderRegistration, classe

La classe système **\_ \_ PropertyProviderRegistration** inscrit des fournisseurs de propriétés dans WMI.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __PropertyProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
  boolean        SupportsPut = False;
  boolean        SupportsGet = False;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ PropertyProviderRegistration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ PropertyProviderRegistration** possède les propriétés suivantes.

<dl> <dt>

**moteur**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ fournisseur**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance du [**\_ \_ fournisseur**](--provider.md) qui représente le chemin d’accès de l’objet du fournisseur de propriétés. Cette propriété est héritée de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> <dt>

**SupportsGet**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le fournisseur de classes ou d’instances prend en charge la récupération de données.

<dt>

Vrai
</dt> <dd>

Le fournisseur prend en charge la récupération de données en implémentant [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>

Faux
</dt> <dd>

Le fournisseur ne prend pas en charge la récupération de données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> </dl>

</dd> <dt>

**SupportsPut**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le fournisseur de classes ou d’instances prend en charge la modification des données.

<dt>

Vrai
</dt> <dd>

Le fournisseur prend en charge la modification de classe ou d’instance en implémentant l’une des méthodes suivantes :

-   [**IWbemServices ::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (fournisseurs de classes)
-   [**IWbemServices ::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (fournisseurs de classes)

</dd> <dt>

Faux
</dt> <dd>

Le fournisseur ne prend pas en charge la modification des données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) ou [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **\_ \_ PropertyProviderRegistration** est dérivée de [**\_ \_ ProviderRegistration**](--providerregistration.md). Seuls les administrateurs peuvent inscrire un fournisseur de propriétés en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et **\_ \_ PropertyProviderRegistration**. Seuls les administrateurs peuvent supprimer un fournisseur de propriétés.

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

[Inscription d’un fournisseur de propriétés](registering-a-property-provider.md)
</dt> </dl>

 

