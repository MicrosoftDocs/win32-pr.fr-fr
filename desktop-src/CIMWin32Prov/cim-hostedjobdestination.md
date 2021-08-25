---
description: La \_ classe CIM HostedJobDestination représente une association entre une destination de travail et le système sur lequel elle réside. Un système peut héberger de nombreuses files d’attente de travaux. Les destinations du travail diffèrent au système d’hébergement.
ms.assetid: 5d853826-1f27-417b-a053-5e0ee9816376
ms.tgt_platform: multiple
title: Classe CIM_HostedJobDestination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedJobDestination
- CIM_HostedJobDestination.Dependent
- CIM_HostedJobDestination.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 072e911471fe6220a7135f45787f5ea8bf9c79279212ed6215a971ff8c1d95cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923529"
---
# <a name="cim_hostedjobdestination-class"></a>\_Classe CIM HostedJobDestination

La classe **CIM \_ HostedJobDestination** représente une association entre une destination de travail et le système sur lequel elle réside. Un système peut héberger de nombreuses files d’attente de travaux. Les destinations du travail diffèrent au système d’hébergement.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{7880DD16-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedJobDestination : CIM_Dependency
{
  CIM_JobDestination REF Dependent;
  CIM_System         REF Antecedent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ HostedJobDestination** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ HostedJobDestination** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ système CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Antecedent »)
</dt> </dl>

[**\_ Système CIM**](cim-system.md) qui décrit le système d’hébergement.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ JobDestination**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

[**\_ JobDestination CIM**](cim-jobdestination.md) décrivant la destination du travail hébergée sur le système.

</dd> </dl>

## <a name="remarks"></a>Remarques

**CIM \_ HostedJobDestination** est dérivé de [**la \_ dépendance CIM**](cim-dependency.md).

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

 

