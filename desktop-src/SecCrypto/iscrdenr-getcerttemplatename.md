---
description: Récupère le nom du modèle de certificat.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: 'ISCrdEnr :: getCertTemplateName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateName
- SCrdEnr.getCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4eee84140e0a23b8a0dd5d26099ca61b868a90fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210243"
---
# <a name="iscrdenrgetcerttemplatename-method"></a>ISCrdEnr :: getCertTemplateName, méthode

La méthode **getCertTemplateName** récupère le nom du modèle de certificat.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT getCertTemplateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.getCertTemplateName( _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Valeur qui détermine si le nom réel ou le nom complet du modèle de certificat est retourné. Si la valeur de *dwFlags* est le \_ \_ \_ nom complet du \_ modèle \_ de certificat d’inscription au nouveau, le nom complet du modèle de certificat est récupéré ; sinon, le nom réel du modèle de certificat s’affiche.

</dd> <dt>

*pbstrCertTemplateName* \[ à\]
</dt> <dd>

Pointeur vers une chaîne qui retourne le nom du modèle de certificat qui sera utilisé dans la demande de [*certificat*](../secgloss/c-gly.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

### <a name="c"></a>C++

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

### <a name="vb"></a>VB

Chaîne qui représente le nom du modèle de certificat qui sera utilisé dans la demande de [*certificat*](../secgloss/c-gly.md).

## <a name="remarks"></a>Notes

Si vous ne définissez pas le nom du modèle de certificat en appelant [**ISCrdEnr :: setCertTemplateName**](iscrdenr-setcerttemplatename.md), le nom par défaut est le prénom dans la liste des modèles de certificats disponibles.

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

[**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
