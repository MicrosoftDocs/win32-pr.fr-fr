---
description: Une fenêtre vidéo est en cours d’activation ou de désactivation.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14d9b0ad192045f179d9f0f366eed6a32efb0e6cc6f61b47255f118b7f55258
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966059"
---
# <a name="ec_activate"></a>\_activation EC

Une fenêtre vidéo est en cours d’activation ou de désactivation.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**Bool**) **True** si la fenêtre est activée ou **false** si la fenêtre est désactivée.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du convertisseur.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Le gestionnaire de graphique de filtre définit le focus, via l’interface [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) . Elle n’envoie pas la notification d’événement à l’application.

## <a name="remarks"></a>Remarques

Un convertisseur vidéo envoie cet événement chaque fois que sa fenêtre est activée ou désactivée (autrement dit, lorsqu’il reçoit un \_ message WM ACTIVATEAPP). L’activation ou la désactivation de la fenêtre peut se produire parce que la fenêtre a obtenu ou perdu le focus, ou parce que le convertisseur a basculé entre le mode plein écran et le mode fenêtre.

Cet événement permet au gestionnaire de graphes de filtre d’allouer des ressources qui dépendent du focus de la fenêtre, telles que les périphériques audio.

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

 

 




