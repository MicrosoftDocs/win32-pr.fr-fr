---
description: Récupère le corps d’entité de réponse sous la forme d’un tableau d’octets non signés.
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: 'IWinHttpRequest :: ResponseBody, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseBody
- IWinHttpRequest.get_ResponseBody
- WinHttpRequest.ResponseBody
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 5a608f2744ad2880ecf7c4862b03821afcef9630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528348"
---
# <a name="iwinhttprequestresponsebody-property"></a>IWinHttpRequest :: ResponseBody, propriété

La propriété **ResponseBody** récupère le corps d’entité de réponse sous la forme d’un tableau d’octets non signés.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_ResponseBody(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseBody = WinHttpRequest.ResponseBody
```





## <a name="property-value"></a>Valeur de la propriété

Valeur de **type Variant** qui reçoit le corps d’entité de réponse sous la forme d’un tableau d’octets non signés. Ce tableau contient les données brutes telles qu’elles ont été reçues directement à partir du serveur.

## <a name="error-codes"></a>Codes d’erreur

La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.

## <a name="remarks"></a>Notes

Cette propriété retourne les données de réponse dans un tableau d’octets non signés. Si la réponse n’a pas de corps de réponse, un variant vide est retourné. Cette propriété ne peut être appelée qu’une fois que la méthode [**Send**](iwinhttprequest-send.md) a été appelée.

> [!Note]  
> Pour plus d’informations sur l’implémentation de pour Windows XP et Windows 2000, consultez [Configuration requise](winhttp-start-page.md)pour l’exécution.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]<br/>            |
| Serveur minimal pris en charge<br/> | Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]<br/>         |
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

[**ResponseStream**](iwinhttprequest-responsestream.md)
</dt> <dt>

[**ResponseText**](iwinhttprequest-responsetext.md)
</dt> <dt>

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




