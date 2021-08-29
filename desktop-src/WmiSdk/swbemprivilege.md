---
description: L’objet SWbemPrivilege représente un privilège unique. Cet objet ne peut pas être créé par l’appel VBScript CreateObject.
ms.assetid: 18ee4587-6347-4075-b5e9-c5fb02f3cbf7
ms.tgt_platform: multiple
title: Objet SWbemPrivilege (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege
- ISWbemPrivilege
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: eeb9726f3aaf696d4e889ea32e39c85306271b7690f02b05d93fff80715f497b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097149"
---
# <a name="swbemprivilege-object"></a>Objet SWbemPrivilege

L’objet **SWbemPrivilege** représente un privilège unique. Cet objet ne peut pas être créé par l’appel VBScript **CreateObject** .

## <a name="members"></a>Membres

L’objet **SWbemPrivilege** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **SWbemPrivilege** a ces propriétés.



| Propriété                                                     | Type d’accès           | Description                                                                      |
|:-------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------|
| [**NomComplet**](swbemprivilege-displayname.md)<br/> | Lecture seule<br/>  | Nom complet de ce privilège.<br/>                                       |
| [**Identificateur**](swbemprivilege-identifier.md)<br/>   | Lecture/écriture<br/> | Entier qui représente le privilège qui est défini ou récupéré.<br/> |
| [**IsEnabled**](swbemprivilege-isenabled.md)<br/>     | Lecture/écriture<br/> | Valeur booléenne qui indique si ce privilège est activé.<br/>            |
| [**Nom**](swbemprivilege-name.md)<br/>               | Lecture seule<br/>  | Nom de ce privilège.<br/>                                               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilege<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemPrivilege<br/>                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Exécution des opérations privilégiées](executing-privileged-operations.md)
</dt> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

 




