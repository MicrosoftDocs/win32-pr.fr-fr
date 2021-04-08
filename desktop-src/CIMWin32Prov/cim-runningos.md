---
description: La \_ classe CIM executos représente le système d’exploitation en cours d’exécution. Au maximum, un système d’exploitation peut s’exécuter à tout moment sur un système informatique. le système informatique n’est peut-être pas en cours de démarrage ou son système d’exploitation est peut-être inconnu.
ms.assetid: 93e3d425-d751-4252-aa81-7d6774c8f8c5
ms.tgt_platform: multiple
title: Classe CIM_RunningOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RunningOS
- CIM_RunningOS.Dependent
- CIM_RunningOS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ff86af88342a1b8f0147ecd9721765794faf39e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748949"
---
# <a name="cim_runningos-class"></a>\_Classe en cours d’exécution CIM

La classe CIM executos représente le système d’exploitation **\_ en** cours d’exécution. Au maximum, un système d’exploitation peut s’exécuter à tout moment sur un système informatique. le système informatique n’est peut-être pas en cours de démarrage ou son système d’exploitation est peut-être inconnu.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{1F2EA300-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RunningOS : CIM_Dependency
{
  CIM_ComputerSystem  REF Dependent;
  CIM_OperatingSystem REF Antecedent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ Running** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM- \_ Running** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ OperatingSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Antecedent »)
</dt> </dl>

Un système d’exploitation [**CIM \_**](cim-operatingsystem.md) qui décrit le système d’exploitation en cours d’exécution sur le système informatique.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Un [**\_ ComputerSystem CIM**](cim-computersystem.md) qui décrit le système informatique.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **CIM \_ en cours d’exécution** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).

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

 

