---
description: COM+ introduit des cloisonnements neutres pour simplifier la programmation dans les environnements multithread. Le cloisonnement neutre est le modèle préféré pour COM+ pour les composants sans interface utilisateur.
ms.assetid: 679742af-7c04-4b0e-822a-a43e1aafa936
title: Cloisonnements neutres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beea8fbc3d007b26274d4a2b9d4cfd1ac0b604991ad9039b5053ccf534a5c6d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070429"
---
# <a name="neutral-apartments"></a>Cloisonnements neutres

COM+ introduit des cloisonnements neutres pour simplifier la programmation dans les environnements multithread. Le cloisonnement neutre est le modèle préféré pour COM+ pour les composants sans interface utilisateur.

Par le passé, pour éviter les goulots d’étranglement, les développeurs COM+ nécessitant une évolutivité du serveur devaient implémenter des composants à threads libres. Toutefois, les modèles de threads libres sont difficiles à implémenter, car ils doivent gérer l’accès au verrouillage. Dans les cloisonnements neutres, les objets suivent les instructions pour les cloisonnements multithread, mais peuvent s’exécuter sur n’importe quel type de thread. Quand un thread s’exécute dans un cloisonnement neutre, le contexte de l’objet est reçu sans provoquer de changement de thread.

Chaque processus ne peut avoir qu’un seul cloisonnement neutre. Pour sélectionner un cloisonnement neutre, utilisez le paramètre de Registre suivant :

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         ThreadingModel = Neutral
```

Les composants qui ont des interfaces utilisateur doivent continuer à utiliser des Apartments à thread unique comme modèle préféré. Pour sélectionner un cloisonnement à thread unique, utilisez le paramètre de Registre suivant :

**ThreadingModel** = cloisonnement

 

 



