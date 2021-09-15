---
description: 'Récupère le nom du certificat résultant d’un appel antérieur réussi à ISCrdEnr :: Enroll.'
ms.assetid: e33b217a-b717-49bd-b0f3-3ba9229a0696
title: 'ISCrdEnr :: getEnrolledCertificateName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getEnrolledCertificateName
- SCrdEnr.getEnrolledCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3c9640e7719d2b5ac0e576384246cda5e1b2bfe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311305"
---
# <a name="iscrdenrgetenrolledcertificatename-method"></a>ISCrdEnr :: getEnrolledCertificateName, méthode

La méthode **getEnrolledCertificateName** récupère le nom du certificat résultant d’un appel antérieur réussi à [**ISCrdEnr :: ENROLL**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).

Cette méthode peut également être utilisée pour afficher le certificat dans une boîte de dialogue. Cette méthode appelle la [](../secgloss/c-gly.md) fonction CryptoAPI [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT getEnrolledCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pBstrCertName
);
```


```VB

SCrdEnr.getEnrolledCertificateName( _
  ByVal dwFlags, _
  ByRef pBstrCertName _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Valeur qui détermine si le certificat est affiché dans une boîte de dialogue. Si cette valeur est \_ \_ \_ \_ incorrecte inscrire aucun certificat d’affichage (défini comme 0x01), le certificat inscrit n’est pas affiché ; toute autre valeur entraîne l’affichage du certificat inscrit dans la boîte de dialogue **certificat** .

</dd> <dt>

*pBstrCertName* \[ à\]
</dt> <dd>

Pointeur vers une chaîne qui retourne le nom du certificat récupéré.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

### <a name="c"></a>C++

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

### <a name="vb"></a>VB

Chaîne qui représente le nom du certificat récupéré.

## <a name="remarks"></a>Notes

Étant donné que cette méthode fonctionne sur un certificat existant, vous devez avoir appelé [**ISCrdEnr :: ENROLL**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) avant de pouvoir appeler **getEnrolledCertificateName**.

La méthode **getEnrolledCertificateName** appelle la fonction [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) pour récupérer le nom du certificat en fonction de la séquence décrite pour la \_ \_ \_ valeur de type d’affichage simple du nom de certificat \_ du paramètre *dwType* de **CertGetNameString**.

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

[**ISCrdEnr :: inscrire**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
