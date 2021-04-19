---
description: Utilisé pour associer un RegisteredProfile CIM d’instance \_ à une instance de \_ RegisteredProfile CIM d’un autre profil qui fait référence au profil dépendant en tant que profil associé.
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: Classe CIM_ReferencedProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReferencedProfile
- CIM_ReferencedProfile.Antecedent
- CIM_ReferencedProfile.Dependent
api_type:
- Schema
api_location:
- Root\interop
ms.openlocfilehash: 8fdc0d8dccd325ae7e13de971e09cce6faf93455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518843"
---
# <a name="cim_referencedprofile-class"></a>\_Classe CIM ReferencedProfile

Utilisé pour associer un [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)) d’instance à une instance **de \_ RegisteredProfile CIM** d’un autre profil qui fait référence au profil dépendant en tant que profil associé.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Version("2.8.0"), UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_ReferencedProfile : CIM_Dependency
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ReferencedProfile** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ReferencedProfile** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’instance [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)) qui est référencée par le profil **dépendant** .

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie une instance [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)) qui référence d’autres profils.

</dd> </dl>

## <a name="remarks"></a>Notes

L’utilisation des propriétés **Dependent** et **Antecedent** dans l’Association **CIM \_ ReferencedProfile** est définie de telle sorte que le profil référencé est l’antécédent et que le profil faisant l’objet d’un référencement soit le dépendant.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                      |
| Espace de noms<br/>                | \\Interop racine<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Interop. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

