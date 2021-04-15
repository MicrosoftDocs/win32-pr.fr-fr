---
title: Méthode IMsTscNonScriptable ResetPassword
description: Réinitialise tous les États de mot de passe dans le contrôle ActiveX Bureau à distance.
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ResetPassword
- Méthode ResetPassword Services Bureau à distance, interface IMsTscNonScriptable
- Services Bureau à distance de l’interface IMsTscNonScriptable, méthode ResetPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ResetPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0401b97d1b16fda97ba706aef5b795b9f9bc0f3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466751"
---
# <a name="imstscnonscriptableresetpassword-method"></a>IMsTscNonScriptable :: ResetPassword, méthode

Réinitialise tous les États de mot de passe dans le contrôle ActiveX Bureau à distance. Vous pouvez appeler cette méthode pour effacer les mots de passe qui sont stockés dans l’un des trois formats pris en charge : texte en clair, encodé portable ou encodé binaire (non transférable). Notez que les mots de passe encodés ne doivent pas être considérés comme étant chiffrés de manière sécurisée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Vous pouvez appeler cette méthode pour réinitialiser le mot de passe du contrôle après la déconnexion. Cela garantit que les connexions suivantes qui utilisent la même instance du contrôle ne se connectent pas automatiquement avec un mot de passe défini précédemment.

Vous pouvez appeler cette méthode uniquement lorsque le Bureau à distance contrôle ActiveX n’est pas dans l’état connecté. Cette méthode retourne **E \_ Fail** si elle est appelée lorsque le contrôle est connecté. Pour vérifier l’état connecté, appelez la méthode [**obtenir la \_ connexion**](imstscax-connected.md) par le biais de l’interface [**IMsTscAx**](imstscax-interface.md) ou de l’une des interfaces qui en hérite.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable est défini en tant que c1e6743a-41c1-4a74-832a-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





