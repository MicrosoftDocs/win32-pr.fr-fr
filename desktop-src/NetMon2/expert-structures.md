---
description: Les fonctions d’assistance d’experts fournies par Moniteur réseau et les fonctions d’assistance courantes utilisent les structures décrites dans le tableau suivant.
ms.assetid: 3c49dd0a-836f-43f1-b383-357e8ba6545f
title: Structures d’experts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16accf769b0983b782a6e6dbd723dd08df27415220bda1d59122b951439bac65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939016"
---
# <a name="expert-structures"></a>Structures d’experts

Les fonctions d’assistance d’experts fournies par Moniteur réseau et les fonctions d’assistance courantes utilisent les structures décrites dans le tableau suivant.



| Structure                                              | Description                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**CONFIGUREDEXPERT**](configuredexpert.md)           | Associe une DLL d’expert à sa configuration.                                                       |
| [**EXPERTCONFIG**](expertconfig.md)                   | Fournit des données de configuration brutes.                                                                       |
| [**EXPERTENUMINFO**](expertenuminfo.md)               | Fournit des informations sur la DLL de l’expert. Moniteur réseau utilise les informations.                       |
| [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) | Fournit des informations sur un frame.                                                                    |
| [**EXPERTSTARTUPINFO**](expertstartupinfo.md)         | Fournit des informations de démarrage sur l’expert.                                                         |
| [**EXPERTSTATUS**](expertstatus.md)                   | Indique l’état actuel d’un expert en cours d’exécution.                                                       |
| [**FILTEROBJECT**](filterobject.md)                   | Définit les caractéristiques de filtre d’affichage pour un expert.                                              |
| [**NMEVENTDATA**](nmeventdata.md)                     | Fournit des informations sur une ligne affichée dans la visionneuse d’experts.                                      |
| [**NMCOLUMNINFO**](nmcolumninfo.md)                   | Fournit des informations qui définissent une colonne dans le observateur d’événements.                                        |
| [**NMCOLUMNVARIANT**](nmcolumnvariant.md)             | Fournit un conteneur pour toutes les données possibles insérées dans une colonne sur une ligne dans le observateur d’événements.     |
| [**NMCOLUMNTYPE**](nmcolumntype.md)                   | Point d’entrée dans la variante qui indique l’élément de l’Union à utiliser et comment le mettre en forme. |



 

Moniteur réseau fournit également des fonctions d’exportation (fonctions d’assistance que l’expert peut appeler) et des énumérations.



| Pour obtenir des informations sur                                          | Consultez                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------|
| Exportez les fonctions qui fournissent des points d’entrée à votre DLL d’expert. | [Fonctions d’exportation de DLL d’experts](expert-dll-export-functions.md)               |
| Fonctions d’assistance qui peuvent être appelées par des experts et des analyseurs.    | [Fonctions courantes des experts et de l’analyseur](expert-and-parser-common-functions.md) |
| Fonctions d’assistance appelées uniquement par des experts.              | [Fonctions d’experts](expert-functions.md)                                     |
| Énumérations utilisées par les structures et fonctions d’experts.          | [Énumérations d’experts](expert-enumerations.md)                               |



 

 

 



