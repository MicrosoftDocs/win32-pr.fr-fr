---
description: Classe abstraite pour les sous-classes qui décrit les capacités d’un élément géré associé et le potentiel des capacités.
ms.assetid: f0ffddf5-99d4-49be-ac0a-c2cfd4a92d96
title: Classe CIM_Capabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Capabilities
- CIM_Capabilities.InstanceID
- CIM_Capabilities.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7fc640950b7e943f0e549f41ec216b2832ec9de3b91938ef1aadea1893ac2faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561909"
---
# <a name="cim_capabilities-class"></a>\_Classe des fonctionnalités CIM

Classe abstraite pour les sous-classes qui décrit les capacités d’un élément géré associé et le potentiel des capacités.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_Capabilities : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a>Membres

La classe des **\_ fonctionnalités CIM** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe des **\_ fonctionnalités CIM** possède ces propriétés.

<dl> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**obligatoire**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Nom convivial de cette instance de classe. En outre, le nom convivial de l’utilisateur peut être utilisé comme propriété d’index pour une requête. Cette valeur ne doit pas nécessairement être unique dans son espace de noms.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")
</dt> </dl>

Identifie de façon unique et opaque une instance de cette classe dans la portée de l’espace de noms conteneur.

> [!IMPORTANT]
>
> Pour garantir l’unicité au sein de l’espace de noms, la valeur de la propriété **InstanceID** doit être construite au format suivant : *identifiant OrgID*:*LocalID*
>
> *Identifiant OrgID* doit inclure un nom de droits d’auteur, de marque déposée ou d’autre nom unique qui est détenu par l’entité métier qui définit l' **InstanceID**, ou être un ID inscrit qui est affecté par une autorité globale reconnue. Ce modèle est similaire à la structure des noms de classes de schéma. En outre, pour garantir l’unicité, les premiers deux-points dans **InstanceID** doivent être compris entre *identifiant OrgID* et *LocalID*. Par conséquent, le *identifiant OrgID* ne doit pas contenir de signe deux-points («  : »).
>
> *LocalID* est choisi par l’entité métier et ne doit pas être réutilisé pour identifier des éléments réels sous-jacents différents.
>
> Si le modèle ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que la valeur **InstanceID** obtenue n’est pas réutilisée dans les propriétés **InstanceID** produites par ce fournisseur ou d’autres fournisseurs pour cet espace de noms.
>
> Pour les instances définies pour Distributed Management Task Force (DMTF), le modèle doit être utilisé avec le *identifiant OrgID* défini sur CIM.

 

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

 

