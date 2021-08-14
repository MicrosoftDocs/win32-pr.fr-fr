---
description: Se produit lorsqu’une erreur d’exécution se produit dans l’application.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: 'IWinHttpRequestEvents :: OnError, événement'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31127dcc3155b804bbda1c3ab94ee8a410c73f5a96c3ecfc6f787479ccd51539
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744337"
---
# <a name="iwinhttprequesteventsonerror-event"></a>IWinHttpRequestEvents :: OnError, événement

L’événement **OnError** se produit lorsqu’une erreur d’exécution se produit dans l’application.

## <a name="syntax"></a>Syntaxe


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Errornumber* \[ dans\]
</dt> <dd>

Reçoit la valeur numérique de l’erreur. Les 16 bits inférieurs de ce numéro d’erreur correspondent à l’une des erreurs figurant dans les [**messages d’erreur**](error-messages.md).

</dd> <dt>

*ErrorDescription* \[ dans\]
</dt> <dd>

Spécifie une brève description de l’erreur qui s’est produite.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

> [!Note]  
> pour Windows XP et Windows 2000, consultez la section [configuration requise](winhttp-start-page.md) pour l’exécution de la Page de démarrage de WinHTTP.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professional avec les \[ applications de bureau SP3 uniquement\]<br/>            |
| Serveur minimal pris en charge<br/> | Windows server 2003, Windows 2000 server avec des \[ applications de bureau SP3 uniquement\]<br/>         |
| Composant redistribuable<br/>          | WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.<br/> |
| MIDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




