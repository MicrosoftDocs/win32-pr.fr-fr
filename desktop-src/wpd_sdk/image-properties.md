---
description: Windows Appareils mobiles prend en charge les propriétés d’image suivantes.
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: Propriétés de l’image (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 0d2ebe552a66dadf6b9bec6a0a741d85e1c7f1f018ef108e36ec1bb3cb4b6165
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430758"
---
# <a name="image-properties"></a>Propriétés de l’image

Windows Appareils mobiles prend en charge les propriétés d’image suivantes.



| Property                                                                                                                                       | VarType     | Description                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_image wpd \_ BITDEPTH**                                                                                                                       | **VT \_ UI4** | Profondeur de bit de l’image.                                                                                                                                                                                                                                                                                                                     |
| <span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**État de couleur de l' \_ image wpd \_ \_ corrigé \_** | **VT \_ UI4** | Énumération de [**\_ \_ \_ \_ valeurs d’État corrigées pour la couleur wpd**](wpd-color-corrected-status-values.md) qui spécifie si le fichier a été corrigé par des couleurs. Cela empêche plusieurs appareils de corriger automatiquement les couleurs de l’image pendant le traitement.<br/>                                                                       |
| **\_ \_ État rogné de l’image wpd \_**                                                                                                                | **VT \_ UI4** | Énumération des valeurs d’état d’un fichier [**wpd \_ rogné \_ \_**](wpd-cropped-status-values.md) qui spécifie si le fichier a été rogné. Cela empêche plusieurs appareils de rogner automatiquement l’image pendant le traitement.<br/>                                                                                                        |
| **\_index d' \_ exposition d’image wpd \_**                                                                                                                | **VT \_ UI4** | Valeur qui identifie les paramètres de vitesse du film lorsque cette image a été capturée. Les paramètres correspondent aux désignations ISO de ASA/DIN.<br/> En règle générale, un appareil prend en charge des valeurs énumérées discrètes, mais le contrôle continu sur une plage est possible.<br/> La valeur 0xFFFFFFFF correspond au paramètre ISO automatique.<br/> |
| **temps d’exposition de l' \_ image wpd \_ \_**                                                                                                                 | **VT \_ UI4** | Identifie la vitesse d’obturation de l’appareil lorsque cette image a été capturée. Les unités sont en secondes mises à l’échelle par 10000.<br/>                                                                                                                                                                                                                        |
| **\_image wpd \_ FNUMBER**                                                                                                                        | **VT \_ UI4** | Identifie le paramètre d’ouverture de la lentille lorsque cette image a été capturée. Les unités sont égales au nombre f mis à l’échelle par 100.<br/>                                                                                                                                                                                                              |
| **\_ \_ résolution horizontale de l’image wpd \_**                                                                                                         | **VT \_ R8**  | Indique la résolution horizontale d’une image, en points par pouce (DPI).                                                                                                                                                                                                                                                                       |
| **\_ \_ résolution verticale de l’image wpd \_**                                                                                                           | **VT \_ R8**  | Indique la résolution verticale d’une image, en points par pouce (DPI).                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




