---
title: Délégués
description: L’API de diffusion multimédia en continu fournit les fonctions de gestionnaire d’événements suivantes.
ms.assetid: CDE7B829-D0D1-479D-9B35-4445E711AF58
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23fbf0f44a0822fd0c8914833b0696fcb9aacad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507885"
---
# <a name="delegates"></a>Délégués

L' [API de diffusion multimédia en continu](media-streaming-api-portal.md) fournit les fonctions de gestionnaire d’événements suivantes.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                   | Description                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))<br/>                   | Représente la fonction qui gérera l’événement [**ConnectionStatusChanged**](connectionstatuschanged.md) qui avertit le client des modifications de l’état de la connexion réseau de l’appareil.<br/>               |
| [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))<br/>       | Représente la fonction qui gérera les événements [**DeviceArrival**](devicearrival.md) et [**DeviceDeparture**](devicedeparture.md) qui informent le client des modifications apportées à la liste des appareils mis en cache.<br/> |
| [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))<br/> | Représente la fonction qui gérera l’événement [**RenderingParametersUpdate**](renderingparametersupdate.md) , qui avertit le client d’une mise à jour de tous les paramètres de contrôle de rendu de la gestion des événements.<br/>  |
| [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))<br/> | Représente la fonction qui gérera l’événement [**TransportParametersUpdate**](transportparametersupdate.md) , qui notifie le client d’une mise à jour à l’un des paramètres de transport de la gestion des e/s.<br/>          |



 

 

