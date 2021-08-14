---
description: URI qui représente l’identificateur de service.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Élément ServiceID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dc6ac1da57109f4f5671caf16a49b3a6174e7bfb63335d5ba15a548d7135990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756739"
---
# <a name="serviceid-element"></a>Élément ServiceID

URI qui représente l’identificateur de service.

## <a name="usage"></a>Usage

``` syntax
<ServiceID/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                             | Description                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HBA**](host.md)<br/>     | Définit les éléments **ServiceId** et [**types**](types.md) pour l’hôte de service. S’il n’est pas fourni explicitement, WSDAPI ne fournit pas de données par défaut en réponse aux demandes de métadonnées.<br/> <br/>                                                                                                                     |
| [**Hébergement**](hosted.md)<br/> | Définit les éléments **ServiceId** et [**types**](types.md) pour les services fournis par cet hôte de service. Chaque service fourni par cet hôte de service doit disposer de ses propres informations d’élément [**hébergé**](hosted.md) pour s’assurer que le service est correctement publié dans les réponses aux demandes de métadonnées.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




