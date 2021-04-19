---
description: URI qui représente l’identificateur de service.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Élément ServiceID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e97250b0b33d276dced4b5d454aec9298387c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539728"
---
# <a name="serviceid-element"></a>Élément ServiceID

URI qui représente l’identificateur de service.

## <a name="usage"></a>Utilisation

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



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




