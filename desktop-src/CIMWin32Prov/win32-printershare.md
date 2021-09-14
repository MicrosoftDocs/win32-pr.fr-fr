---
description: La \_ classe WMI de l’Association PrinterShare Win32 lie une imprimante locale et le partage qui la représente lorsqu’elle est affichée sur un réseau.
ms.assetid: 9ac99e52-5e8f-4329-960f-7bd1fd229e37
ms.tgt_platform: multiple
title: Classe Win32_PrinterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterShare
- Win32_PrinterShare.Antecedent
- Win32_PrinterShare.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57bc15fc5d3db78179335b039851d7d3b7cbf8a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126924176"
---
# <a name="win32_printershare-class"></a>\_Classe PrinterShare Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ PrinterShare Win32** lie une imprimante locale et le partage qui la représente lorsqu’elle est affichée sur un réseau.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class Win32_PrinterShare : CIM_Dependency
{
  Win32_Printer REF Antecedent;
  Win32_Share   REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ PrinterShare** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ PrinterShare** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ imprimante Win32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Référence à l’instance de qui représente l’imprimante locale partagée dans cette association.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ partage Win32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Référence à l’instance représentant le partage de l’imprimante dans cette association.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ PrinterShare** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
