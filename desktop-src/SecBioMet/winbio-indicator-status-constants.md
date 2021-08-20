---
title: Constantes WINBIO_INDICATOR_STATUS ( \_ types WINBIO. h)
description: Définissez un témoin lumineux.
ms.assetid: 1e00ff9d-6693-4763-8ac3-b42d2a3e987d
topic_type:
- apiref
api_name:
- WINBIO_INDICATOR_ON
- WINBIO_INDICATOR_OFF
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fd05d279bd11eafda89eed436c94d6141e97ad0eb9d2fc426d5c89000f36414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910012"
---
# <a name="winbio_indicator_status-constants"></a>\_Constantes d’état de l’indicateur WINBIO \_

Les valeurs suivantes peuvent être utilisées pour définir un témoin lumineux. Par défaut, les capteurs ne sont pas allumés, mais les applications peuvent utiliser ces valeurs pour activer ou désactiver les indicateurs d’indicateur. La valeur d' **\_ \_ État du capteur WINBIO** fournit plus de détails sur l’état d’un voyant lumineux. Pour plus d’informations, consultez les fonctions suivantes :

-   [**SensorAdapterSetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)
-   [**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)
-   [**SensorAdapterQueryStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)



| Constante                                                                                                                                                                            | Description                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="WINBIO_INDICATOR_ON"></span><span id="winbio_indicator_on"></span><dl> <dt>**\_indicateur WINBIO \_ activé**</dt> </dl>    | La lumière de l’indicateur de capteur est allumée.<br/>  |
| <span id="WINBIO_INDICATOR_OFF"></span><span id="winbio_indicator_off"></span><dl> <dt>**\_indicateur WINBIO \_ désactivé**</dt> </dl> | La lumière de l’indicateur de capteur est désactivée.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> </dl>

 

 





