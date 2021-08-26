---
description: Il est possible de développer une application qui effectue des opérations qui requièrent des privilèges d’administrateur, mais qui s’exécute en tant qu’utilisateur standard.
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: Développement d’applications nécessitant des privilèges d’administrateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410dc8ea112cfec6297cf7c11a044e62695a24e93d7eb0b13a773d40acd6c6cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994429"
---
# <a name="developing-applications-that-require-administrator-privilege"></a>Développement d’applications nécessitant des privilèges d’administrateur

Il est possible de développer une application qui effectue des opérations qui requièrent des privilèges d’administrateur, mais qui s’exécute en tant qu’utilisateur standard.

Pour ce faire, il existe plusieurs modèles.



| Rubrique                                                                | Description                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Modèle de tâche avec élévation de privilèges](elevated-task-model.md)                       | Une application s’exécutant en tant qu’utilisateur standard effectue des opérations qui requièrent des privilèges d’administrateur en démarrant une tâche planifiée.                                                                     |
| [Modèle de service du système d’exploitation](operating-system-service-model.md) | Une application s’exécutant en tant qu’utilisateur standard communique avec un service exécuté en tant que **système** à l’aide d’un [appel de procédure distante](/windows/desktop/Rpc/rpc-start-page) (RPC).                                              |
| [Modèle de Broker administrateur](administrator-broker-model.md)         | L’application est divisée en deux programmes. L’un des programmes s’exécute en tant qu’utilisateur standard et l’autre s’exécute avec des privilèges d’administrateur.                                                          |
| [Modèle d’objet COM administrateur](administrator-com-object-model.md) | Une application s’exécutant en tant qu’utilisateur standard effectue des opérations qui requièrent des privilèges d’administrateur en créant un objet de [modèle d’objet de composant](/windows/desktop/com/component-object-model--com--portal) avec élévation de privilèges. |



 

 

 
