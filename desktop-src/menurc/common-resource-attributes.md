---
title: Attributs de ressources communes
description: Les instructions de définition de ressources prises en charge sur Windows 16 bits incluent une option de chargement qui spécifie les caractéristiques de chargement et de mémoire de la ressource.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa15ae7207c80737e284151f0dfd3d7981935943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512452"
---
# <a name="common-resource-attributes"></a>Attributs de ressources communes

Les instructions de définition de ressources prises en charge sur Windows 16 bits incluent une option de *chargement* qui spécifie les caractéristiques de chargement et de mémoire de la ressource. Ces attributs sont autorisés dans les scripts de ressources à des fins de compatibilité descendante, mais ils sont ignorés. Les ressources Windows sont chargées lorsque le module correspondant est chargé, et sont libérées quand le module est déchargé.

## <a name="load-attributes"></a>Charger les attributs

Les attributs de chargement spécifient le moment où la ressource doit être chargée. Le paramètre de charge doit être l’un des attributs suivants.



| Attribut      | Description                                                                  |
|----------------|------------------------------------------------------------------------------|
| **PRÉ**    | Ignoré. Dans Windows 16 bits, la ressource est chargée avec le fichier exécutable. |
| **LOADONCALL** | Ignoré. Dans Windows 16 bits, la ressource est chargée quand elle est appelée.              |



 

## <a name="memory-attributes"></a>Attributs de mémoire

Les attributs de mémoire spécifient si la ressource est fixe ou mobile, si elle peut être supprimée et si elle est pure. Le paramètre de mémoire peut être un ou plusieurs des attributs suivants.



| Attribut       | Description                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **FIXED**       | Ignoré. Dans Windows 16 bits, la ressource reste à un emplacement de mémoire fixe.                                                              |
| **PLACÉ**    | Ignoré. Dans Windows 16 bits, la ressource peut être déplacée si nécessaire pour compacter la mémoire.                                                     |
| **POUVANT être éliminée** | Ignoré. Dans Windows 16 bits, la ressource peut être ignorée si vous n’en avez plus besoin.                                                            |
| **FCP**        | Ignoré. Accepté pour la compatibilité avec les scripts de ressources existants.                                                                       |
| **IMPURES**      | Ignoré. Accepté pour la compatibilité avec les scripts de ressources existants.                                                                       |
| **PARTAGÉ**      | Ignoré. Dans Windows 16 bits, SHAREd est ignoré pour les modules normaux. Pour une ressource d’un module ROM Windows, la mémoire est partagée.        |
| **NON partagée**   | Ignoré. Dans Windows 16 bits, non partagé est ignoré pour les modules normaux. Pour une ressource d’un module ROM Windows, la mémoire n’est pas partagée. |



 

 

 




