---
description: Vous pouvez utiliser les propriétés de l’objet SWbemQualifier pour représenter un qualificateur unique d’une classe, d’une instance, d’une propriété ou d’un paramètre de méthode WMI. Cet objet ne peut pas être créé par l’appel VBScript CreateObject.
ms.assetid: b5dbe98a-e1d8-4679-a563-c88760d08b79
ms.tgt_platform: multiple
title: Objet SWbemQualifier (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifier
- ISWbemQualifier
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 25315805a4cabc901fab9b7f28cca6c023fc18389b6d94f8f459c91fd785b361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463734"
---
# <a name="swbemqualifier-object"></a>Objet SWbemQualifier

Vous pouvez utiliser les propriétés de l’objet **SWbemQualifier** pour représenter un qualificateur unique d’une classe, d’une instance, d’une propriété ou d’un paramètre de méthode WMI. Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](creating-an-object-using-vbscript.md) .

## <a name="members"></a>Membres

L’objet **SWbemQualifier** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **SWbemQualifier** a ces propriétés.



| Propriété                                                                       | Type d’accès           | Description                                                                                           |
|:-------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------|
| [**IsAmended**](swbemqualifier-isamended.md)<br/>                       | Lecture seule<br/>  | Valeur booléenne qui indique si ce qualificateur a été localisé à l’aide d’une opération de fusion.<br/> |
| [**IsLocal**](swbemqualifier-islocal.md)<br/>                           | Lecture seule<br/>  | Valeur booléenne qui indique si ce qualificateur est local.<br/>                                   |
| [**IsOverridable**](swbemqualifier-isoverridable.md)<br/>               | Lecture/écriture<br/> | Valeur booléenne qui indique si ce qualificateur peut être substitué lorsqu’il est propagé.<br/>          |
| [**Nom**](swbemqualifier-name.md)<br/>                                 | Lecture seule<br/>  | Nom de ce qualificateur.<br/>                                                                    |
| [**PropagatesToInstance**](swbemqualifier-propagatestoinstance.md)<br/> | Lecture/écriture<br/> | Valeur booléenne qui indique si ce qualificateur peut être propagé à une instance.<br/>           |
| [**PropagatesToSubClass**](swbemqualifier-propagatestosubclass.md)<br/> | Lecture seule<br/>  | Valeur booléenne qui indique si ce qualificateur peut être propagé à une sous-classe.<br/>            |
| [**Valeur**](swbemqualifier-value.md)<br/>                               | Lecture/écriture<br/> | Valeur de type variant de ce qualificateur. Il s’agit de la propriété par défaut de cet objet.<br/>              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifier<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemQualifier<br/>                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

 




