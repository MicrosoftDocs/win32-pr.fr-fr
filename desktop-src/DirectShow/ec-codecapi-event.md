---
description: "L' \\_ \\_ événement d’événement EC CODECAPI est envoyé par un encodeur pour signaler un événement d’encodage. Le client s’inscrit à l’événement d’encodeur en appelant la méthode ICodecAPI :: RegisterForEvent."
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5765c2a1156653e66c5d3685cacfdd551cd22032eea34463f5450dc6d4fbea3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965939"
---
# <a name="ec_codecapi_event"></a>\_événement EC CODECAPI \_

L' \_ \_ événement d’événement EC CODECAPI est envoyé par un encodeur pour signaler un événement d’encodage. Le client s’inscrit à l’événement d’encodeur en appelant la méthode [**ICodecAPI :: RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Données utilisateur. La valeur de ce paramètre est le pointeur que l’appelant a spécifié dans le paramètre *UserData* de la méthode [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Pointeur vers les données d’événement. Ces données sont allouées par l’encodeur et doivent être libérées par l’application, à l’aide de la fonction **CoTaskMemFree** . Le bloc de données commence par une structure [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) ; Effectuez un cast du paramètre *lParam2* en un pointeur vers cette structure.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Aucune action par défaut.

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

 

 




