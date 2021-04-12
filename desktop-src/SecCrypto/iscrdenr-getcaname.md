---
description: Récupère le nom de l’autorité de certification (CA) spécifiée pour un modèle de certificat donné.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: 'ISCrdEnr :: getCAName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCAName
- SCrdEnr.getCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b62b0a7e871a29ff0a8edd28eb8cd5e18e97c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210245"
---
# <a name="iscrdenrgetcaname-method"></a>ISCrdEnr :: getCAName, méthode

La méthode **getCAName** récupère le nom de l’autorité de [*certification*](../secgloss/c-gly.md) (ca) spécifiée pour un modèle de certificat donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT getCAName(
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.getCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Valeur qui détermine si le nom fait référence au nom de l’autorité de certification ou au nom de l’ordinateur de l’autorité de certification. Si cette valeur est un \_ \_ \_ \_ nom d’ordinateur d’autorité de certification d’inscription cicatrice (défini comme 0x01), le nom fait référence au nom d’ordinateur de l’autorité de certification ; sinon, le nom fait référence au nom de l’autorité de certification.

</dd> <dt>

*bstrCertTemplateName* \[ dans\]
</dt> <dd>

Nom du modèle de certificat.

</dd> <dt>

*pbstrCAName* \[ à\]
</dt> <dd>

Pointeur vers une chaîne qui retourne le nom de l’autorité de certification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

### <a name="c"></a>C++

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

### <a name="vb"></a>VB

Chaîne qui représente le nom de l’autorité de certification.

## <a name="remarks"></a>Notes

Le nom de l’autorité de certification par défaut est le prénom dans la liste des autorités de certification disponibles.

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

[**ISCrdEnr::enumCAName**](iscrdenr-enumcaname.md)
</dt> <dt>

[**ISCrdEnr::getCACount**](iscrdenr-getcacount.md)
</dt> <dt>

[**ISCrdEnr::setCAName**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
