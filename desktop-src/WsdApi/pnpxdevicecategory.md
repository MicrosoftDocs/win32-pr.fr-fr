---
description: Spécifie la catégorie PnP-X à laquelle l’appareil appartient. Plusieurs catégories peuvent être spécifiées.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Élément PnPXDeviceCategory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42a34a3f63333a2d33266991c0e028e7d42a7244c962617974c9cc15e290d03c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897359"
---
# <a name="pnpxdevicecategory-element"></a>Élément PnPXDeviceCategory

Spécifie la catégorie PnP-X à laquelle l’appareil appartient. Plusieurs catégories peuvent être spécifiées.

## <a name="usage"></a>Usage

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



## <a name="remarks"></a>Remarques

Les appareils peuvent également spécifier une sous-catégorie d’appareil pour une catégorie d’appareil plus descriptive. par exemple, « phones. WindowsMobile cameras. DigitalStillCamera MediaDevices. MusicPlayer » identifie un appareil qui est un appareil Microsoft Windows Mobile avec un appareil photo et un lecteur de musique. La catégorie d’appareil principale de cet appareil est « téléphone ».

Pour spécifier plusieurs catégories d’appareils, séparez-les par un espace. par exemple, « printers Stockage » identifie un appareil avec la catégorie principale « printers » et une catégorie secondaire « Stockage ».

Si un élément **PnPXDeviceCategory** est présent, au moins un élément [**hébergé**](hosted.md) doit contenir à la fois des éléments [**PnPXHardwareId**](pnpxhardwareid.md) et [**PnPXCompatibleId**](pnpxcompatibleid.md) . De même, si des éléments **PnPXHardwareId** et **PnPXCompatibleId** sont présents dans un élément **hébergé** , au moins un élément **PnPXDeviceCategory** doit être présent dans l’élément [**thisModelMetadata**](thismodelmetadata.md) .

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




