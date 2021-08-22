---
description: Association générique utilisée pour établir une partie des relations entre des éléments managés.
ms.assetid: 4D237D68-0A63-4A19-B6AD-E3C781090994
title: Classe Msvm_ConcreteComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteComponent
- Msvm_ConcreteComponent.GroupComponent
- Msvm_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24b813e7b8460f3de24207ed91b2e113f0d6b9633e17263806ef8447c166bdf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531749"
---
# <a name="msvm_concretecomponent-class"></a>MSVM \_ ConcreteComponent, classe

Association générique utilisée pour établir des relations « partie de » entre des éléments managés. [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) est défini comme une sous-classe concrète de la classe de [**\_ composant CIM**](/windows/desktop/CIMWin32Prov/cim-component) abstraite, à utiliser à la place de nombreuses sous-classes spécifiques de composant qui n’ajoutent aucune sémantique (c’est-à-dire des sous-classes qui ne clarifient pas le type de composition, les cardinales de mise à jour ou l’ajout ou la suppression de qualificateurs).

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteComponent : CIM_ConcreteComponent
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ConcreteComponent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ConcreteComponent** possède les propriétés suivantes.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Élément parent dans l’Association. Cette propriété est héritée de la [**\_ ConcreteComponent CIM**](/previous-versions//cc150665(v=vs.85)).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Élément enfant dans l’Association. Cette propriété est héritée de la [**\_ ConcreteComponent CIM**](/previous-versions//cc150665(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ ConcreteComponent** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_CONCRETECOMPONENT CIM**](cim-concretecomponent.md)
</dt> <dt>

[**\_CONCRETECOMPONENT CIM**](/previous-versions//cc150665(v=vs.85))
</dt> <dt>

[Classes du système virtuel](virtual-system-classes.md)
</dt> </dl>

 

