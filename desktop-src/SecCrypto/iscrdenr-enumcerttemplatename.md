---
description: Énumère les noms de modèles de certificats.
ms.assetid: 4741eb0d-b8e0-468c-8a00-9ccacb52a9a7
title: 'ISCrdEnr :: enumCertTemplateName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCertTemplateName
- SCrdEnr.enumCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a0a4850143cac48ef9b9b853f99153d4daeb4366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534097"
---
# <a name="iscrdenrenumcerttemplatename-method"></a>ISCrdEnr :: enumCertTemplateName, méthode

La méthode **enumCertTemplateName** énumère les noms de modèles de certificats.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT enumCertTemplateName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.enumCertTemplateName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwIndex* \[ dans\]
</dt> <dd>

Index de base zéro de la séquence d’énumération.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Valeur qui détermine si le modèle de certificat énuméré s’applique aux certificats de l’utilisateur ou de l’ordinateur. Si cette valeur est \_ \_ \_ \_ un modèle de certificat d’utilisateur à l’utilisation infinie (défini comme 1), l’énumération s’applique aux modèles de certificats utilisateur. Si cette valeur est \_ \_ \_ \_ un modèle de certificat d’ordinateur d’inscription cicatrice (défini sur 2), l’énumération s’applique aux modèles de certificat d’ordinateur.

</dd> <dt>

*pbstrCertTemplateName* \[ à\]
</dt> <dd>

Pointeur vers une chaîne qui retourne le nom du modèle de certificat énuméré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

### <a name="c"></a>C++

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

### <a name="vb"></a>VB

Chaîne qui contient le nom du modèle de certificat énuméré.

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

[**ISCrdEnr::getCertTemplateCount**](iscrdenr-getcerttemplatecount.md)
</dt> <dt>

[**ISCrdEnr::getCertTemplateName**](iscrdenr-getcerttemplatename.md)
</dt> <dt>

[**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 




