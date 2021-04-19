---
description: Définit les métadonnées d’hébergement pour l’appareil à implémenter. Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: élément hostMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: becd6bc3eab6b1aa1d95414c6348288e0d29dbd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524466"
---
# <a name="hostmetadata-element"></a>élément hostMetadata

Définit les métadonnées d’hébergement pour l’appareil à implémenter. Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).

## <a name="usage"></a>Utilisation

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                             | Description                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HBA**](host.md)<br/>     | Définit les éléments ServiceID et [**types**](types.md) pour l’hôte de service. S’il n’est pas fourni explicitement, WSDAPI ne fournit pas de données par défaut en réponse aux demandes de métadonnées.<br/> <br/>                                                                                                                                          |
| [**Hébergement**](hosted.md)<br/> | Définit les éléments [**ServiceId**](serviceid.md) et [**types**](types.md) pour les services fournis par cet hôte de service. Chaque service fourni par cet hôte de service doit disposer de ses propres informations d’élément [**hébergé**](hosted.md) pour s’assurer que le service est correctement publié dans les réponses aux demandes de métadonnées.<br/> <br/> |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                                                         | Description                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**relationshipMetadata**](relationshipmetadata.md)<br/> | Décrit l’hôte et les métadonnées hébergées pour l’appareil.<br/> <br/> |



## <a name="remarks"></a>Notes

Les métadonnées d’hébergement apparaissent dans cet élément sous une forme similaire à celle spécifiée dans le profil d’appareil. **hostMetadata** est légèrement différent du format décrit dans le profil de l’appareil, car la seule propriété de référence qu’il prend en charge est l’ID du service.

L’élément [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) est utilisé par la suite pour générer une constante C contenant ces informations.

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Non            |



 

 




