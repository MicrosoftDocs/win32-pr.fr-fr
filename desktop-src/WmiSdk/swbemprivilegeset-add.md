---
description: La méthode Add de l’objet SWbemPrivilegeSet ajoute un objet SWbemPrivilege à la collection SWbemPrivilegeSet. Si un privilège portant le même nom existe déjà dans la collection, il est remplacé.
ms.assetid: 7d44193f-60e1-4e83-8640-31d8df509d98
ms.tgt_platform: multiple
title: Méthode SWbemPrivilegeSet. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 080b9d3e3ab6dbfc0ed8afc8ac0476981b7c26e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010447"
---
# <a name="swbemprivilegesetadd-method"></a>SWbemPrivilegeSet. Add, méthode

La méthode **Add** de l’objet [**SWbemPrivilegeSet**](swbemprivilegeset.md) ajoute un objet [**SWbemPrivilege**](swbemprivilege.md) à la collection **SWbemPrivilegeSet** . Si un privilège portant le même nom existe déjà dans la collection, il est remplacé.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objPrivilege = .Add( _
  ByVal iPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iPrivilege* 
</dt> <dd>

Obligatoire. L’une des constantes WMI du groupe [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) . Ces constantes sont essentiellement des entiers qui représentent des privilèges spécifiques. Par exemple, pour ajouter le privilège qui vous permet d’arrêter un système informatique, utilisez la constante **wbemPrivilegeShutdown** . Dans un script, vous devez utiliser l’équivalent numérique 23 (0x17). Pour obtenir la liste complète de ces constantes et des chaînes de privilèges associées, consultez [**constantes de privilège**](privilege-constants.md).

</dd> <dt>

*bIsEnabled* \[ facultatif\]
</dt> <dd>

Valeur booléenne qui active ou désactive ce privilège. La valeur par défaut est **true**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

En cas de réussite, la méthode retourne un objet [**SWbemPrivilege**](swbemprivilege.md) qui représente le nouveau privilège. Dans le cas contraire, un objet null est retourné.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **Add** , l’objet **Err** peut contenir le code d’erreur figurant dans la liste suivante.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> </dl>

## <a name="examples"></a>Exemples

Un exemple de code utilisant cette méthode est décrit dans la rubrique [**SWbemPrivilegeSet**](swbemprivilegeset.md) .

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

[Exécution d’opérations privilégiées à l’aide de VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md)
</dt> <dt>

[**SWbemPrivilegeSet. Remove**](swbemprivilegeset-remove.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Constantes de privilège**](privilege-constants.md)
</dt> </dl>

 

 




