---
description: Une image vidéo est prête à être affichée.
ms.assetid: af6198be-9656-49a6-9598-b1c040be5a1a
title: EC_VIDEOFRAMEREADY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 776ab80f5ba3a9e01bf274c46a26d383767f37fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540527"
---
# <a name="ec_videoframeready"></a>\_VIDEOFRAMEREADY EC

Une image vidéo est prête à être affichée.

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

Aucun.

## <a name="remarks"></a>Notes

Le filtre de [source Windows Media](windows-media-source-filter.md) hérité envoie cet événement. Les nouveaux filtres ne doivent pas envoyer cet événement.

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

 

 




