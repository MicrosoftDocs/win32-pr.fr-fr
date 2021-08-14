---
title: IMsRdpDrive propriété RedirectionState
description: Indique l’état de redirection du lecteur.
ms.assetid: 05333671-460d-4c07-8b7e-fbb7bc215353
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectionState
- Services Bureau à distance de la propriété RedirectionState, interface IMsRdpDrive
- Services Bureau à distance de l’interface IMsRdpDrive, propriété RedirectionState
topic_type:
- apiref
api_name:
- IMsRdpDrive.RedirectionState
- IMsRdpDrive.get_RedirectionState
- IMsRdpDrive.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6069ec911210fac3f4334bdf9e84da080e5536a4f4b6cfc7aca0e54fe0bd2228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351957"
---
# <a name="imsrdpdriveredirectionstate-property"></a>IMsRdpDrive :: RedirectionState, propriété

Indique l’état de redirection du lecteur.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a>Valeur de la propriété

Affectez à ce paramètre la valeur **Variant \_ false**. pour désactiver la redirection ou la **variante \_ true**. pour activer la redirection.

## <a name="error-codes"></a>Codes d’erreur

Si la méthode est réussie, **S \_ OK** est retourné. Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDrive est défini en tant que d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

 





