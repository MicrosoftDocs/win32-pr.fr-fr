---
description: Récupère le nom du sujet à partir du certificat de signature.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: 'ISCrdEnr :: getSigningCertificateName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getSigningCertificateName
- SCrdEnr.getSigningCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 8d9a8a84067e82a18e5066721f3e7f39d075c339
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324753"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a>ISCrdEnr :: getSigningCertificateName, méthode

La méthode **getSigningCertificateName** récupère le nom du sujet à partir du certificat de signature.

Cette méthode peut également être utilisée pour afficher le certificat dans une boîte de dialogue. Cette méthode appelle la [](../secgloss/c-gly.md) fonction CryptoAPI [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT getSigningCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrSigningCertName
);
```


```VB

SCrdEnr.getSigningCertificateName( _
  ByVal dwFlags, _
  ByRef pbstrSigningCertName _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Valeur qui détermine si le certificat est affiché dans une boîte de dialogue. Si cette valeur est \_ \_ incorrecte inscrire aucun certificat d' \_ affichage \_ (défini comme 0x01), le certificat de signature n’est pas affiché ; toutes les autres valeurs entraînent l’affichage du certificat de signature dans la boîte de dialogue **certificat** .

</dd> <dt>

*pbstrSigningCertName* \[ à\]
</dt> <dd>

Pointeur vers une chaîne qui retourne le nom du certificat de signature. Le certificat de signature est utilisé pour signer la [*demande de certificat*](../secgloss/c-gly.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

### <a name="c"></a>C++

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

### <a name="vb"></a>VB

Chaîne qui représente le nom du certificat de signature. Le certificat de signature est utilisé pour signer la [*demande de certificat*](../secgloss/c-gly.md).

## <a name="remarks"></a>Notes

La méthode **getSigningCertificateName** retourne le nom du sujet du certificat que vous (ou un autre administrateur) avez sélectionné lors d’un appel précédent réussi à [**ISCrdEnr :: selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) ou [**ISCrdEnr :: setSigningCertificate**](iscrdenr-setsigningcertificate.md). Cette méthode appelle la fonction [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) pour récupérer le nom de l’objet en fonction de la séquence décrite pour la \_ \_ \_ \_ valeur de type d’affichage simple du nom de certificat du paramètre *dwType* de **CertGetNameString**.

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

[**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
