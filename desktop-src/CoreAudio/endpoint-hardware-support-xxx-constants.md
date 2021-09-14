---
description: Les \_ \_ \_ constantes support matériel de point de terminaison xxx sont des indicateurs de support matériel pour un périphérique de point de terminaison audio.
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: Constantes ENDPOINT_HARDWARE_SUPPORT_XXX (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffb5b2255330b205519ce3065ccb5f7eebb6b65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114958"
---
# <a name="endpoint_hardware_support_xxx-constants"></a>SUPPORT matériel de point de terminaison \_ \_ xxx, \_ constantes

Les \_ \_ \_ constantes support matériel de point de terminaison xxx sont des indicateurs de support matériel pour un périphérique de point de terminaison audio.



| Constante/valeur                                                                                                                                                                                                                                                                           | Description                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <dt>**Point de terminaison \_ \_ \_ Volume de support matériel**</dt> <dt>0x00000001</dt> </dl> | L’appareil de point de terminaison audio prend en charge un contrôle de volume matériel.<br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <dt>**Point de terminaison \_ \_Support matériel \_ muet**</dt> <dt>0x00000002</dt> </dl>       | L’appareil de point de terminaison audio prend en charge un contrôle matériel muet.<br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <dt>**Point de terminaison \_ MATÉRIEL \_ pris \_ en charge**</dt> par le compteur <dt>0x00000004</dt> </dl>    | L’appareil de point de terminaison audio prend en charge un indicateur de pic matériel.<br/>     |



## <a name="remarks"></a>Notes

Les méthodes [**IAudioEndpointVolume :: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) et [**IAudioMeterInformation :: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) utilisent les \_ constantes support matériel de point de terminaison \_ \_ xxx.

Un masque de support matériel indique les fonctions qu’un périphérique de point de terminaison audio implémente dans le matériel. Le masque peut avoir la valeur 0 ou la combinaison or au niveau du bit (or) d’une ou de plusieurs \_ \_ constantes support matériel de point de terminaison \_ . Si un bit qui correspond à une constante particulière support matériel de point de terminaison \_ \_ \_ est défini dans le masque, la signification est que la fonction représentée par cette constante est implémentée dans le matériel par l’appareil.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>MMDeviceAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes audio principales](core-audio-constants.md)
</dt> <dt>

[**IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 




