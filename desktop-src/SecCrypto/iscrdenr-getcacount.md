---
description: Retourne le nombre d’autorités de certification (ca) disposé à émettre un certificat basé sur le modèle de certificat spécifié.
ms.assetid: 377121a8-3895-4308-a803-4a62580c6de0
title: 'ISCrdEnr :: getCACount, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCACount
- SCrdEnr.getCACount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: eb33f6c7345862dedf6c909054d811ff4da470ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237558"
---
# <a name="iscrdenrgetcacount-method"></a>ISCrdEnr :: getCACount, méthode

La méthode **getCACount** retourne le nombre d' [*autorités de certification*](../secgloss/c-gly.md) prêtes à émettre un certificat basé sur le modèle de certificat spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT getCACount(
  [in]  BSTR     bstrCertTemplateName,
  [out] LONG *pdwCACount
);
```


```VB

SCrdEnr.getCACount( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCACount _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrCertTemplateName* \[ dans\]
</dt> <dd>

Chaîne qui représente le nom du modèle de certificat.

</dd> <dt>

*pdwCACount* \[ à\]
</dt> <dd>

Pointeur vers une **valeur de type long** qui retourne le nombre d’autorités de certification disponibles qui émettra un certificat pour le modèle de certificat spécifié dans *bstrCertTemplateName*.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

### <a name="c"></a>C++

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

### <a name="vb"></a>VB

Valeur de **type long** qui représente le nombre d’autorités de certification disponibles qui émettra un certificat pour le modèle de certificat spécifié dans *bstrCertTemplateName*.

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

 

 
