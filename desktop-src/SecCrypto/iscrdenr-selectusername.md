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
ms.openlocfilehash: 13059775abc8520c39a0ad3dea2d604fc8d65455
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120926"
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

## <a name="return-value"></a>Valeur de retour

### <a name="vb"></a>VB

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

## <a name="remarks"></a>Notes

Utilisez cette méthode pour sélectionner le nom de l’utilisateur. Une fois qu’un nom d’utilisateur a été sélectionné, sa valeur peut être récupérée en appelant la méthode [**ISCrdEnr :: GetUserName**](iscrdenr-getusername.md) .

Une alternative à l’utilisation de l’interface « Select User » consiste à spécifier un utilisateur en appelant la méthode [**ISCrdEnr :: setUserName**](iscrdenr-setusername.md) .

## <a name="requirements"></a>Spécifications



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

 

 




