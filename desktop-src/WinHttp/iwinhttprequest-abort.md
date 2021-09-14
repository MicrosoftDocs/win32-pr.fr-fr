---
description: La méthode Abort interrompt une méthode d’envoi WinHTTP.
ms.assetid: 8326feef-8611-4441-b52d-74855e6acfff
title: 'IWinHttpRequest :: Abort, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Abort
- WinHttpRequest.Abort
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 56290dfc16f9986cb7d7596c098bb53c207efebe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228318"
---
# <a name="iwinhttprequestabort-method"></a>IWinHttpRequest :: Abort, méthode

La méthode **Abort** interrompt une méthode d' [**envoi**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Abort();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.

## <a name="remarks"></a>Notes

Vous pouvez abandonner à la fois les méthodes d' [**envoi**](iwinhttprequest-send.md) asynchrones et synchrones. Pour abandonner une méthode d' [**envoi**](iwinhttprequest-send.md) synchrone, vous devez appeler **Abort** à partir d’un événement [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) .

> [!Note]  
> pour Windows XP et Windows 2000, consultez la section [configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHttp.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professional avec les \[ applications de bureau SP3 uniquement\]<br/>            |
| Serveur minimal pris en charge<br/> | Windows server 2003, Windows 2000 server avec des \[ applications de bureau SP3 uniquement\]<br/>         |
| Composant redistribuable<br/>          | WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.<br/> |
| MIDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




