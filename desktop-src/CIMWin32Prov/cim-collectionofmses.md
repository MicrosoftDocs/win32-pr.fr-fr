---
description: L' \_ objet CIM CollectionOfMSEs autorise le regroupement d' \_ objets ManagedSystemElement CIM afin d’associer les paramètres et les configurations. Il est abstrait d’exiger une définition et un affinage sémantique supplémentaires dans les sous-classes.
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: CIM_CollectionOfMSEs, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.Caption
- CIM_CollectionOfMSEs.CollectionID
- CIM_CollectionOfMSEs.Description
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57942dd6e00d819e4375ddd316e5e15126621b97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110994"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a>CIM_CollectionOfMSEs, classe (fournisseurs WMI CIMWin32)

L’objet **CIM \_ CollectionOfMSEs** autorise le regroupement d’objets [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) afin d’associer les paramètres et les configurations. Il est abstrait d’exiger une définition et un affinage sémantique supplémentaires dans les sous-classes.

L' **objet \_ CIMOM CIM** ne contient pas d’informations d’État ou d’État, mais il représente uniquement un regroupement d’éléments. Pour cette raison, il est incorrect pour les groupes de sous-classes dont l’État/l’État est **CIM \_ CollectionOfMSEs**. un exemple est [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) (qui est correctement sous-classé à partir de [**CIM \_ LogicalElement**](cim-logicalelement.md)). En général, les collections agrègent des objets « like » et représentent une optimisation. Sans les collections, l’une est forcée de définir des associations [**CIM \_ ElementSetting**](cim-elementsetting.md) et [**CIM \_ ElementConfiguration**](cim-elementconfiguration.md) , pour lier des paramètres et des objets de configuration à des [**\_ ManagedSystemElements CIM**](cim-managedsystemelement.md)individuels. Il peut y avoir de nombreuses doublons pour attribuer le même paramètre à plusieurs objets. En outre, l’utilisation de l’objet de collection permet de déterminer que les associations de paramètres et de configuration sont identiques pour les membres de la collection. Dans le cas contraire, ces informations seraient obtenues en définissant la collection de manière propriétaire, puis en interrogeant les associations **CIM \_ ElementSetting** et **CIM \_ ElementConfiguration** pour déterminer si le jeu d’collections est entièrement couvert.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class CIM_CollectionOfMSEs
{
  string Caption;
  string CollectionID;
  string Description;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ CollectionOfMSEs** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ CollectionOfMSEs** possède les propriétés suivantes.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Courte description textuelle de l’objet CollectionOfMSEs.

</dd> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identification de l’objet de collection. Lorsqu’elle est sous-classée, la propriété de l’un peut être substituée pour être une propriété de clé.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de l’objet CollectionOfMSEs.

</dd> </dl>

## <a name="remarks"></a>Notes

WMI n’implémente pas cette classe. Consultez [classes Win32](win32-provider.md) pour les classes WMI dérivées de **CIM \_ CollectionOfMSEs**.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




