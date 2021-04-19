---
description: Le \_ message de bouton téléphone TAPI est envoyé pour notifier l’application que la surveillance de l’appui sur les boutons est activée si elle a détecté une pression de bouton sur le téléphone local.
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: Message PHONE_BUTTON (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da810630a937f8415e070373f359dca06a694e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532670"
---
# <a name="phone_button-message"></a>\_Message du bouton téléphone

Le message **de \_ bouton téléphone** TAPI est envoyé pour notifier l’application que la surveillance de l’appui sur les boutons est activée si elle a détecté une pression de bouton sur le téléphone local.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPhone* 
</dt> <dd>

Handle vers l’appareil mobile.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel de l’application fournie lors de l’ouverture du périphérique téléphonique.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificateur de bouton/lampe du bouton sur lequel l’utilisateur a appuyé. Notez que les identificateurs de bouton allant de 0 à 11 sont toujours les boutons du clavier, « 0 » étant l’identificateur de bouton zéro, « 1 » étant l’identificateur de bouton 1 (et ainsi de suite jusqu’à l’identificateur de bouton 9) et « » est l’identificateur de \* bouton 10 et « » \# est l’identificateur de bouton 11. Des informations supplémentaires sur un identificateur de bouton sont disponibles avec [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) et [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Mode du bouton. Ce paramètre utilise l’une des [**\_ constantes PHONEBUTTONMODE**](phonebuttonmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Spécifie s’il s’agit d’un événement de bouton ou de bouton. Ce paramètre utilise l’une des [**\_ constantes PHONEBUTTONSTATE**](phonebuttonstate--constants.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Un message de **\_ bouton téléphone** est envoyé chaque fois qu’un bouton change d’État. Une application garantit que pour chaque événement de clic de bouton, il reçoit finalement un événement de rebours de bouton correspondant. Un fournisseur de services qui ne peut pas détecter le bouton vers le haut est requis pour générer le message de bouton vers le haut peu après le bouton enfoncé pour chaque pression sur le bouton.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




