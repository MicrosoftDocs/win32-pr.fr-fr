---
title: Entrées de Registre pour le suivi de la progression de l’installation
description: Entrées de Registre pour le suivi de la progression de l’installation
ms.assetid: 898f9117-94fd-4230-9378-b8c6a4401a96
keywords:
- Lecteur Windows Media, suivi de la progression de l’installation
- Lecteur Windows Media, suivi de la progression de l’installation
- Lecteur Windows Media, suivi de la progression des installations
- Lecteur Windows Media, registre
- Registre, suivi de la progression de l’installation
- Registre, suivi de la progression de l’installation
- Registre, suivi de la progression des installations
- registre, paramètres pour Lecteur Windows Media
- suivi de la progression de l’installation
- installation du suivi de la progression
- suivi de la progression des installations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7febb9f25a04c5e4358e891f963ab6a8569cfd6facef7e4f2072807bd09e2605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570300"
---
# <a name="registry-entries-for-tracking-installation-progress"></a>Entrées de Registre pour le suivi de la progression de l’installation

le programme d’installation de Lecteur Windows Media 11,wm.exe de configuration \_ , écrit les entrées suivantes dans le registre afin que les programmes d’installation puissent suivre la progression du programme d’installation de Lecteur Windows Media lors de son exécution.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



Dans la syntaxe précédente du Registre, la *valeur* est un espace réservé pour une valeur entière.

Progress \_ CurrentDialog indique la boîte de dialogue Lecteur Windows Media installation actuellement affichée. Progress \_ MaxDialog indique le nombre total de boîtes de dialogue qui s’affichent Windows média. par exemple, si progress \_ CurrentDialog = 2 et progress \_ MaxDialog = 5, Lecteur Windows Media affiche actuellement la deuxième boîte de dialogue dans une séquence de cinq.

Progress \_ CurrentInstall et Progress \_ MaxInstall, pris ensemble, indiquent le pourcentage d’achèvement de la boîte de dialogue active. Par exemple, si Progress \_ CurrentInstall = 6 et Progress \_ MaxInstall = 25, la boîte de dialogue actuelle est 6/25 (c’est-à-dire 24%) terminé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres du Registre**](registry-settings.md)
</dt> </dl>

 

 




