---
description: Illustre la clé de Registre qui doit être définie pour empêcher l’exécution automatique.
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: Comment empêcher l’exécution automatique d’un composant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b44817f6803c25bbf506a5f76c8b068c683af4b5d4c7536482c30cd3aee2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859686"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a>Comment empêcher l’exécution automatique d’un composant

Illustre la clé de Registre qui doit être définie pour empêcher l’exécution automatique.

## <a name="instructions"></a>Instructions


Pour empêcher le lancement de l’exécution automatique en réponse à un événement, ajoutez la valeur **reg \_ SZ** suivante, comme illustré dans cet exemple.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     CancelAutoplay
                        CLSID
                           00000000-0000-0000-0000-000000000000
```

La valeur correspond à l’identificateur de classe (CLSID) que le composant qui génère l’événement est connu dans la table ROT (Running Object Table). La valeur n’a pas de données.

> [!IMPORTANT]
> Sous cette clé, les CLSID ne sont pas mis entre accolades ( {} ).

 

 

 



