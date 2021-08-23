---
description: 'la méthode Connecter connecte le pin à un autre code confidentiel. cette méthode implémente la méthode IPin :: Connecter.'
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: CBasePin. méthode Connecter (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a134b87e9c7c4d0f665ae37df7ec9cd0ecb3a37c0d0548f27835ead7b8ecca21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074793"
---
# <a name="cbasepinconnect-method"></a>CBasePin. méthode Connecter

La `Connect` méthode connecte le pin à un autre code confidentiel. cette méthode implémente la méthode [**IPin :: Connecter**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Connect(
         IPin          *pReceivePin,
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du pin de réception.

</dd> <dt>

*crédit* 
</dt> <dd>

Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui spécifie le type de média pour la connexion.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                                  | Description                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Réussite.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ déjà \_ connecté**</dt> </dl>    | Le pin est déjà connecté.<br/>                                           |
| <dl> <dt>**VFW \_ E \_ aucun \_ \_ type acceptable**</dt> </dl> | Impossible de trouver un type de média acceptable.<br/>                                |
| <dl> <dt>**VFW \_ E \_ non \_ arrêté**</dt> </dl>          | Le filtre est actif et le code confidentiel ne prend pas en charge la reconnexion dynamique.<br/> |
| <dl> <dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt> </dl>   | Le type de média spécifié n’est pas acceptable.<br/>                             |



 

## <a name="remarks"></a>Remarques

Le paramètre *VPM* peut avoir la **valeur null**. Il peut également spécifier un type de média partiel, avec la valeur GUID \_ null pour le type, le sous-type ou le format principal.

Dans la classe de base, cette méthode teste si le pin est déjà connecté et si le filtre est arrêté. Elle délègue le reste du processus de connexion à la méthode [**CBasePin :: AgreeMediaType**](cbasepin-agreemediatype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




