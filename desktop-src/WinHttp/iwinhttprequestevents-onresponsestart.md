---
description: Se produit lorsque les données de réponse commencent à être reçues.
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: 'Événement IWinHttpRequestEvents :: OnResponseStart'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a299c535dd854bff07f2c24989096f7b9e49fc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008326"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a>Événement IWinHttpRequestEvents :: OnResponseStart

L’événement **OnResponseStart** se produit lorsque les données de réponse commencent à être reçues.

## <a name="syntax"></a>Syntaxe


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*État* \[ dans\]
</dt> <dd>

Reçoit le code d’état standard retourné avec les données de réponse. Les codes d’État sont définis dans le [document RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

</dd> <dt>

*ContentType* \[ dans\]
</dt> <dd>

Spécifie le type de contenu reçu, par exemple « text/html » ou « image/GIF ».

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Pour que cet événement se produise, utilisez [**Open**](iwinhttprequest-open.md) pour envoyer une connexion http en mode asynchrone et utilisez [**Send**](iwinhttprequest-send.md) pour envoyer une demande de données à un serveur Internet.

Il s’agit du premier événement WinHTTP qui se produit après l' [**envoi**](iwinhttprequest-send.md).

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

 

 




