---
description: Si un expert échoue au moment de l’exécution, si vous utilisez Moniteur réseau Functions pour la gestion de la mémoire, Moniteur réseau libère la mémoire allouée.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Gestion de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4cc5b38f5525b7c0d19e115c83ed9f770c72215c6b64825a089ec389bfc09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555879"
---
# <a name="managing-memory"></a>Gestion de la mémoire

Si un expert échoue au moment de l’exécution, si vous utilisez Moniteur réseau Functions pour la gestion de la mémoire, Moniteur réseau libère la mémoire allouée. Toutefois, lorsque vous écrivez un expert, il peut être nécessaire d’acquérir des ressources système et des informations sur la structure des données. Par exemple, l’expert de la fusion de protocole Moniteur réseau acquiert un descripteur de fichier pour générer une nouvelle capture. Chaque expert doit créer son propre traitement **try/catch** afin que l’expert puisse libérer les ressources qu’il a acquises.

Lorsque la mémoire est allouée, utilisez les fonctions de mémoire existantes suivantes :

-   [**ExpertAllocMemory**](expertallocmemory.md)
-   [**ExpertReallocMemory**](expertreallocmemory.md)

 

 



