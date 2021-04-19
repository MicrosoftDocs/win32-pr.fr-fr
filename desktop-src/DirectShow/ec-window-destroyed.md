---
description: Le convertisseur vidéo a été détruit ou supprimé du graphique.
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: EC_WINDOW_DESTROYED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd3e641c7fb911a8da10a4c89682fa266e862de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532541"
---
# <a name="ec_window_destroyed"></a>\_fenêtre EC \_ détruite

Le convertisseur vidéo a été détruit ou supprimé du graphique.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du convertisseur vidéo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Le gestionnaire de graphes de filtre libère cette fenêtre comme le focus, via l’interface [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) . Elle n’envoie pas la notification d’événement à l’application.

## <a name="remarks"></a>Notes

Le convertisseur vidéo envoie cet événement lorsqu’il quitte le graphique de filtre, dans sa méthode [**IBaseFilter :: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) . (L’envoi de l’événement lorsque le filtre est détruit peut être trop tard, car, à ce stade, le gestionnaire de graphique de filtre peut également être détruit.)

Cet événement permet à d’autres filtres d’acquérir des ressources qui dépendent du focus de la fenêtre, tels que les périphériques audio.

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

 

 




