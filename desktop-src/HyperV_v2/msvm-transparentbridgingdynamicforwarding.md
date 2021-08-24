---
description: Connecte un service de pontage transparent à une entrée de transfert dynamique (adresse MAC apprise).
ms.assetid: CA083F15-1E75-4EB9-BE56-95742181FDAC
title: Classe Msvm_TransparentBridgingDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingDynamicForwarding
- Msvm_TransparentBridgingDynamicForwarding.Antecedent
- Msvm_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dd768b458ffed82f82b682b6f121baf67c6a909e142a9e9efdf7f63e29573671
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811759"
---
# <a name="msvm_transparentbridgingdynamicforwarding-class"></a>MSVM \_ TransparentBridgingDynamicForwarding, classe

Connecte un service de pontage transparent à une entrée de transfert dynamique (adresse MAC apprise).

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingDynamicForwarding : CIM_TransparentBridgingDynamicForwarding
{
  Msvm_TransparentBridgingService REF Antecedent;
  Msvm_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ TransparentBridgingDynamicForwarding** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ TransparentBridgingDynamicForwarding** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) qui représente le service de pontage transparent.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) qui représente l’entrée de transfert dynamique de la base de données de transfert.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ TransparentBridgingDynamicForwarding** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_TRANSPARENTBRIDGINGDYNAMICFORWARDING CIM**](cim-transparentbridgingdynamicforwarding.md)
</dt> <dt>

[**\_TRANSPARENTBRIDGINGDYNAMICFORWARDING CIM**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingdynamicforwarding)
</dt> </dl>

 

