---
description: La méthode DeleteAll de l’objet SWbemPrivilegeSet supprime tous les privilèges de la collection, ce qui la vide.
ms.assetid: 368caa14-1c53-4090-8569-97ea743905de
ms.tgt_platform: multiple
title: SWbemPrivilegeSet. DeleteAll, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 382382b0c22c029f41c9ab33fb959287e5222d59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010435"
---
# <a name="swbemprivilegesetdeleteall-method"></a>SWbemPrivilegeSet. DeleteAll, méthode

La méthode **DeleteAll** de l’objet [**SWbemPrivilegeSet**](swbemprivilegeset.md) supprime tous les privilèges de la collection, ce qui la vide.

## <a name="syntax"></a>Syntaxe


```VB
SWbemPrivilegeSet.DeleteAll()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **DeleteAll** , l’objet **Err** peut contenir le code d’erreur ci-dessous.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilegeSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemPrivilegeSet<br/>                                                      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> <dt>

[Exécution des opérations privilégiées](executing-privileged-operations.md)
</dt> <dt>

[**SWbemPrivilegeSet. Remove**](swbemprivilegeset-remove.md)
</dt> </dl>

 

 




