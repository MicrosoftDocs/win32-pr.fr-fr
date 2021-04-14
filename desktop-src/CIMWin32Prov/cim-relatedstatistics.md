---
description: L' \_ Association CIM RelatedStatistics représente les hiérarchies et les dépendances des \_ classes StatisticalInformation CIM associées.
ms.assetid: f5cea01d-7854-4ad4-a89e-db0ce9f4a83f
ms.tgt_platform: multiple
title: Classe CIM_RelatedStatistics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RelatedStatistics
- CIM_RelatedStatistics.RelatedStats
- CIM_RelatedStatistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01fb70535a4ae8f84d637cf92a06eee4fe318a49
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523116"
---
# <a name="cim_relatedstatistics-class"></a>\_Classe CIM RelatedStatistics

L’Association **CIM \_ RelatedStatistics** représente les hiérarchies et les dépendances des classes [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md) associées.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Association, UUID("{956597A4-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_RelatedStatistics
{
  CIM_StatisticalInformation REF RelatedStats;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ RelatedStatistics** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ RelatedStatistics** possède les propriétés suivantes.

<dl> <dt>

**RelatedStats**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ StatisticalInformation**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence aux statistiques ou mesures associées.

</dd> <dt>

**Stats**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ StatisticalInformation**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence aux informations statistiques ou à l’objet.

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



 

 




