---
description: La \_ classe d’association CIM CollectedMSEs représente les membres de l’objet de regroupement, une classe CollectionOfMSEs.
ms.assetid: 3dca2094-57f1-447e-809c-f924f88a185a
ms.tgt_platform: multiple
title: CIM_CollectedMSEs, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 82ffbf9e3c00a9a0463e1337ee5c5ed6ab188dc5258c622cfa6b41eb717d8589
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959078"
---
# <a name="cim_collectedmses-class-cimwin32-wmi-providers"></a>CIM_CollectedMSEs, classe (fournisseurs WMI CIMWin32)

La classe d’association **CIM \_ CollectedMSEs** représente les membres de l’objet de regroupement, une classe [**CollectionOfMSEs**](cim-collectionofmses.md) .

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class CIM_CollectedMSEs
{
  CM_CollectionOfMSEs      REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ CollectedMSEs** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ CollectedMSEs** possède les propriétés suivantes.

<dl> <dt>

**Collection**
</dt> <dd> <dl> <dt>

Type de données : **cm \_ CollectionOfMSEs**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence au regroupement ou à l’objet « Bag » qui représente la collection.

</dd> <dt>

**Membre**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à un membre de la collection.

</dd> </dl>

## <a name="remarks"></a>Remarques

WMI n’implémente pas cette classe. Pour plus d’informations sur les classes WMI dérivées de **CIM \_ CollectedMSEs**, consultez [classes Win32](win32-provider.md).

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




