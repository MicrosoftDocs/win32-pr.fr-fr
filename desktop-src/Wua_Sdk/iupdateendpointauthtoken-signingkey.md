---
description: Obtient la clé utilisée pour chiffrer les messages sortants protégés par le jeton.
ms.assetid: 1ADBDFC8-E4D9-440B-B310-913213086283
title: 'IUpdateEndpointAuthToken :: SigningKey, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.SigningKey
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: ae9847eb698bfcf0402a550ecb54705c4b3f3a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034037"
---
# <a name="iupdateendpointauthtokensigningkey-method"></a>IUpdateEndpointAuthToken :: SigningKey, méthode

Obtient la clé utilisée pour chiffrer les messages sortants protégés par le jeton.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SigningKey(
  [in, out, unique] BYTE  *pbKey,
  [in, out]         ULONG *pcbKeySize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbKey* \[ in, out\]
</dt> <dd>

Clé utilisée pour chiffrer les messages sortants.

</dd> <dt>

*pcbKeySize* \[ in, out\]
</dt> <dd>

Taille de la clé référencée par le paramètres *pbkey* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite. Sinon, retourne un code d’erreur COM ou Windows.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]<br/>                   |
| Serveur minimal pris en charge<br/> | Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]<br/>                |
| En-tête<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




