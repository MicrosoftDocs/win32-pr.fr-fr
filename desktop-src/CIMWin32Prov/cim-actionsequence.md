---
description: L' \_ Association CIM ActionSequence définit une série d’opérations qui font passer l’élément logiciel (référencé par l' \_ Association CIM SoftwareElementActions) à son état suivant, ou supprime l’élément logiciel de son état actuel.
ms.assetid: b539c424-bc2a-414b-b56c-72550004720f
ms.tgt_platform: multiple
title: Classe CIM_ActionSequence
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActionSequence
- CIM_ActionSequence.Next
- CIM_ActionSequence.Prior
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71150d1ad9785d81579d8f305fe46bc6b7e57d00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512894"
---
# <a name="cim_actionsequence-class"></a>\_Classe CIM ActionSequence

L’Association **CIM \_ ActionSequence** définit une série d’opérations qui font passer l’élément logiciel (référencé par l’Association [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md) ) à son état suivant, ou supprime l’élément logiciel de son état actuel.

Les actions d’état suivant et les actions de désinstallation associées à un élément logiciel particulier doivent être une séquence continue. Étant donné que **CIM \_ ActionSequence** est une association, les boucles sur la classe d' [**\_ action CIM**](cim-action.md) , avec les rôles pour l’action « précédente » et l’action « suivante », forment une séquence.

La nécessité d’une séquence continue implique les étapes suivantes :

-   Dans l’ensemble des actions d’état suivant ou de désinstallation, il n’y a qu’une seule action qui n’a pas d’instance de l’Association **CIM \_ ActionSequence** qui la référence dans le rôle « suivant ». Il s’agit de la première action de la séquence.
-   Dans l’ensemble des actions d’état suivant ou de désinstallation, il n’y a qu’une seule action qui n’a pas d’instance de l’Association **CIM \_ ActionSequence** qui la référence dans le rôle « antérieur ». Il s’agit de la dernière action de la séquence.
-   Toutes les autres actions au sein de l’ensemble des actions d’état suivant et de désinstallation doivent participer à deux instances de l’Association **CIM \_ ActionSequence** , une dans un rôle « antérieur » et une dans le rôle « suivant ».

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Association, UUID("{F127E50E-E3E0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ActionSequence
{
  CIM_Action REF Next;
  CIM_Action REF Prior;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ActionSequence** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ActionSequence** possède les propriétés suivantes.

<dl> <dt>

**Next**
</dt> <dd> <dl> <dt>

Type de données **: \_ action CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Référence à l’action suivante.

</dd> <dt>

**Antérieure**
</dt> <dd> <dl> <dt>

Type de données **: \_ action CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Référence à l’action précédente.

</dd> </dl>

## <a name="remarks"></a>Notes

Les classes d' [**\_ action CIM**](cim-action.md) qui participent à cette association doivent avoir la même valeur pour la propriété **direction** .

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

[Classes CIM](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

