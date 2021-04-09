---
description: Définit les métadonnées du fabricant et du modèle pour l’appareil à implémenter. Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: élément thisModelMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a35d6449d4e8bba0ecf79e7dc87b00dee894b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867601"
---
# <a name="thismodelmetadata-element"></a>élément thisModelMetadata

Définit les métadonnées du fabricant et du modèle pour l’appareil à implémenter. Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).

## <a name="usage"></a>Utilisation

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                     | Description                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**fécule**](manufacturer.md)<br/>             | Nom du fabricant. Au moins un [**fabricant**](manufacturer.md) ou [**manufacturerLS**](manufacturerls.md) doit être présent dans les métadonnées.<br/> <br/> |
| [**manufacturerLS**](manufacturerls.md)<br/>         | Version localisée du nom du fabricant.<br/> <br/>                                                                                                                 |
| [**manufacturerURL**](manufacturerurl.md)<br/>       | Adresse URL du fabricant.<br/> <br/>                                                                                                                                   |
| [**modelName**](modelname.md)<br/>                   | Nom de l'unité. Au moins l’un des [**modelname**](modelname.md) ou [**modelNameLS**](modelnamels.md) doit être présent dans les métadonnées.<br/> <br/>                   |
| [**modelNameLS**](modelnamels.md)<br/>               | Version localisée du nom de l’appareil.<br/> <br/>                                                                                                                       |
| [**modelNumber**](modelnumber.md)<br/>               | Numéro de modèle de l’appareil.<br/> <br/>                                                                                                                                 |
| [**modelURL**](modelurl.md)<br/>                     | Adresse URL du modèle d’appareil.<br/> <br/>                                                                                                                           |
| [**PnPXDeviceCategory**](pnpxdevicecategory.md)<br/> | Catégorie PnP-X à laquelle appartient l’appareil. <br/> <br/>                                                                                                                |
| [**presentationURL**](presentationurl.md)<br/>       | Adresse URL des données de présentation du modèle d’appareil.<br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  manufacturer?, 
  manufacturerLS*, 
  manufacturerURL?, 
  modelName?, 
  modelNameLS*, 
  modelNumber, 
  modelURL?, 
  PnPXDeviceCategory?, 
  presentationURL?
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                                     | Description                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Élément racine d’un fichier de script XML du générateur de code WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Notes

Les métadonnées du fabricant correspondent à la section des métadonnées du fabricant décrite dans le profil de l’appareil (pour plus d’informations, consultez le profil de l’appareil). Le nom du fabricant ou au moins une version localisée du nom du fabricant doit être fourni. Le nom du modèle ou au moins une version localisée du nom du modèle doit être fourni.

L’élément [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) est ensuite utilisé pour générer une constante C contenant ces informations.

Si un élément [**PnPXDeviceCategory**](pnpxdevicecategory.md) est présent, au moins un élément [**hébergé**](hosted.md) doit contenir à la fois des éléments [**PnPXHardwareId**](pnpxhardwareid.md) et [**PnPXCompatibleId**](pnpxcompatibleid.md) . De même, si des éléments **PnPXHardwareId** et **PnPXCompatibleId** sont présents dans un élément **hébergé** , un élément **PnPXDeviceCategory** doit être présent dans l’élément **thisModelMetadata** .

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Non            |



 

 




