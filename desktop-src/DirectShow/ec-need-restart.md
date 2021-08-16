---
description: Un filtre demande que le graphique soit redémarré.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fae3426048229c19b1d35a061d67d3d1d0a3149a8f820e891987c88405b76f7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820141"
---
# <a name="ec_need_restart"></a>redémarrage de l’EC \_ requis \_

Un filtre demande que le graphique soit redémarré.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Zéro.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Le gestionnaire de graphique de filtre met en pause et redémarre le graphique. Elle ne passe pas l’événement à l’application.

## <a name="remarks"></a>Remarques

Si un filtre rejette un échantillon au milieu d’un flux, le pin amont arrête de fournir des exemples. Le filtre peut redémarrer le flux en envoyant cet événement. Par exemple, le convertisseur audio peut perdre l’accès au périphérique audio, car une fenêtre vidéo a perdu le focus. À ce stade, le convertisseur audio commence à rejeter des exemples. Lorsqu’il regagne l’accès au périphérique audio, il envoie cet événement pour redémarrer le flux audio.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> <dt>

[Notification d’événements dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




