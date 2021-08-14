---
description: La méthode Clone \_ de l’objet SWbemLastError retourne un nouvel objet qui est un clone de l’objet SWbemLastError actuel.
ms.assetid: 577be060-309f-40a2-a4db-c0a477c21f11
ms.tgt_platform: multiple
title: Méthode SWbemLastError.Clone_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Clone_
- ISWbemLastError.Clone_
- ISWbemLastError.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 162944eeb4ee7ca0c72102b704e9f75851bbfb41885e6b79e86d1a438487473f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314665"
---
# <a name="swbemlasterrorclone_-method"></a>SWbemLastError. Clone, \_ méthode

La **méthode \_ clone** de l’objet [**SWbemLastError**](swbemlasterror.md) retourne un nouvel objet qui est un clone de l’objet **SWbemLastError** actuel.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la **méthode \_ clone** réussit, elle retourne un nouvel objet [**SWbemLastError**](swbemlasterror.md) .

## <a name="error-codes"></a>Codes d’erreur

À la fin de la **méthode \_ clone** , l’objet **Err** peut contenir l’un des codes d’erreur ci-dessous.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre spécifié n’est pas valide.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> </dl>

## <a name="remarks"></a>Remarques

Utilisez la **méthode \_ clone** pour dupliquer une définition ou une instance de classe. Cette méthode est utile lorsque vous devez sauvegarder la copie d’origine de l’objet lors de la modification d’une nouvelle copie. Utilisez également cette méthode pour créer de nombreuses nouvelles instances à partir d’une seule instance source. Par exemple, utilisez [**SWbemObject. SpawnInstance \_**](swbemobject-spawninstance-.md) pour créer une instance de démarrage unique et utilisez **SWbemLastError. \_ clone** pour produire rapidement 100 copies de l’instance. Par la suite, vous pouvez modifier les objets, en attribuant des valeurs spécifiques à chaque objet.

Il n’est pas possible d’utiliser cette méthode pour convertir une définition de classe en instance ou pour convertir une instance en une définition de classe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



 

 




