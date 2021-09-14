---
description: Se produit lorsque des données sont disponibles à partir de la réponse.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: 'Événement IWinHttpRequestEvents :: OnResponseDataAvailable'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cb2fbc680b1f6739a66bb68565188c8a5d78b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008334"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a>Événement IWinHttpRequestEvents :: OnResponseDataAvailable

L’événement **OnResponseDataAvailable** se produit lorsque des données sont disponibles à partir de la réponse.

## <a name="syntax"></a>Syntaxe


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Données* \[ dans\]
</dt> <dd>

tableau de base zéro d’octets qui reçoit les données de réponse reçues par Microsoft Windows HTTP Services (WinHTTP) jusqu’au point que cet événement se produit. Il s’agit d’une **variante** de type VT \_ array \| VT \_ UI1.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Comme les données sont en octets, elles doivent être converties en caractères larges lorsqu’elles sont placées dans une chaîne à caractères larges (Unicode).

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

 

 




