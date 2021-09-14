---
description: La propriété Name d’un objet SWbemPrivilege est une chaîne qui décrit de façon unique un privilège.
ms.assetid: cc1cdde7-20ad-4ff7-ad49-43eb46c15df9
ms.tgt_platform: multiple
title: Propriété SWbemPrivilege.Name (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.Name
- ISWbemPrivilege.Name
- ISWbemPrivilege.get_Name
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b83ccc7c2757c5d5a0746efd4434db3d108b6992
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923344"
---
# <a name="swbemprivilegename-property"></a>Propriété SWbemPrivilege.Name

La propriété **Name** d’un objet [**SWbemPrivilege**](swbemprivilege.md) est une chaîne qui décrit de façon unique un privilège. Par exemple, le privilège qui contrôle si un utilisateur peut exécuter la méthode Shutdown d’un objet possède la chaîne « SeShutdownPrivilege » dans la propriété **SWbemPrivilege.Name** . Cette propriété est en lecture seule.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemPrivilege.Name As 
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilege<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemPrivilege<br/>                                                         |



 

 




