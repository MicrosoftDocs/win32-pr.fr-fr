---
description: Récupère le nombre de modèles de certificats.
ms.assetid: f56e6e72-1562-4c53-b0da-b4bc69511559
title: 'ISCrdEnr :: getCertTemplateCount, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateCount
- SCrdEnr.getCertTemplateCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 86a78f03929bc6cdcfc7b611944b81c59a1c9fc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868209"
---
# <a name="iscrdenrgetcerttemplatecount-method"></a>ISCrdEnr :: getCertTemplateCount, méthode

La méthode **getCertTemplateCount** récupère le nombre de modèles de certificats.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT getCertTemplateCount(
  [in]  DWORD     dwFlags,
  [out] LONG *pdwCertTemplateCount
);
```


```VB

SCrdEnr.getCertTemplateCount( _
  ByVal dwFlags, _
  ByRef pdwCertTemplateCount _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Valeur qui détermine si le modèle est pour les certificats d’utilisateur ou d’ordinateur. Si cette valeur est \_ \_ \_ \_ un modèle de certificat de l’utilisateur avec un quota d’utilisateurs cicatrices (défini sur 1), le nombre renvoyé sera pour les modèles de certificats utilisateur. Si cette valeur est \_ \_ \_ \_ un modèle de certificat d’ordinateur d’inscription cicatrice (défini sur 2), le nombre retourné sera pour les modèles de certificat d’ordinateur.

</dd> <dt>

*pdwCertTemplateCount* \[ à\]
</dt> <dd>

Pointeur vers une **valeur de type long** qui retourne le nombre de modèles de certificats.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

### <a name="c"></a>C++

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

### <a name="vb"></a>VB

Valeur de **type long** qui représente le nombre de modèles de certificats.

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

[**ISCrdEnr::enumCertTemplateName**](iscrdenr-enumcerttemplatename.md)
</dt> </dl>

 

 




