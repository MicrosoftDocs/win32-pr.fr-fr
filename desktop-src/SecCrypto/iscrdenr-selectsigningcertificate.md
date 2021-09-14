---
description: Affiche une boîte de dialogue Sélectionner un certificat, qui permet de sélectionner un certificat de signature (également appelé certificat de l’agent d’inscription).
ms.assetid: b8198f65-4ffb-4dfa-8286-e62ef483ab16
title: 'ISCrdEnr :: selectSigningCertificate, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectSigningCertificate
- SCrdEnr.selectSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a4ef3be0ef16797597f57c12e90736ba50109601
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120922"
---
# <a name="iscrdenrselectsigningcertificate-method"></a>ISCrdEnr :: selectSigningCertificate, méthode

La méthode **selectSigningCertificate** affiche une boîte de dialogue **Sélectionner un certificat** , qui permet de sélectionner un certificat de signature (également appelé *certificat de l’agent d’inscription*).

Avant de procéder à l’inscription au nom des utilisateurs, vous devez sélectionner un certificat de signature. La [*clé privée*](../secgloss/p-gly.md) associée à ce certificat de signature est utilisée pour signer une \# demande PKCS 7. Le PKCS \# 7, quant à lui, contient la requête PKCS 10 de l’utilisateur \# (qui est signée avec la clé privée de l’utilisateur).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT selectSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.selectSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Réservé pour un usage futur. Définissez cette valeur sur zéro.

</dd> <dt>

*bstrCertTemplateName* \[ dans\]
</dt> <dd>

Chaîne qui représente le nom du modèle de certificat pour le certificat de signature. Vous pouvez utiliser la valeur « EnrollmentAgent » si vous avez obtenu un certificat EnrollmentAgent.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

### <a name="vb"></a>VB

Si la méthode est réussie, la méthode retourne **S \_ OK**.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

## <a name="remarks"></a>Notes

Avant de procéder à l’inscription pour le compte d’un utilisateur, vous devez d’abord obtenir un certificat de signature. Vous pouvez obtenir un certificat de signature à l’aide du composant logiciel enfichable MMC du gestionnaire de certificats. La méthode **selectSigningCertificate** n’obtient pas le certificat de signature, mais affiche une boîte de dialogue des certificats de signature précédemment obtenus, ce qui vous permet de choisir le certificat qui sera utilisé pour signer les demandes d’inscription à la place.

Une alternative à **selectSigningCertificate** est [**ISCrdEnr :: setSigningCertificate**](iscrdenr-setsigningcertificate.md).

Une fois le certificat de signature sélectionné, son nom peut être récupéré en appelant [**ISCrdEnr :: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).

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

[**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
