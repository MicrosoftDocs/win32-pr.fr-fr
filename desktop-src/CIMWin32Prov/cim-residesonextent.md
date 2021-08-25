---
description: La \_ classe CIM ResidesOnExtent représente une association entre un système de fichiers et l’extension de stockage où elle se trouve. En règle générale, un système de fichiers réside sur un disque logique.
ms.assetid: 911a81e9-3032-41ff-a337-044c06d02307
ms.tgt_platform: multiple
title: Classe CIM_ResidesOnExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResidesOnExtent
- CIM_ResidesOnExtent.Dependent
- CIM_ResidesOnExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7149de4ab84b13ef4e0f6b2c3aed908f8ef933ad09541c885f53edd3caec9d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920349"
---
# <a name="cim_residesonextent-class"></a>\_Classe CIM ResidesOnExtent

La classe **CIM \_ ResidesOnExtent** représente une association entre un système de fichiers et l’extension de stockage où elle se trouve. En règle générale, un système de fichiers réside sur un disque logique.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{10458E26-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ResidesOnExtent : CIM_Dependency
{
  CIM_FileSystem    REF Dependent;
  CIM_StorageExtent REF Antecedent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ResidesOnExtent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ResidesOnExtent** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ StorageExtent**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ StorageExtent CIM**](cim-storageextent.md) qui décrit l’extension de stockage.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ système de fichiers CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Un système de fichiers [**CIM \_**](cim-filesystem.md) qui décrit le système de fichiers qui se trouve sur l’extension de stockage.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **CIM \_ ResidesOnExtent** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).

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

 

