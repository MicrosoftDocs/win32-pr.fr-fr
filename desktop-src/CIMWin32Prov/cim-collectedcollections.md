---
description: La \_ classe COLLECTEDCOLLECTIONS CIM est une association d’agrégation qui représente une collection d’éléments système gérés (MSE) contenus dans une collection de MSEs.
ms.assetid: 7baaf429-1211-4545-ace2-c6312d53c0f6
ms.tgt_platform: multiple
title: Classe CIM_CollectedCollections
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedCollections
- CIM_CollectedCollections.Collection
- CIM_CollectedCollections.CollectionInCollection
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cecac67d96aba6b8ad8c5937f098eaef312af89b80c28febaa8073c5f7be26f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322289"
---
# <a name="cim_collectedcollections-class"></a>\_Classe CIM CollectedCollections

La **classe \_ CollectedCollections CIM** est une association d’agrégation qui représente une collection d’éléments système gérés (MSE) contenus dans une collection de MSEs.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class CIM_CollectedCollections
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_CollectionOfMSEs REF CollectionInCollection;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ CollectedCollections** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ CollectedCollections** possède les propriétés suivantes.

<dl> <dt>

**Collection**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ CollectionOfMSEs**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence au « niveau supérieur » ou à l’élément parent dans l’agrégation.

</dd> <dt>

**CollectionInCollection**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ CollectionOfMSEs**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à la **collection**« collectée ».

</dd> </dl>

## <a name="remarks"></a>Remarques

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



 

 




