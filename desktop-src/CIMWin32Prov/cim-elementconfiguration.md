---
description: L' \_ Association CIM ElementConfiguration associe un \_ objet de configuration CIM à un ou plusieurs éléments système gérés. L' \_ objet de configuration CIM représente un comportement spécifique ou un état fonctionnel souhaité pour le MANAGEDSYSTEMELEMENT CIM associé \_ .
ms.assetid: 4d2af009-7466-4394-af42-72c8d96e0786
ms.tgt_platform: multiple
title: Classe CIM_ElementConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConfiguration
- CIM_ElementConfiguration.Configuration
- CIM_ElementConfiguration.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7707338a3c2268cba51146aa8462b3b244b149ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033704"
---
# <a name="cim_elementconfiguration-class"></a>\_Classe CIM ElementConfiguration

L’Association **CIM \_ ElementConfiguration** associe un objet de [**\_ configuration CIM**](cim-configuration.md) à un ou plusieurs éléments système gérés. L’objet de **\_ configuration CIM** représente un comportement spécifique ou un état fonctionnel souhaité pour le [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md)associé.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{FC049DCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ElementConfiguration
{
  CIM_Configuration        REF Configuration;
  CIM_ManagedSystemElement REF Element;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ElementConfiguration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ElementConfiguration** possède les propriétés suivantes.

<dl> <dt>

**Configuration**
</dt> <dd> <dl> <dt>

Type de données **: \_ configuration CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à l’objet de [**\_ configuration CIM**](cim-configuration.md) qui regroupe les paramètres et les dépendances associés à l’élément système géré.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à l’élément système managé.

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



 

 




