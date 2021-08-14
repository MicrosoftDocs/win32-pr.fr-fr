---
description: Affiche une interface utilisateur de sélection, qui permet de sélectionner un nom d’utilisateur.
ms.assetid: 0a02d9e5-b2cf-4818-a2e1-89e6019e53d4
title: 'ISCrdEnr :: selectUserName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectUserName
- SCrdEnr.selectUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b6414b78c07f9dff8761456f92b1088c5ed7eb6c23e7c7ed0eb2cd3980677dca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409419"
---
# <a name="iscrdenrselectusername-method"></a>ISCrdEnr :: selectUserName, méthode

La méthode **selectUserName** affiche une interface **utilisateur Select** , qui permet de sélectionner un nom d’utilisateur.

Le nom d’utilisateur s’applique à l’utilisateur au nom duquel l’inscription de certificat est prévue.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT selectUserName(
  [in] DWORD dwFlags
);
```


```VB

SCrdEnr.selectUserName( _
  ByVal dwFlags _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Réservé pour un usage futur. Définissez cette valeur sur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

### <a name="vb"></a>VB

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

## <a name="remarks"></a>Remarques

Utilisez cette méthode pour sélectionner le nom de l’utilisateur. Une fois qu’un nom d’utilisateur a été sélectionné, sa valeur peut être récupérée en appelant la méthode [**ISCrdEnr :: GetUserName**](iscrdenr-getusername.md) .

Une alternative à l’utilisation de l’interface « Select User » consiste à spécifier un utilisateur en appelant la méthode [**ISCrdEnr :: setUserName**](iscrdenr-setusername.md) .

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

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr :: setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 




