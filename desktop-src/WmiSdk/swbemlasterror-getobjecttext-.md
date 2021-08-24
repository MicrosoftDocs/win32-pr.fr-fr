---
description: La \_ méthode GetObjectText de l’objet SWbemLastError retourne un rendu textuel de l’objet au Format format MOF (MOF).
ms.assetid: efe3f3f6-c2f2-4295-bbf3-60d5b06ef98f
ms.tgt_platform: multiple
title: Méthode SWbemLastError.GetObjectText_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7f935457c6fa6566d69c10b6cb5cade914e6e81c175f7451cc6eaff5268358e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679589"
---
# <a name="swbemlasterrorgetobjecttext_-method"></a>Méthode SWbemLastError. GetObjectText \_

La **méthode \_ GetObjectText** de l’objet [**SWbemLastError**](swbemlasterror.md) retourne un rendu textuel de l’objet au format [format MOF (MOF)](managed-object-format--mof-.md) . Cet objet MOF peut être utilisé pour afficher le contenu d’un objet. Notez que le texte MOF qui est retourné ne contient pas toutes les informations relatives à l’objet, mais uniquement les informations nécessaires au compilateur MOF pour pouvoir recréer l’objet d’origine. Par exemple, vous ne trouverez aucune information sur les qualificateurs propagés ou les propriétés de la classe parente.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Ce paramètre est réservé et doit avoir la valeur 0 (zéro) s’il est spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette méthode retourne une chaîne qui contient le texte de sortie.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la **méthode \_ GetObjectText** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

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



 

 




