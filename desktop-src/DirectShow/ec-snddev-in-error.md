---
description: Une erreur d’appareil s’est produite dans un filtre de capture audio.
ms.assetid: 13f8641b-7881-4f1c-816c-77c140e48ed4
title: EC_SNDDEV_IN_ERROR (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f9b95055483b1bda812179f1a1bf132d12de7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111077"
---
# <a name="ec_snddev_in_error"></a>EC \_ SNDDEV \_ en \_ erreur

Une erreur d’appareil s’est produite dans un filtre de capture audio.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valeur DWORD du type énuméré [**SNDDEV \_ Err**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) , indiquant comment l’appareil a fait l’objet d’un accès lorsque la défaillance s’est produite.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valeur DWORD indiquant l’erreur renvoyée par l’appel de périphérique audio.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Aucun.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> <dt>

[Notification d’événements dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




