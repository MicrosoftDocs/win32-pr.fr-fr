---
description: Indique que la lecture du DVD s’est arrêtée à la suite d’un appel à la méthode IDvdControl2 ::P layChaptersAutoStop.
ms.assetid: ccafaf76-ec8c-4d67-9b29-565f3ed6593b
title: EC_DVD_CHAPTER_AUTOSTOP (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_AUTOSTOP
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: a25c4ea621875403ad47ee6815b07b84572f939e4f2a6713d47aa53ba61f983e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652673"
---
# <a name="ec_dvd_chapter_autostop"></a>\_arrêt du \_ chapitre du DVD ce \_

Indique que la lecture du DVD s’est arrêtée à la suite d’un appel à la méthode [**IDvdControl2 ::P laychaptersautostop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop) .

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

## <a name="remarks"></a>Remarques

Cet événement est déclenché dans le domaine de titre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdevcode. h (inclure DShow. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> <dt>

[Codes de notification des événements DVD](dvd-notification-codes.md)
</dt> <dt>

[Notification d’événements dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




