---
title: Utilisation de PlaySound pour lire des sons système
description: Utilisation de PlaySound pour lire des sons système
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- Wave audio, fonction PlaySound
- audio Wave, lecture des sons système
- sons Waveform, événements sonores
- PlaySound, fonction, jouer des sons système
- PlaySound, fonction, événements sonores
- lecture des sons du système Waveform-Audio
- événements sonores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9978e9e33c049db82a033b2379ac9f52b5e2959fd9d8425deac180ba7a81e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804569"
---
# <a name="using-playsound-to-play-system-sounds"></a>Utilisation de PlaySound pour lire des sons système

La fonction [**PlaySound**](/previous-versions//dd743680(v=vs.85)) lira également des sons référencés par un nom de clé dans le registre. Les utilisateurs peuvent assigner leurs propres sons à des alertes et des avertissements système, ou à des actions de l’utilisateur, comme un clic sur un bouton de la souris. Les sons associés aux alertes système et aux avertissements sont appelés des *événements sonores*.

Pour lire un événement sonore, appelez **PlaySound** avec le paramètre *pszSound* pointant vers une chaîne contenant le nom de l’entrée de Registre qui identifie le son. Par exemple, pour lire le son associé à l’entrée « MouseClick » et attendre la fin du son avant de retourner, utilisez l’instruction suivante :


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



Si l’entrée de Registre spécifiée ou le fichier Waveform-Audio qu’il identifie n’existe pas, ou si le fichier ne tient pas dans la mémoire disponible, **PlaySound** lit le son système par défaut.

Les événements sonores prédéfinis par le système peuvent varier en fonction de la plateforme. La liste suivante indique les événements sonores définis pour toutes les implémentations de l’API Win32 :

-   SystemAsterisk
-   SystemExclamation
-   SystemExit
-   SystemHand
-   SystemQuestion
-   SystemStart

Si une application enregistre ses propres événements de son, l’utilisateur peut configurer l’événement son à l’aide de l’interface standard du panneau de configuration. L’application doit enregistrer l’événement sonore à l’aide des fonctions de Registre standard. Pour plus d’informations, consultez [Registry](../sysinfo/registry.md). Les entrées appartiennent à la même position dans la hiérarchie du registre que le reste des événements sonores. Cette position varie en fonction de l’implémentation Win32. La valeur de données appropriée varie également en fonction de l’implémentation.

La fonction [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) recherche toujours dans le registre un KeyName correspondant à *lpszSound* avant de tenter de charger un fichier portant ce nom. La fonction [**PlaySound**](/previous-versions//dd743680(v=vs.85)) accepte les indicateurs qui spécifient l’emplacement du son.

 

 