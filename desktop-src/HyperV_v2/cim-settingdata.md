---
description: Représente les paramètres de configuration et opérationnels pour les \_ instances CIM propriété ManagedElement.
ms.assetid: a9ee0eb6-dc48-43f2-bdb5-f84fe7bbc1f2
title: Classe CIM_SettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingData
- CIM_SettingData.InstanceID
- CIM_SettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 19c62496b7980c265ff20ae0b1cdb050e311e4c5e09fd981b49b562eed14596b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647318"
---
# <a name="cim_settingdata-class"></a>\_Classe SETTINGDATA CIM

Représente les paramètres de configuration et opérationnels pour les instances [**CIM \_ propriété ManagedElement**](cim-managedelement.md) .

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingData : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ SettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ SettingData** possède ces propriétés.

<dl> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**obligatoire**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Nom convivial d’une instance de cette classe. En outre, le nom convivial peut être utilisé comme index pour une recherche ou une requête. Le nom ne doit pas nécessairement être unique au sein d’un espace de noms.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")
</dt> </dl>

Identifie de façon unique une instance de cette classe dans la portée de l’espace de noms conteneur.

> [!IMPORTANT]
>
> Pour garantir l’unicité au sein de l’espace de noms, la valeur de la propriété **InstanceID** doit être construite au format suivant : *identifiant OrgID*:*LocalID*
>
> -   *Identifiant OrgID* doit inclure un nom de droits d’auteur, de marque déposée ou un nom unique qui est détenu par l’entité métier qui définit la propriété **InstanceID** , ou être un ID inscrit qui est attribué par une autorité globale reconnue.
> -   *Identifiant OrgID* ne doit pas contenir de signe deux-points. Le premier signe deux-points dans **InstanceID** doit être compris entre *identifiant OrgID* et *LocalID*.
> -   *LocalID* est choisi par l’entité métier et ne doit pas être réutilisé pour identifier des éléments réels sous-jacents différents.
> -   Si le modèle ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que la valeur **InstanceID** obtenue n’est pas réutilisée dans les propriétés **InstanceID** produites par ce fournisseur ou d’autres fournisseurs pour cet espace de noms.
> -   Pour les instances DMTF définies, le modèle doit être utilisé avec le *identifiant OrgID* défini sur « CIM ».

 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Propriété MANAGEDELEMENT CIM**](cim-managedelement.md)
</dt> </dl>

 

