---
description: 'La méthode ReceiveConnection accepte une connexion à partir d’un autre code PIN. Cette méthode implémente la méthode IPin :: ReceiveConnection.'
ms.assetid: f17e7d93-ac45-4b8a-98c6-0c76ec7117c9
title: Méthode CBasePin. ReceiveConnection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ReceiveConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d0a8134201af1d3c931121f59a20360020a53a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537992"
---
# <a name="cbasepinreceiveconnection-method"></a>Méthode CBasePin. ReceiveConnection

La `ReceiveConnection` méthode accepte une connexion à partir d’un autre code PIN. Cette méthode implémente la méthode [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReceiveConnection(
   IPin          *pConnector,
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pConnector* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du code PIN de connexion.

</dd> <dt>

*crédit* 
</dt> <dd>

Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui spécifie le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                                | Description                                                                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Opération réussie.<br/>                                                                |
| <dl> <dt>**\_pointeur E**</dt> </dl>                  | Argument de pointeur **null** .<br/>                                              |
| <dl> <dt>**VFW \_ E \_ déjà \_ connecté**</dt> </dl>  | Le pin est déjà connecté.<br/>                                           |
| <dl> <dt>**VFW \_ E \_ non \_ arrêté**</dt> </dl>        | Le filtre est actif et le code confidentiel ne prend pas en charge la reconnexion dynamique.<br/> |
| <dl> <dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt> </dl> | Le type de média spécifié n’est pas acceptable.<br/>                             |



 

## <a name="remarks"></a>Notes

La broche de sortie appelle cette méthode sur la broche d’entrée. Si la broche d’entrée retourne un code d’erreur, la connexion échoue.

Dans la classe de base, cette méthode effectue les étapes suivantes :

-   Vérifie si le code PIN est déjà connecté.
-   Vérifie si le filtre est arrêté.
-   Appelle la méthode [**CBasePin :: CheckConnect**](cbasepin-checkconnect.md) pour tester si le code confidentiel de connexion est approprié.
-   Appelle la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) pour tester si le type de média est acceptable.

Si toutes ces étapes réussissent, la méthode appelle les méthodes [**CBasePin :: CompleteConnect**](cbasepin-completeconnect.md) et [**SetMediaType**](cbasepin-setmediatype.md) pour terminer la connexion. Ces méthodes stockent le type de média et un pointeur vers la broche de sortie.

Si **CheckConnect** ou **CheckMediaType** échouent, la classe de base appelle la méthode [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) pour rompre la connexion, puis retourne un code d’erreur à partir de `ReceiveConnection` .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




