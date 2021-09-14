---
description: Définit les éléments ServiceID et types pour l’hôte de service.
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: élément hôte
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9f051f6665715ecaa519a060e18a3cbf4912210
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010361"
---
# <a name="host-element"></a>élément hôte

Définit les éléments [**ServiceId**](serviceid.md) et [**types**](types.md) pour l’hôte de service.

## <a name="usage"></a>Usage

``` syntax
<host>
  child elements
</host>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                   | Description                                                                 |
|-------------------------------------------|-----------------------------------------------------------------------------|
| [**ServiceID**](serviceid.md)<br/> | Définit l’identificateur de service pour l’hôte de service.<br/> <br/> |
| [**Types**](types.md)<br/>         | Définit une liste de noms qualifiés XSD.<br/> <br/>               |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  ServiceID, 
  Types
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                                         | Description                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [**hostMetadata**](hostmetadata.md)<br/> | Métadonnées d’hébergement pour l’appareil à implémenter.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Non            |



 

 




