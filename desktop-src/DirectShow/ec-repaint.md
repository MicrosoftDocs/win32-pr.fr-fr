---
description: Un convertisseur vidéo requiert un redessin.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7edd498d84aaace460a10c88d5579c2f5a87bba42e1a5f393786134bbe727af3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102789"
---
# <a name="ec_repaint"></a>redessin ce \_

Un convertisseur vidéo requiert un redessin.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche d’entrée du convertisseur vidéo, ou **null**.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Le paramètre *lParam1* peut spécifier la broche d’entrée du convertisseur vidéo. Si c’est le cas, le gestionnaire de graphique de filtre recherche la broche de sortie connectée à ce code confidentiel et l’interroge pour l’interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) . Si la broche de sortie prend en charge **IMediaEventSink**, le gestionnaire de graphique de filtre appelle [**IMediaEventSink :: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) avec le \_ code d’événement de redessin ce. Cela donne au filtre en amont la possibilité de renvoyer le dernier échantillon.

Si *lParam1* a la **valeur null**, ou si le code PIN ne prend pas en charge [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink), ou si la méthode [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) échoue, le gestionnaire de graphique de filtre gère l' \_ événement de redessin ce par lui-même. Son comportement dépend de l’état du graphique :

-   Running : ignore l’événement. (Le convertisseur recevra l’exemple suivant dans le flux.)
-   Paused : recherche le graphique à son emplacement actuel, ce qui a pour effet de vider le filtre et de remettre les données en file d’attente.
-   Arrêté : suspend et arrête le graphique, ce qui a pour effet de replacer en file d’attente les données.

Par défaut, le gestionnaire de graphes de filtre ne transmet pas cet événement à l’application.

## <a name="remarks"></a>Remarques

Les convertisseurs vidéo envoient ce message lorsqu’ils reçoivent un message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) et n’ont pas de données à afficher.

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

 

