---
description: Décrit un profil qui est référencé par un autre profil enregistré.
ms.assetid: 36FC0161-C57F-488A-9B4A-C86C6EB481D7
title: Classe Msvm_ReferencedProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencedProfile
- Msvm_ReferencedProfile.Antecedent
- Msvm_ReferencedProfile.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1dbfe81dede2e3a6eb8b902ff03fe034deda1b5ab8160e830376e3380fe811c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046399"
---
# <a name="msvm_referencedprofile-class"></a>MSVM \_ ReferencedProfile, classe

Décrit un profil qui est référencé par un autre profil enregistré.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class Msvm_ReferencedProfile : CIM_ReferencedProfile
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ReferencedProfile** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ReferencedProfile** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Profil inscrit qui est référencé par le profil **dépendant** .

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Profil inscrit qui référence d’autres profils.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\Interop racine<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

