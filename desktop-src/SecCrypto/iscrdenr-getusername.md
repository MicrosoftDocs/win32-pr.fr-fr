---
description: Récupère le nom de l’utilisateur au nom duquel l’inscription de certificat est prévue.
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: 'ISCrdEnr :: getUserName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getUserName
- SCrdEnr.getUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 51f551a704f3a98b932e646c95810f928e73bac7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324750"
---
# <a name="iscrdenrgetusername-method"></a>ISCrdEnr :: getUserName, méthode

La méthode **getUserName** récupère le nom de l’utilisateur au nom duquel l’inscription de certificat est prévue.

Avant d’appeler cette méthode, vous devez spécifier le nom d’utilisateur dans un appel à [**ISCrdEnr :: selectUserName**](iscrdenr-selectusername.md) ou [**ISCrdEnr :: setUserName**](iscrdenr-setusername.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT getUserName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrUserName
);
```


```VB

SCrdEnr.getUserName( _
  ByVal dwFlags, _
  ByRef pbstrUserName _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Cette valeur doit être égale à zéro (0), \_ nom UPN d’inscription cicatrice \_ \_ ou \_ \_ \_ nom compatible avec l’inscription au sam \_ .

Si cette valeur est \_ \_ \_ un nom UPN d’inscription cicatrice, **getUserName** retourne le nom d’utilisateur principal universel (UPN) de l’utilisateur, tel que « someone@example.com ».

Si cette valeur est un \_ \_ \_ nom compatible avec \_ l’inscription en mode Sam, la méthode retourne le nom Sam (Security Access Manager) de l’utilisateur au format « utilisateur de domaine \\ ».

Si cette valeur est égale à zéro, la méthode retourne le nom UPN de l’utilisateur, le cas échéant. Si l’utilisateur n’a pas de nom UPN, la méthode retourne le nom SAM de l’utilisateur.

</dd> <dt>

*pbstrUserName* \[ à\]
</dt> <dd>

Pointeur vers une chaîne qui retourne le nom de l’utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

### <a name="c"></a>C++

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

### <a name="vb"></a>VB

Chaîne qui représente le nom de l’utilisateur.

## <a name="remarks"></a>Notes

Vous pouvez spécifier le nom de l’utilisateur pour lequel la [*carte à puce*](../secgloss/s-gly.md) est émise en appelant [**ISCrdEnr :: setUserName**](iscrdenr-setusername.md) ou [**ISCrdEnr :: selectUserName**](iscrdenr-selectusername.md). Une fois qu’un nom d’utilisateur a été spécifié, sa valeur peut être récupérée en appelant **getUserName**.

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

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> <dt>

[**ISCrdEnr :: setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 
