---
description: Représente un service de commutation qui bascule les images entre les ports de commutateur.
ms.assetid: ee2d4831-df00-408c-b350-26d2d1d3e8aa
title: Classe CIM_SwitchesAmong
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchesAmong
- CIM_SwitchesAmong.Antecedent
- CIM_SwitchesAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7a12d4ffa10f8a1a921b64fab26082a9b99e00022d2ae6363a1d093a0627b044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899635"
---
# <a name="cim_switchesamong-class"></a>\_Classe CIM SwitchesAmong

Représente un service de commutation qui bascule les images entre les ports de commutateur.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchesAmong : CIM_ForwardsAmong
{
  CIM_SwitchPort    REF Antecedent;
  CIM_SwitchService REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ SwitchesAmong** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ SwitchesAmong** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ switchport**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Référence [**CIM \_ switchport**](cim-switchport.md) au port commuté.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ SwitchService**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Référence [**CIM \_ SwitchService**](cim-switchservice.md) au service de commutation.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_FORWARDSAMONG CIM**](cim-forwardsamong.md)
</dt> </dl>

 

