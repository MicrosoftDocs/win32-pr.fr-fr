---
description: L' \_ Association CIM PackageAlarm représente la relation dans laquelle un appareil d’alarme est installé dans le cadre d’un package. L’installation indique des problèmes avec l’environnement du package&\# 8212 ; son état de sécurité ou son intégrité globale.
ms.assetid: 4911502a-de9c-46b4-91f6-a042c69fd052
ms.tgt_platform: multiple
title: Classe CIM_PackageAlarm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageAlarm
- CIM_PackageAlarm.Dependent
- CIM_PackageAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c8fde43197bd71712986c52e6badcb4e13c13c39be81ad806a74fb3da7e8337a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820729"
---
# <a name="cim_packagealarm-class"></a>\_Classe CIM PackageAlarm

L’Association [**CIM \_ PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) représente la relation dans laquelle un appareil d’alarme est installé dans le cadre d’un package. L’installation indique des problèmes liés à l’état de sécurité de l’environnement du package ou à son état d’intégrité global.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Aggregation, UUID("{FAF76B90-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageAlarm : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_AlarmDevice     REF Antecedent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ PackageAlarm** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ PackageAlarm** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ AlarmDevice**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ AlarmDevice CIM**](cim-alarmdevice.md) qui décrit l’appareil d’alarme pour le package.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ PhysicalPackage**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

[**\_ PhysicalPackage CIM**](cim-physicalpackage.md) décrivant le package physique dont l’intégrité, la sécurité, l’environnement, etc. sont alarmements.

</dd> </dl>

## <a name="remarks"></a>Remarques

**CIM \_ PackageAlarm** est dérivé de [**la \_ dépendance CIM**](cim-dependency.md).

WMI n’implémente pas cette classe.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Dépendance CIM**](cim-dependency.md)
</dt> </dl>

 

