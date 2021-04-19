---
description: Avertit un filtre de la fenêtre du convertisseur vidéo.
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: EC_NOTIFY_WINDOW (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3165247f05e2fb945f02fee43149b84480bd4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541715"
---
# <a name="ec_notify_window"></a>\_fenêtre EC Notify \_

Avertit un filtre de la fenêtre du convertisseur vidéo.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HWND**) Handle de la fenêtre.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Cet événement est utilisé en interne par DirectShow. Le gestionnaire de graphes de filtre ne transmet pas cet événement à l’application. Les applications ne peuvent pas remplacer l’action par défaut pour cet événement.

## <a name="remarks"></a>Notes

Lorsqu’un convertisseur vidéo est connecté, il vérifie si la broche de sortie en amont prend en charge l’interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) . Si c’est le cas, le convertisseur envoie cet événement au filtre amont.

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

 

 




