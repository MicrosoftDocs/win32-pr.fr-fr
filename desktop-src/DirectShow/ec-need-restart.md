---
description: Un filtre demande que le graphique soit redémarré.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651ae51b8dd8969a95b4f5e9d5093ec2e879f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527978"
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

## <a name="remarks"></a>Notes

Si un filtre rejette un échantillon au milieu d’un flux, le pin amont arrête de fournir des exemples. Le filtre peut redémarrer le flux en envoyant cet événement. Par exemple, le convertisseur audio peut perdre l’accès au périphérique audio, car une fenêtre vidéo a perdu le focus. À ce stade, le convertisseur audio commence à rejeter des exemples. Lorsqu’il regagne l’accès au périphérique audio, il envoie cet événement pour redémarrer le flux audio.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> <dt>

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




