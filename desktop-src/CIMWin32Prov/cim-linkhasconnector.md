---
description: La \_ classe CIM LinkHasConnector associe les câbles et les liens utilisés comme connecteurs physiques, qui connectent les éléments physiques. Cette association définit explicitement la relation des connecteurs pour les \_ PHYSICALLINK CIM.
ms.assetid: c8244b93-749a-424a-ab40-ce5ce79c8b02
ms.tgt_platform: multiple
title: Classe CIM_LinkHasConnector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LinkHasConnector
- CIM_LinkHasConnector.PartComponent
- CIM_LinkHasConnector.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: daeb9d07fefc4c52c7b630dcc69099c1cae429a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861238"
---
# <a name="cim_linkhasconnector-class"></a>\_Classe CIM LinkHasConnector

La classe **CIM \_ LinkHasConnector** associe les câbles et les liens utilisés comme connecteurs physiques, qui connectent les éléments physiques. Cette association définit explicitement la relation des connecteurs pour [**les \_ PhysicalLink CIM**](cim-physicallink.md).

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{FAF76B8B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_LinkHasConnector : CIM_Component
{
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalLink      REF GroupComponent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ LinkHasConnector** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ LinkHasConnector** possède les propriétés suivantes.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ PhysicalLink**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**\_ PhysicalLink CIM**](cim-physicallink.md) qui décrit le lien physique qui possède un connecteur.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ PhysicalConnector**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

[**\_ PhysicalConnector CIM**](cim-physicalconnector.md) qui décrit le connecteur physique.

</dd> </dl>

## <a name="remarks"></a>Notes

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

[**\_Composant CIM**](cim-component.md)
</dt> </dl>

 

