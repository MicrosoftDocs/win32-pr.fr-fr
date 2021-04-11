---
title: Entrées de Registre pour le suivi de la progression de l’installation
description: Entrées de Registre pour le suivi de la progression de l’installation
ms.assetid: 898f9117-94fd-4230-9378-b8c6a4401a96
keywords:
- Windows Media Player, suivi de la progression de l’installation
- Windows Media Player, suivi de la progression de l’installation
- Lecteur Windows Media, suivi de la progression des installations
- Lecteur Windows Media, registre
- Registre, suivi de la progression de l’installation
- Registre, suivi de la progression de l’installation
- Registre, suivi de la progression des installations
- Registre, paramètres pour le lecteur Windows Media
- suivi de la progression de l’installation
- installation du suivi de la progression
- suivi de la progression des installations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3add1d2feb668ee90418704b9a11b0072530f120
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029842"
---
# <a name="registry-entries-for-tracking-installation-progress"></a>Entrées de Registre pour le suivi de la progression de l’installation

Le programme d’installation de Windows Media Player 11, Setup \_wm.exe, écrit les entrées suivantes dans le registre afin que les programmes d’installation puissent suivre la progression du programme d’installation du lecteur Windows Media lors de son exécution.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



Dans la syntaxe précédente du Registre, la *valeur* est un espace réservé pour une valeur entière.

Progress \_ CurrentDialog indique la boîte de dialogue que le programme d’installation du lecteur Windows Media affiche actuellement. Progress \_ MaxDialog indique le nombre total de boîtes de dialogue affichées par Windows Media. Par exemple, si Progress \_ CurrentDialog = 2 et Progress \_ MaxDialog = 5, le lecteur Windows Media affiche actuellement la deuxième boîte de dialogue dans une séquence de cinq.

Progress \_ CurrentInstall et Progress \_ MaxInstall, pris ensemble, indiquent le pourcentage d’achèvement de la boîte de dialogue active. Par exemple, si Progress \_ CurrentInstall = 6 et Progress \_ MaxInstall = 25, la boîte de dialogue actuelle est 6/25 (c’est-à-dire 24%) Remplissez.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres du Registre**](registry-settings.md)
</dt> </dl>

 

 




