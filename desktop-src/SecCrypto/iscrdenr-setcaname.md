---
description: Spécifie le nom de l’autorité de certification.
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: 'ISCrdEnr :: setCAName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 46dcd9294337c088b9e1b0ab68bddefe4308ed27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120910"
---
# <a name="iscrdenrsetcaname-method"></a>ISCrdEnr :: setCAName, méthode

La méthode **setCAName** spécifie le nom de l' [*autorité de certification*](../secgloss/c-gly.md) (ca).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Valeur qui spécifie si le nom fait référence au nom de l’autorité de certification ou au nom de l’ordinateur de l’autorité de certification. Si cette valeur est un \_ \_ \_ nom d’ordinateur de \_ l’autorité de certification d’inscription au format 0x01 (défini comme 0x01), le nom fait référence au nom de l’ordinateur de l’autorité de certification. Dans le cas contraire, le nom fait référence au nom de l’autorité de certification.

</dd> <dt>

*bstrCertTemplateName* \[ dans\]
</dt> <dd>

Nom du modèle de certificat.

</dd> <dt>

*bstrCAName* \[ dans\]
</dt> <dd>

Nom de l’autorité de certification à utiliser avec le modèle de certificat spécifié par *bstrCertTemplateName*.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

### <a name="vb"></a>VB

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique que l’appel a réussi.

## <a name="remarks"></a>Notes

Utilisez cette méthode pour spécifier une autorité de certification pour un modèle de certificat.

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

[**ISCrdEnr::enumCAName**](iscrdenr-enumcaname.md)
</dt> <dt>

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> </dl>

 

 
