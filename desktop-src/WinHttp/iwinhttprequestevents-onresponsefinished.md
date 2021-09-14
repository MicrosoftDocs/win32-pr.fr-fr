---
description: Se produit lorsque les données de réponse sont terminées.
ms.assetid: 0df2031e-826f-436e-a689-201fa8b5c38f
title: 'Événement IWinHttpRequestEvents :: OnResponseFinished'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d3a596e23028cec0401a21a1ee866ef6e51d9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008333"
---
# <a name="iwinhttprequesteventsonresponsefinished-event"></a>Événement IWinHttpRequestEvents :: OnResponseFinished

L’événement **OnResponseFinished** se produit lorsque les données de réponse sont terminées.

## <a name="syntax"></a>Syntaxe


```C++
void OnResponseFinished();
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cet événement signale que toutes les données de réponse relatives à la demande la plus récente ont été reçues. [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) ne se reproduit pas jusqu’à la requête suivante.

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

 

 




