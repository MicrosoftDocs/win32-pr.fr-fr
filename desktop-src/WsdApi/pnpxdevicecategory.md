---
description: Spécifie la catégorie PnP-X à laquelle l’appareil appartient. Plusieurs catégories peuvent être spécifiées.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Élément PnPXDeviceCategory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731dd78fbe366fc9c7923686d3d9ac90b772c23d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524248"
---
# <a name="pnpxdevicecategory-element"></a>Élément PnPXDeviceCategory

Spécifie la catégorie PnP-X à laquelle l’appareil appartient. Plusieurs catégories peuvent être spécifiées.

## <a name="usage"></a>Utilisation

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                   | Description                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**thisModelMetadata**](thismodelmetadata.md)<br/> | Définit les métadonnées du fabricant et du modèle pour l’appareil à implémenter.<br/> <br/> |



## <a name="remarks"></a>Notes

Les appareils peuvent également spécifier une sous-catégorie d’appareil pour une catégorie d’appareil plus descriptive. Par exemple, « phones. WindowsMobile cameras. DigitalStillCamera MediaDevices. MusicPlayer » identifie un appareil qui est un appareil Microsoft Windows Mobile avec un appareil photo et un lecteur de musique. La catégorie d’appareil principale de cet appareil est « téléphone ».

Pour spécifier plusieurs catégories d’appareils, séparez-les par un espace. Par exemple, « imprimantes Storage » identifie un appareil avec la catégorie principale « Printers » et une catégorie secondaire de « Storage ».

Si un élément **PnPXDeviceCategory** est présent, au moins un élément [**hébergé**](hosted.md) doit contenir à la fois des éléments [**PnPXHardwareId**](pnpxhardwareid.md) et [**PnPXCompatibleId**](pnpxcompatibleid.md) . De même, si des éléments **PnPXHardwareId** et **PnPXCompatibleId** sont présents dans un élément **hébergé** , au moins un élément **PnPXDeviceCategory** doit être présent dans l’élément [**thisModelMetadata**](thismodelmetadata.md) .

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




