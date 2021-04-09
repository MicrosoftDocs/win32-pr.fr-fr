---
description: Utilisé pour déterminer si un modèle de certificat contient l' \_ utilisation de la clé de protection de messagerie szOID PKIX \_ \_ \_ .
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: 'ISCrdEnr :: getCertTemplateSMIME, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateSMIME
- SCrdEnr.getCertTemplateSMIME
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4ed66af6a8a91855fbfc5a972a8bf00358314663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867398"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a>ISCrdEnr :: getCertTemplateSMIME, méthode

La méthode **getCertTemplateSMIME** est utilisée pour déterminer si un modèle de certificat contient l' \_ utilisation de la clé de protection de \_ \_ courrier électronique szOID PKIX \_ .

Si l’utilisation de la clé fait partie du modèle de certificat, le modèle de certificat prend en charge les opérations S/MIME ( [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) ).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT getCertTemplateSMIME(
  [in]  BSTR      bstrCertTemplateName,
  [out] DWORD *pdwCertTemplateSMIME
);
```


```VB

SCrdEnr.getCertTemplateSMIME( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCertTemplateSMIME _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrCertTemplateName* \[ dans\]
</dt> <dd>

Nom du certificat interrogé pour l’utilisation de la clé S/MIME.

</dd> <dt>

*pdwCertTemplateSMIME* \[ à\]
</dt> <dd>

Pointeur vers une valeur **DWORD** qui retourne la valeur un si *bstrCertTemplateName* prend en charge S/MIME ; Sinon, elle retourne zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

### <a name="c"></a>C++

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

### <a name="vb"></a>VB

Valeur **longue** d’une si *bstrCertTemplateName* prend en charge S/MIME ; Sinon, zéro.

## <a name="remarks"></a>Notes

La constante pour la \_ protection de la \_ messagerie électronique szOID PKIX \_ \_ est définie dans wincrypt. h.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr :: inscrire**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
