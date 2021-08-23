---
description: Efface le nom d’utilisateur du contrôle de carte à puce.
ms.assetid: fff50db5-0610-4985-94c6-96d7ce990219
title: 'ISCrdEnr :: resetUser, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.resetUser
- SCrdEnr.resetUser
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 873872b17684aac3874b82f0570dfac93988356743055088c1916ef3cb41f4a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867899"
---
# <a name="iscrdenrresetuser-method"></a>ISCrdEnr :: resetUser, méthode

La méthode **resetUser** efface le nom d’utilisateur du contrôle de carte à puce.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT resetUser();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="remarks"></a>Remarques

Cette méthode efface du nom d’utilisateur existant et du certificat précédemment inscrit de la mémoire. Toutefois, le certificat précédemment inscrit n’est pas supprimé de la carte à puce.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr :: getUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> <dt>

[**ISCrdEnr :: setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 




