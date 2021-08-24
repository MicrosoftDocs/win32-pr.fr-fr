---
description: La \_ classe Mount CIM représente une association entre un système de fichiers et un répertoire auquel elle est attachée.
ms.assetid: abf1833b-9b39-45c0-8400-2be2bf3a1c3c
ms.tgt_platform: multiple
title: Classe CIM_Mount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Mount
- CIM_Mount.Dependent
- CIM_Mount.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1298c695237ac40097b0c081d313769ee4e4e1190571b1bdd58137e25d53c10a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821019"
---
# <a name="cim_mount-class"></a>\_Classe Mount CIM

La **classe \_ Mount CIM** représente une association entre un système de fichiers et un répertoire auquel elle est attachée.

La sémantique de cette relation exige que le répertoire monté soit contenu dans un système de fichiers (via l’Association de stockage file) qui est différent du système de fichiers référencé comme dépendant. Le système de fichiers contenant le répertoire peut être local ou distant. Par exemple, un système de fichiers local sur un système d’ordinateur Solaris peut monter un répertoire à partir du système de fichiers accessible via le lecteur de CD-ROM de l’ordinateur (autrement dit, un autre système de fichiers local). En revanche, dans un cas « distant », le répertoire est d’abord exporté par son système de fichiers, qui est hébergé sur un autre système informatique, par exemple, en tant que serveur de fichiers. Pour distinguer les deux montages, une association d' [**\_ exportation CIM**](cim-export.md) doit toujours être définie pour les répertoires accessibles/montés à distance.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{75BCF4F6-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Mount : CIM_Dependency
{
  CIM_NFS       REF Dependent;
  CIM_Directory REF Antecedent;
};
```

## <a name="members"></a>Membres

La **classe \_ Mount CIM** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ Mount CIM** possède ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ répertoire CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Antecedent »)
</dt> </dl>

[**\_ Répertoire CIM**](cim-directory.md) décrivant le répertoire monté.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Un [**\_ NFS CIM**](cim-nfs.md) décrivant le système de fichiers sur lequel le répertoire est monté.

</dd> </dl>

## <a name="remarks"></a>Remarques

**CIM \_ Le montage** est dérivé de la [**\_ dépendance CIM**](cim-dependency.md).

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

 

