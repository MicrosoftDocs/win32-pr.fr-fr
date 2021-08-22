---
description: La \_ classe CIM ComputerSystemMappedIO représente une association entre un système informatique et les ports d’e/s mappés en mémoire disponibles.
ms.assetid: 5df9db36-67ad-4a94-a7db-150b58977af1
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemMappedIO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemMappedIO
- CIM_ComputerSystemMappedIO.GroupComponent
- CIM_ComputerSystemMappedIO.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bf81632bd380756e49cde1804f7e35d3115b8575460ce04772e8d153255d6777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322039"
---
# <a name="cim_computersystemmappedio-class"></a>\_Classe CIM ComputerSystemMappedIO

La classe **CIM \_ ComputerSystemMappedIO** représente une association entre un système informatique et les ports d’e/s mappés en mémoire disponibles.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{A2EFC897-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemMappedIO : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_MemoryMappedIO REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ComputerSystemMappedIO** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ComputerSystemMappedIO** possède les propriétés suivantes.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)
</dt> </dl>

Un [**\_ ComputerSystem CIM**](cim-computersystem.md) qui décrit le système informatique mappé au port d’e/s.

Cette propriété est héritée de [ **CIM \_ ComputerSystemResource**](cim-computersystemresource.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ MemoryMappedIO**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

[**\_ MemoryMappedIO CIM**](cim-memorymappedio.md) qui décrit un port d’e/s mappé à la mémoire du système informatique.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **CIM \_ ComputerSystemMappedIO** est dérivée de [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md).

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

[**\_COMPUTERSYSTEMRESOURCE CIM**](cim-computersystemresource.md)
</dt> </dl>

 

