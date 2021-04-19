---
description: La taille de la vidéo native a changé.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a70ceab583d8dfc51b417fb701a2988b2e96f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520937"
---
# <a name="ec_video_size_changed"></a>taille de la \_ vidéo ce \_ \_ modifiée

La taille de la vidéo native a changé.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) MOT de poids faible spécifie la nouvelle largeur, en pixels ; MOT de poids fort spécifie la nouvelle hauteur, en pixels.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Aucun.

## <a name="remarks"></a>Notes

Les convertisseurs vidéo peuvent envoyer cet événement s’ils détectent une modification de la taille de la vidéo native.

Le [convertisseur de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7) et le [convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) (VMR-9) envoient cet événement en mode fenêtre, mais pas en mode sans fenêtre ni en mode de rendu. Pour plus d’informations sur le mode fenêtre dans VMR, consultez [rendu vidéo](video-rendering.md).

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

 

 




