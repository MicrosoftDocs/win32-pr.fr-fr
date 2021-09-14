---
description: L' \_ agrégation CIM StorageDefect collecte les erreurs de stockage pour une étendue de stockage.
ms.assetid: 7acd3d25-4691-43cb-badc-662684989345
ms.tgt_platform: multiple
title: Classe CIM_StorageDefect
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageDefect
- CIM_StorageDefect.Error
- CIM_StorageDefect.Extent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e6c2be45fe2f44afa407dc72e3ae90c486593ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225385"
---
# <a name="cim_storagedefect-class"></a>\_Classe CIM StorageDefect

L’agrégation **CIM \_ StorageDefect** collecte les erreurs de stockage pour une étendue de stockage.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{5CC70817-DB31-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_StorageDefect
{
  CIM_StorageError  REF Error;
  CIM_StorageExtent REF Extent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ StorageDefect** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ StorageDefect** possède les propriétés suivantes.

<dl> <dt>

**Error**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ StorageError**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **faible**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Référence à l’objet d’erreur, qui définit les adresses de début et de fin qui sont mappées en dehors de l’étendue de stockage.

</dd> <dt>

**Extension**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ StorageExtent**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Référence à l’extension de stockage sur laquelle les erreurs se sont produites.

</dd> </dl>

## <a name="remarks"></a>Notes

WMI n’implémente pas cette classe.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

