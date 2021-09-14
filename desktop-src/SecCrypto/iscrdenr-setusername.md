---
description: Spécifie le nom de l’utilisateur au nom duquel l’inscription de certificat est prévue.
ms.assetid: e088af63-5064-4b1b-976f-047f52e56af8
title: 'ISCrdEnr :: setUserName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setUserName
- SCrdEnr.setUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: cc2d3157e41fc7ffd9fc0bf7f607de137559e751
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120897"
---
# <a name="iscrdenrsetusername-method"></a>ISCrdEnr :: setUserName, méthode

La méthode **setUserName** spécifie le nom de l’utilisateur au nom duquel l’inscription de certificat est prévue.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT setUserName(
  [in] DWORD dwFlags,
  [in] BSTR bstrUserName
);
```


```VB

SCrdEnr.setUserName( _
  ByVal dwFlags, _
  ByVal bstrUserName _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Cette valeur doit être un \_ nom UPN d’inscription cicatrice \_ \_ (défini comme 1) ou un \_ \_ \_ nom compatible avec l’inscription \_ au Sam (défini sur 2).

Définissez cette valeur sur \_ le nom UPN de l’inscription à l’utilisation de cicatrices \_ \_ , si le nom spécifié dans *bstrUserName* est le nom de principal universel de l’utilisateur, tel que « someone@example.com ». Le nom UPN de l’utilisateur doit correspondre à un nom SAM (Security Access Manager) existant.

Définissez cette valeur sur \_ inscrire \_ \_ un nom compatible sam \_ en cours d’inscription. Si le nom spécifié dans *bstrUserName* est le nom Sam de l’utilisateur au format « utilisateur du domaine \\ ».

</dd> <dt>

*bstrUserName* \[ dans\]
</dt> <dd>

Nom de l'utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

### <a name="vb"></a>VB

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

## <a name="remarks"></a>Notes

Appelez cette méthode pour spécifier le nom d’utilisateur à émettre pour la [*carte à puce*](../secgloss/s-gly.md). Une alternative à **setUserName** est [**ISCrdEnr :: selectUserName**](iscrdenr-selectusername.md).

Une fois qu’un nom d’utilisateur a été spécifié, sa valeur peut être récupérée en appelant [**getUserName**](iscrdenr-getusername.md).

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

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> </dl>

 

 
