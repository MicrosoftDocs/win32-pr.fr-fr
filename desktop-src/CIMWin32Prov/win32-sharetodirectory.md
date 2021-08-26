---
description: La \_ classe WMI de l’Association ShareToDirectory Win32 associe une ressource partagée sur le système de l’ordinateur et le répertoire auquel elle est mappée.
ms.assetid: f8562539-2cb4-4661-8ef9-8b665e76a292
ms.tgt_platform: multiple
title: Classe Win32_ShareToDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShareToDirectory
- Win32_ShareToDirectory.Share
- Win32_ShareToDirectory.SharedElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d041209dcdbd1d9a39d08acb75180ec9cf292f01934c21762418571d44a32460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917539"
---
# <a name="win32_sharetodirectory-class"></a>\_Classe ShareToDirectory Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ ShareToDirectory Win32** associe une ressource partagée sur le système de l’ordinateur et le répertoire auquel elle est mappée.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{8502C511-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ShareToDirectory
{
  Win32_Share   REF Share;
  CIM_Directory REF SharedElement;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ ShareToDirectory** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ ShareToDirectory** a ces propriétés.

<dl> <dt>

**Partager**
</dt> <dd> <dl> <dt>

Type de données **: \_ partage Win32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| partage WMI Win32 \_ »)
</dt> </dl>

Référence à l’instance de qui représente les propriétés d’une ressource partagée disponible par le biais du répertoire.

</dd> <dt>

**SharedElement**
</dt> <dd> <dl> <dt>

Type de données **: \_ répertoire CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« répertoire CIM CIM \| \_ »)
</dt> </dl>

Référence à l’instance représentant les propriétés du répertoire qui a été mappé à une ressource partagée.

</dd> </dl>

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

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
