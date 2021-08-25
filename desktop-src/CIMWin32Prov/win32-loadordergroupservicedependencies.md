---
description: La \_ classe WMI de l’Association LoadOrderGroupServiceDependencies Win32 associe un service de base et un groupe d’ordre de chargement dont dépend le service pour démarrer l’exécution.
ms.assetid: 56739b80-9028-4a2e-85ed-973a078860c1
ms.tgt_platform: multiple
title: Classe Win32_LoadOrderGroupServiceDependencies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceDependencies
- Win32_LoadOrderGroupServiceDependencies.Antecedent
- Win32_LoadOrderGroupServiceDependencies.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55684bb5382c5e253c8f72b929674b9730ba7cab51a6c0cae9c27946fad5ff8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085789"
---
# <a name="win32_loadordergroupservicedependencies-class"></a>\_Classe LoadOrderGroupServiceDependencies Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ LoadOrderGroupServiceDependencies Win32** associe un service de base et un groupe d’ordre de chargement dont dépend le service pour démarrer l’exécution.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceDependencies : CIM_Dependency
{
  Win32_LoadOrderGroup REF Antecedent;
  Win32_BaseService    REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ LoadOrderGroupServiceDependencies** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ LoadOrderGroupServiceDependencies** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ LoadOrderGroup**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LoadOrderGroup")
</dt> </dl>

Référence à l’instance de qui représente les propriétés du groupe d’ordre de chargement qui doit démarrer avant que le service de base dépendant de cette classe puisse démarrer.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ BaseService**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI \| Win32 \_ BaseService »)
</dt> </dl>

Référence à l’instance de qui représente les propriétés du service de base qui dépend du groupe d’ordre de chargement pour démarrer l’exécution.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ LoadOrderGroupServiceDependencies** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).

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
</dt> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

