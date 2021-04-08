---
title: Types de données simples de la version 2 du gestionnaire de table de routage
description: L’API RTMv2 définit plusieurs types de données simples. Le tableau suivant répertorie ces types de données.
ms.assetid: e935518e-b8d8-47fb-b2b2-c9750c2b540e
keywords:
- Routage et accès à distance service RRAS, gestionnaire de table de routage version 2, types de données simples
- Gestionnaire de table de routage version 2 RRAS, types de données simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6dbd7530799c1c7e1702e0384d51b37a77dda0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674258"
---
# <a name="routing-table-manager-version-2-simple-data-types"></a>Types de données simples de la version 2 du gestionnaire de table de routage

L’API RTMv2 définit plusieurs types de données simples. Le tableau suivant répertorie ces types de données.



| Type de données                                                                                                                                                                                                                                                                                                                   | Description                                                                                                                                      | Typedef              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| \_ \_ ID de vue RTM \* , \_ ID de vue PRTM \_                                                                                                                                                                                                                                                                                             | Identifie une vue particulière.                                                                                                                    | INT                  |
| \_ \_ jeu de vues RTM DWORD \* , \_ ensemble de vues PRTM \_                                                                                                                                                                                                                                                                                     | Identifie un ensemble de vues ; exprimée sous la forme d’un masque.                                                                                                  | DWORD                |
| descripteur d’entité RTM, descripteur d' \_ \_ \* entité PRTM, handle de \_ \_ \_ dest RTM \_ , \* \_ \_ DEscripteur de dest PRTM, \_ \_ \* \_ \_ \_ \_ \* \_ \_ \_ \_ \* \_ \_ \_ \_ \_ \* \_ \_ \_ \_ \_ \* \_ \_ handle d’itinéraire RTM, descripteur d’itinéraire PRTM, descripteur de routage RTM, PRTM handle nexthop, handle d’énumération RTM, descripteur d’énumération RTM, descripteur de liste de routes RTM, descripteur de liste d’itinéraires | Handles pointant vers des données RTMv2.                                                                                                                  | HANDLE               |
| \_ \_ type de méthode d’entité RTM \_ , \* type de méthode d' \_ entité PRTM \_ \_                                                                                                                                                                                                                                                                     | Identifie les méthodes exportées par un client inscrit.                                                                                              | DWORD                |
| \_méthode d’exportation d’entité RTM \_ \_ , méthode d' \* \_ exportation d’entité PRTM \_ \_                                                                                                                                                                                                                                                                 | Spécifie le prototype commun pour les méthodes clientes.                                                                                               | \_méthode d’entité \_     |
| \_ \_ indicateurs de modification de l’itinéraire RTM \_ , indicateurs de modification de l' \* \_ itinéraire PRTM \_ \_                                                                                                                                                                                                                                                                     | Indicateurs d’entrée et de sortie utilisés pour spécifier l’état lors de l’ajout ou de la mise à jour d’un itinéraire.                                                               | DWORD                |
| \_indicateurs de modification du tronçon RTM \_ \_ , \* \_ indicateurs de modification PRTM nexthop \_ \_                                                                                                                                                                                                                                                                 | Indicateurs de sortie utilisés pour spécifier l’état lors de l’ajout d’un tronçon suivant.                                                                                 | DWORD                |
| \_ \_ indicateurs de correspondance RTM \* , \_ indicateurs de correspondance PRTM \_                                                                                                                                                                                                                                                                                     | Indicateurs d’entrée utilisés pour spécifier des critères lors de la correspondance des itinéraires dans la table de routage.                                                                  | DWORD                |
| \_indicateurs enum RTM \_ , \* indicateurs d' \_ énumération PRTM \_                                                                                                                                                                                                                                                                                       | Identifie les énumérations.                                                                                                                         | DWORD                |
| \_ \_ indicateurs de notification RTM \* , \_ indicateurs de notification PRTM \_                                                                                                                                                                                                                                                                                   | Indicateurs de sortie utilisés pour spécifier le type de notification émis ; composé comme suit : (types de modification \| DestS) un client intéresse. | DWORD                |
| le \_ rappel d’événement RTM \_ , le rappel d' \* \_ événement PRTM \_ ;                                                                                                                                                                                                                                                                              | Identifie le rappel utilisé pour informer les clients qu’une modification s’est produite dans l’état de l’itinéraire ou les clients inscrits.                                  | \_rappel d’événement RTM \_ |



 

 

 




