---
description: La méthode Clone \_ de l’objet SWbemObject retourne un nouvel objet qui est un clone de l’objet actuel.
ms.assetid: d0773c94-30b5-4217-8a9a-0bceb9e75f02
ms.tgt_platform: multiple
title: Méthode SWbemObject.Clone_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Clone_
- ISWbemObject.Clone_
- ISWbemObject.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84ca02bf749fd69db01ca7925b554c4eb0d95c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035076"
---
# <a name="swbemobjectclone_-method"></a>SWbemObject. Clone, \_ méthode

La **méthode \_ clone** de l’objet [**SWbemObject**](swbemobject.md) retourne un nouvel objet qui est un clone de l’objet actuel.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette méthode retourne un nouvel objet [**SWbemObject**](swbemobject.md) .

## <a name="error-codes"></a>Codes d’erreur

Une fois la méthode **clone \_** terminée, l’objet **Err** peut contenir l’un des codes d’erreur ci-dessous.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

**Rien** n’a été spécifié en tant que paramètre et n’est pas acceptable dans cette utilisation.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour cloner l’objet.

</dd> </dl>

## <a name="remarks"></a>Notes

Utilisez la **méthode \_ clone** pour dupliquer une définition de classe ou une instance. Cela est utile lorsque vous avez besoin de la copie d’origine de l’objet à des fins de sauvegarde lors de la modification d’une nouvelle copie. De même, utilisez cette méthode pour créer un grand nombre de nouvelles instances à partir d’une seule instance source. Par exemple, utilisez [**SWbemObject. SpawnInstance \_**](swbemobject-spawninstance-.md) pour créer une instance de démarrage unique et utilisez **SWbemObject. Clone \_** pour produire rapidement 100 copies de l’instance. Par la suite, vous pouvez modifier les objets, en attribuant à chacune d’elles des valeurs spécifiques.

Il n’est pas possible d’utiliser cette méthode pour convertir une définition de classe en instance, ni pour convertir une instance en une définition de classe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




