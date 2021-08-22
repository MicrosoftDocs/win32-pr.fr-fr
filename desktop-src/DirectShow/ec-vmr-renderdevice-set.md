---
description: Envoyé lorsque VMR a sélectionné son mécanisme de rendu.
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: EC_VMR_RENDERDEVICE_SET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc2c8bef78156c4438e1e4e7aea45326562002ed8f4a3786377d7ee43a00a57c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015857"
---
# <a name="ec_vmr_renderdevice_set"></a>\_ \_ jeu RENDERDEVICE EC \_ VMR

Envoyé lorsque VMR a sélectionné son mécanisme de rendu.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Peut prendre l’une des valeurs suivantes :



| Valeur                        | Signification                                                  |
|------------------------------|----------------------------------------------------------|
| segmentation de l' \_ appareil de rendu VMR \_ \_ | VMR s’affiche sur la surface de recouvrement (VMR-7 uniquement). |
| VIDMEM de l' \_ appareil de rendu VMR \_ \_  | VMR s’affichera dans la mémoire vidéo.                     |
| SYSMEM de l' \_ appareil de rendu VMR \_ \_  | VMR s’affichera dans la mémoire système (VMR-7 uniquement).       |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cet événement est envoyé par VMR-7 et VMR-9 et est transféré aux applications. Notez que VMR-9 ne prend en charge que les cibles de rendu de mémoire vidéo.

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

 

 




