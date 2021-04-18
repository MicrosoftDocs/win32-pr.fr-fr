---
description: Fournit des événements pour les services HTTP Microsoft Windows (WinHTTP).
ms.assetid: 0721d7f9-2e84-41a9-be52-89c8d638eb90
title: Interface IWinHttpRequestEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequestEvents
api_type:
- COM
api_location:
- HttpRequest.idl
ms.openlocfilehash: 3cdd0bf10c0d4bd75351ddaab6e88ce7182850fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519503"
---
# <a name="iwinhttprequestevents-interface"></a>Interface IWinHttpRequestEvents

L’interface **IWinHttpRequestEvents** fournit des événements pour les [services http Microsoft Windows (WinHTTP)](about-winhttp.md). Elle utilise uniquement des méthodes d’événement.

## <a name="members"></a>Membres

L’interface **IWinHttpRequestEvents** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWinHttpRequestEvents** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWinHttpRequestEvents** possède ces méthodes.



| Méthode                                                                           | Description                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Se produit lorsqu’une erreur d’exécution se produit dans l’application.<br/> |
| [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) | Se produit lorsque des données sont disponibles à partir de la réponse.<br/>          |
| [**OnResponseFinished**](iwinhttprequestevents-onresponsefinished.md)           | Se produit lorsque les données de réponse sont terminées.<br/>                |
| [**OnResponseStart**](iwinhttprequestevents-onresponsestart.md)                 | Se produit lorsque les données de réponse commencent à être reçues.<br/>      |



 

## <a name="remarks"></a>Notes

La procédure suivante décrit comment s’inscrire pour les notifications.

1.  Obtient une interface [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) en appelant **QueryInterface** sur un objet [**IWinHttpRequest**](iwinhttprequest-interface.md) .
2.  Appelez [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) sur l’interface retournée et transmettez **IID \_ IWinHttpRequestEvents** à *riid*.
3.  Appelez [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) sur le point de connexion retourné et transmettez un pointeur vers une interface **IUnknown** sur un objet qui implémente **IWinHttpRequestEvents** à *punk*.

Les notifications peuvent être arrêtées en appelant [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) sur le point de connexion retourné à l’étape 2.

Pour afficher du code qui s’inscrit pour les notifications COM, consultez la section client de l’article [points de connexion com](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) .

> [!Note]  
> Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]<br/>            |
| Serveur minimal pris en charge<br/> | Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]<br/>         |
| Composant redistribuable<br/>          | WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.<br/> |
| MIDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

