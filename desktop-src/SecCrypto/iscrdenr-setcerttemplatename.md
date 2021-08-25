---
description: Spécifie le nom du modèle de certificat.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: 'ISCrdEnr :: setCertTemplateName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCertTemplateName
- SCrdEnr.setCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 5f757ead06e5d1769e109bcbfc8e3510f4298f32145d60c4c0bc992a01f3ab36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993039"
---
# <a name="iscrdenrsetcerttemplatename-method"></a>ISCrdEnr :: setCertTemplateName, méthode

La méthode **setCertTemplateName** spécifie le nom du modèle de certificat.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT setCertTemplateName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setCertTemplateName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Valeur qui détermine si le nom complet ou le nom réel du modèle de certificat est défini. Si la valeur de *dwFlags* est le \_ \_ \_ nom complet du \_ modèle \_ de certificat d’inscription infinie, le nom complet du modèle de certificat est défini. Dans le cas contraire, le nom réel du modèle de certificat est défini.

</dd> <dt>

*bstrCertTemplateName* \[ dans\]
</dt> <dd>

Nom du modèle de certificat qui sera utilisé dans la demande de certificat.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

### <a name="vb"></a>VB

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

## <a name="remarks"></a>Remarques

Si vous ne définissez pas le nom du modèle de certificat en appelant **ISCrdEnr :: setCertTemplateName**, le nom par défaut est le prénom dans la liste des modèles de certificats disponibles.

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

[**ISCrdEnr::getCertTemplateName**](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




