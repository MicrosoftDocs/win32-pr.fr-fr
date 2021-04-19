---
description: Énumère le nom des autorités de certification (ca) pour un nom de modèle de certificat donné.
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: 'ISCrdEnr :: enumCAName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCAName
- SCrdEnr.enumCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: c23df2f74cdf3791f1280e38cbff8ddd48f924b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518899"
---
# <a name="iscrdenrenumcaname-method"></a>ISCrdEnr :: enumCAName, méthode

La méthode **enumCAName** énumère le nom des autorités de [*certification*](../secgloss/c-gly.md) (ca) pour un nom de modèle de certificat donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT enumCAName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.enumCAName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
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

Valeur qui détermine si le nom fait référence au nom de l’autorité de certification ou au nom de l’ordinateur de l’autorité de certification. Si cette valeur est un \_ \_ \_ nom d’ordinateur de \_ l’autorité de certification d’inscription au format 0x01 (défini comme 0x01), le nom fait référence au nom de l’ordinateur de l’autorité de certification. Dans le cas contraire, le nom fait référence au nom de l’autorité de certification.

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

[**ISCrdEnr::getCACount**](iscrdenr-getcacount.md)
</dt> <dt>

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> <dt>

[**ISCrdEnr::setCAName**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
