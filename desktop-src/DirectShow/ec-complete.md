---
description: Toutes les données d’un flux de données particulier ont été rendues.
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: EC_COMPLETE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd6d548a56173b9c6ea83426ddab3fa8556e312
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536007"
---
# <a name="ec_complete"></a>EC \_ complet

Toutes les données d’un flux de données particulier ont été rendues.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) État du flux à la fin de l’opération. Si aucune erreur ne s’est produite lors de la lecture, la valeur est \_ OK.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Zéro, ou un pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du convertisseur.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Par défaut, le gestionnaire de graphes de filtre ne transfère pas cet événement à l’application. Toutefois, une fois que tous les flux du graphique ont été rapportés par la **communauté \_**, le gestionnaire de graphes de filtre publie un événement **ce \_ complet** distinct dans l’application.

Si l’action par défaut est désactivée pour cet événement, l’application reçoit tous les événements d' **\_ achèvement ce** des convertisseurs.

## <a name="remarks"></a>Notes

Un filtre de convertisseur envoie cet événement lorsqu’il reçoit une notification de fin de flux. (La fin de flux est signalée par le biais de la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .) Le filtre envoie exactement un événement **EC \_ Complete** pour chaque flux. Le filtre doit traiter tous les échantillons en attente avant d’envoyer l’événement. L’arrêt d’un convertisseur réinitialise tout état de fin de flux mis en cache.

Si le convertisseur est suspendu, il n’envoie pas la méthode **EC \_ Complete** tant que la méthode [**IMediaFilter :: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) n’est pas appelée. En outre, il continue à envoyer des événements de type « **EC \_ complet** » pour chaque transition de pause à exécuter, jusqu’à ce que le filtre soit arrêté ou vidé.

Les filtres définissent le paramètre *lParam2* sur un pointeur [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) . Si l’action par défaut est activée, le gestionnaire de graphique de filtre définit ce paramètre sur zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> <dt>

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Autres convertisseurs vidéo](alternative-video-renderers.md)
</dt> </dl>

 

 




