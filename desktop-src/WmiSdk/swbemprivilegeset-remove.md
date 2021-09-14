---
description: La méthode Remove de l’objet SWbemPrivilegeSet supprime un privilège de la collection.
ms.assetid: 4c0b6d49-262c-4840-955b-35b16b68f29f
ms.tgt_platform: multiple
title: SWbemPrivilegeSet. Remove, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f277e291a4296253d7c0b1b11c694952ddc17ddf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010433"
---
# <a name="swbemprivilegesetremove-method"></a>SWbemPrivilegeSet. Remove, méthode

La méthode **Remove** de l’objet [**SWbemPrivilegeSet**](swbemprivilegeset.md) supprime un privilège de la collection.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemPrivilegeSet.Remove( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iPrivilege* 
</dt> <dd>

Obligatoire. Il s’agit de l’une des constantes WMI du groupe [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) . Ces constantes sont essentiellement des entiers qui représentent des privilèges spécifiques. par exemple, pour supprimer le privilège qui vous permet d’arrêter un système Windows, utilisez la constante **wbemPrivilegeShutdown** ou l’équivalent numérique de 0x17.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **Remove** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

Le privilège spécifié n’existe pas.

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

[**SWbemPrivilegeSet. Add**](swbemprivilegeset-add.md)
</dt> </dl>

 

 




