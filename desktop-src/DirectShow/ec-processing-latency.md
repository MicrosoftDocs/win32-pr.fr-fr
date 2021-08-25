---
description: Indique la durée pendant laquelle un composant prend le traitement de chaque échantillon.
ms.assetid: 84f81ee1-76d8-46fb-86ef-2500f8f4ef36
title: EC_PROCESSING_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceb107dd4c895f9819d268e6112c22c0c514e480bf778692f28bc87853aee9bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792619"
---
# <a name="ec_processing_latency"></a>\_latence de traitement ce \_

Indique la durée pendant laquelle un composant prend le traitement de chaque échantillon.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const Reference \_ Time**) durée de \* traitement de chaque échantillon, en unités de 100 nanosecondes.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Aucun.

## <a name="remarks"></a>Notes

Un présentateur pour le filtre EVR ( [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) ) peut envoyer ce message à EVR pour notifier le EVR de la latence de traitement du présentateur.

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

 

 




