---
description: Le graphique met en mémoire tampon des données ou a arrêté la mise en mémoire tampon des données.
ms.assetid: 39e8b151-0323-42b3-99f0-3dcd230925c8
title: EC_BUFFERING_DATA (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc937973db8435657d131ff4adea83892bf87681bb3db9b7d016565f5c38670
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965969"
---
# <a name="ec_buffering_data"></a>\_données de mise en mémoire tampon EC \_

Le graphique met en mémoire tampon des données ou a arrêté la mise en mémoire tampon des données.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**Bool**) **True** si le graphique commence à être mis en mémoire tampon, ou **false** si le graphique a cessé de mettre en mémoire tampon.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Aucun.

## <a name="remarks"></a>Notes

Un filtre peut envoyer cet événement s’il doit mettre en mémoire tampon des données à partir d’une source externe. (Par exemple, il peut charger des données à partir d’un réseau.) L’application peut utiliser cet événement pour ajuster son interface utilisateur.

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

 

 




