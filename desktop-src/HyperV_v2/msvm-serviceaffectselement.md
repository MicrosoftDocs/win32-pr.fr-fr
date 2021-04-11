---
description: Associe une instance de machine virtuelle au service de gestion qui contrôle son état.
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Classe Msvm_ServiceAffectsElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceAffectsElement
- Msvm_ServiceAffectsElement.AffectedElement
- Msvm_ServiceAffectsElement.AffectingElement
- Msvm_ServiceAffectsElement.ElementEffects
- Msvm_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eadb9f33015091999776b73c83d792ccd29396b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113883"
---
# <a name="msvm_serviceaffectselement-class"></a>MSVM \_ ServiceAffectsElement, classe

Associe une instance de machine virtuelle au service de gestion qui contrôle son état.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceAffectsElement : CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[] = 5;
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ServiceAffectsElement** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ServiceAffectsElement** possède les propriétés suivantes.

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à l’ordinateur virtuel. Cette propriété est héritée de la [**\_ ServiceAffectsElement CIM**](/previous-versions//cc136907(v=vs.85)).

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Type de données : **[ **\_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence au service qui contrôle l’ordinateur virtuel. Cette propriété est héritée de la [**\_ ServiceAffectsElement CIM**](/previous-versions//cc136907(v=vs.85)).

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le type de contrôle représenté par l’Association. Cette propriété est héritée de la [**\_ ServiceAffectsElement CIM**](/previous-versions//cc136907(v=vs.85))et est toujours définie sur la valeur suivante.



| Valeur                                                                        | Signification            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>5</dt> </dl> | Gère<br/> |



 

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Détails du type d’association à la position de tableau correspondante dans le tableau de propriétés **ElementAffects** . Ces informations sont requises si **ElementAffects** a la valeur 1 (autre). Cette propriété est héritée de [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))et est toujours définie sur **null**.

</dd> </dl>

## <a name="remarks"></a>Notes

L’accès à la classe **MSVM \_ ServiceAffectsElement** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SERVICEAFFECTSELEMENT CIM**](cim-serviceaffectselement.md)
</dt> <dt>

[**\_SERVICEAFFECTSELEMENT CIM**](/previous-versions//cc136907(v=vs.85))
</dt> </dl>

 

