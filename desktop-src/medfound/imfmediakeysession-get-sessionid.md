---
description: Obtient un ID de session unique créé pour cette session.
ms.assetid: 779ebea9-69ff-469a-8ee0-06d570ede6cb
title: 'IMFMediaKeySession :: get_SessionId, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.get_SessionId
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 7110dbe6c24d1189019fb242621c7e3c01253264
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106531247"
---
# <a name="imfmediakeysessionget_sessionid-method"></a>IMFMediaKeySession :: obtient \_ SessionID, méthode

Obtient un ID de session unique créé pour cette session.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_SessionId(
   BSTR *sessionId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sessionId* 
</dt> <dd>

ID de session de la clé du support.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFMediaKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




