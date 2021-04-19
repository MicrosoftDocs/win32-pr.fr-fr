---
description: Représente une association dans laquelle un élément managé est conforme à la norme d’un profil inscrit.
ms.assetid: 9d5704b6-c764-4f68-bce3-384d5a244e28
title: Classe CIM_ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConformsToProfile
- CIM_ElementConformsToProfile.ConformantStandard
- CIM_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7034001641029099d1b52090b3cc518b6589dc50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517554"
---
# <a name="cim_elementconformstoprofile-class"></a>\_Classe CIM ElementConformsToProfile

Représente une association dans laquelle un élément managé est conforme à la norme d’un profil inscrit. Cette association s’applique généralement à une instance de niveau supérieur, telle qu’un système, un espace de noms ou un service. En cas d’application à une instance de niveau supérieur, tous les éléments constitutifs doivent se comporter de manière appropriée pour la prise en charge de la conformité du propriété ManagedElement au RegisteredProfile nommé.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Interop")]
class CIM_ElementConformsToProfile
{
  CIM_RegisteredProfile REF ConformantStandard;
  CIM_ManagedElement    REF ManagedElement;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ElementConformsToProfile** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ElementConformsToProfile** possède les propriétés suivantes.

<dl> <dt>

**ConformantStandard**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ RegisteredProfile**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Profil inscrit auquel l’élément managé est conforme.

</dd> <dt>

**Propriété ManagedElement**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ propriété ManagedElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Élément managé qui est conforme au profil inscrit.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

