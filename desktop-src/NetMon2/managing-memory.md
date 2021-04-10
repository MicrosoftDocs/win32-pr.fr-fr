---
description: Si un expert échoue au moment de l’exécution, si vous utilisez Moniteur réseau Functions pour la gestion de la mémoire, Moniteur réseau libère la mémoire allouée.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Gestion de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e2a6cca89a095c03c5c0cad25642b87d2c252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951269"
---
# <a name="managing-memory"></a>Gestion de la mémoire

Si un expert échoue au moment de l’exécution, si vous utilisez Moniteur réseau Functions pour la gestion de la mémoire, Moniteur réseau libère la mémoire allouée. Toutefois, lorsque vous écrivez un expert, il peut être nécessaire d’acquérir des ressources système et des informations sur la structure des données. Par exemple, l’expert de la fusion de protocole Moniteur réseau acquiert un descripteur de fichier pour générer une nouvelle capture. Chaque expert doit créer son propre traitement **try/catch** afin que l’expert puisse libérer les ressources qu’il a acquises.

Lorsque la mémoire est allouée, utilisez les fonctions de mémoire existantes suivantes :

-   [**ExpertAllocMemory**](expertallocmemory.md)
-   [**ExpertReallocMemory**](expertreallocmemory.md)

 

 



