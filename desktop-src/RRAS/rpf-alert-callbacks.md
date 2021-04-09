---
title: Rappels d’alerte RPF
description: Une fois que le gestionnaire de groupe de multidiffusion a reçu la notification d’un paquet provenant d’une nouvelle source ou d’un paquet destiné à un nouveau groupe, le gestionnaire de groupe de multidiffusion recherche l’itinéraire vers la source dans la vue multidiffusion de la table de routage.
ms.assetid: dacccca2-e6a5-417a-a217-06ff846d55f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7832a25f8b44821f4b46a69943b4bba3519207c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675977"
---
# <a name="rpf-alert-callbacks"></a>Rappels d’alerte RPF

Une fois que le gestionnaire de groupe de multidiffusion a reçu la notification d’un paquet provenant d’une nouvelle source ou d’un paquet destiné à un nouveau groupe, le gestionnaire de groupe de multidiffusion recherche l’itinéraire vers la source dans la vue multidiffusion de la table de routage. Le gestionnaire de groupe de multidiffusion appelle ensuite le rappel de [**\_ \_ rappel PMGM RPF**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) au protocole propriétaire de l’interface sur laquelle les données sont arrivées.

Une fois ce rappel appelé, le protocole de routage peut modifier l’interface entrante si le protocole de routage doit recevoir les données du groupe sur une autre interface.

 

 




