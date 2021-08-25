---
description: Les fonctions suivantes sont les points d’entrée pour les dll d’experts et les appels du système d’exploitation et Moniteur réseau.
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: Fonctions d’exportation de DLL d’experts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327b36990ac377595b31b55ebc0ed57157fd8d411f690aff3378293f35e39e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911129"
---
# <a name="expert-dll-export-functions"></a>Fonctions d’exportation de DLL d’experts

Les fonctions suivantes sont les points d’entrée pour les dll d’experts et les appels du système d’exploitation et Moniteur réseau.



| Fonction                                   | Description                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Expert DllMain**](dllmain-expert.md)   | Indique que la DLL d’expert a été chargée ou déchargée. Lorsqu’un processus charge ou décharge la DLL, le système d’exploitation appelle la fonction [**DllMain**](/windows/desktop/Dlls/dllmain) . |
| [**Inscrire un expert**](register-expert.md) | Détermine les informations de base sur l’expert au sein de la DLL. Moniteur réseau appelle la fonction **Register** .                                                           |
| [**Configurer**](configure.md)             | Configure l’expert dans la DLL. Moniteur réseau appelle la fonction de [**configuration**](configure.md) .                                                                 |
| [**Exécuter**](run.md)                         | Démarre l’expert dans la DLL. Moniteur réseau appelle la fonction [**Run**](run.md) .                                                                                 |



 

Moniteur réseau fournit également des structures, des énumérations et des fonctions d’assistance que l’expert peut appeler.



| Pour obtenir des informations sur                                      | Consultez                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| Fonctions d’assistance qui peuvent être appelées par des experts et des analyseurs | [Fonctions courantes des experts et de l’analyseur](expert-and-parser-common-functions.md) |
| Fonctions d’assistance appelées uniquement par des experts           | [Fonctions d’experts](expert-functions.md)                                     |
| Structures utilisées par les fonctions d’experts               | [Structures d’experts](expert-structures.md)                                   |
| Énumérations utilisées par les structures et fonctions d’experts       | [Énumérations d’experts](expert-enumerations.md)                               |



 

 

 
