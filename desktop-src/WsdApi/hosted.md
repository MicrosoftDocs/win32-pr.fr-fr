---
description: Définit les éléments ServiceID, types, PnPXHardwareId et PnPXCompatibleId pour les services définis par l’hôte de service.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: élément hébergé
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46549898f0a95de362467c759c3d95eb806a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536592"
---
# <a name="hosted-element"></a>élément hébergé

Définit les éléments [**ServiceId**](serviceid.md), [**types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md)et [**PnPXCompatibleId**](pnpxcompatibleid.md) pour les services définis par l’hôte de service.

## <a name="usage"></a>Utilisation

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                 | Description                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [**PnPXCompatibleId**](pnpxcompatibleid.md)<br/> | Spécifie l’identificateur compatible PnP-X du service.<br/> <br/> |
| [**PnPXHardwareId**](pnpxhardwareid.md)<br/>     | Spécifie l’identificateur matériel PnP-X du service.<br/> <br/>   |
| [**ServiceID**](serviceid.md)<br/>               | Définit un identificateur de service pour l’hôte de service.<br/> <br/>        |
| [**Types**](types.md)<br/>                       | Définit une liste de noms qualifiés XSD.<br/> <br/>                    |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                                         | Description                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [**hostMetadata**](hostmetadata.md)<br/> | Métadonnées d’hébergement pour l’appareil à implémenter.<br/> <br/> |



## <a name="remarks"></a>Notes

Chaque service fourni par un hôte de service doit disposer de ses propres informations d’élément **hébergé** pour s’assurer que le service est correctement publié dans les réponses aux demandes de métadonnées.

Les éléments [**PnPXHardwareId**](pnpxhardwareid.md) et [**PnPXCompatibleId**](pnpxcompatibleid.md) sont facultatifs, mais lorsqu’ils sont utilisés, ils doivent être utilisés ensemble. S’il en existe un, l’autre doit également être présent.

Si un élément [**PnPXDeviceCategory**](pnpxdevicecategory.md) est présent, au moins un élément **hébergé** doit contenir à la fois des éléments [**PnPXHardwareId**](pnpxhardwareid.md) et [**PnPXCompatibleId**](pnpxcompatibleid.md) . De même, si des éléments **PnPXHardwareId** et **PnPXCompatibleId** sont présents dans un élément **hébergé** , au moins un élément **PnPXDeviceCategory** doit être présent dans l’élément [**thisModelMetadata**](thismodelmetadata.md) .

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Non            |



 

 




