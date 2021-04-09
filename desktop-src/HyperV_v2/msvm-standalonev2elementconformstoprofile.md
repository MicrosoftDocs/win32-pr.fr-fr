---
description: Définit les profils enregistrés conformes au système autonome référencé.
ms.assetid: d9ede8d0-c6f3-48bd-84a9-7f2c31637819
title: Classe Msvm_StandaloneV2ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StandaloneV2ElementConformsToProfile
- Msvm_StandaloneV2ElementConformsToProfile.ConformantStandard
- Msvm_StandaloneV2ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c492ad5bdd0e50bbbe86fd220000099269501ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951524"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a>MSVM \_ StandaloneV2ElementConformsToProfile, classe

Définit les profils enregistrés conformes au système autonome référencé.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class Msvm_StandaloneV2ElementConformsToProfile : Msvm_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard = $SVP;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ StandaloneV2ElementConformsToProfile** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ StandaloneV2ElementConformsToProfile** possède les propriétés suivantes.

<dl> <dt>

**ConformantStandard**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ RegisteredProfile**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Profil inscrit auquel le système autonome est conforme.

</dd> <dt>

**Propriété ManagedElement**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ ComputerSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers), **targetNamespace, \_ targetNamespace** ("root \\ \\ Virtualization \\ \\ V2")
</dt> </dl>

Système autonome conforme au profil enregistré.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Interop racine<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ ElementConformsToProfile**](msvm-elementconformstoprofile.md)
</dt> </dl>

 

