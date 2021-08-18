---
title: Noms des appareils
description: Noms des appareils
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85183a1b23817352ba9e45e8dbb2aaa70493430cd092f357e1eaa8e9bf179d65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497269"
---
# <a name="device-names"></a>Noms des appareils

Pour chaque type d’appareil, il peut y avoir plusieurs pilotes MCI qui partagent le jeu de commandes, mais qui opèrent sur des formats de données différents. Pour identifier un pilote MCI de manière unique, MCI utilise des *noms d’appareils*.

Les noms des appareils sont identifiés dans \[ la \] section MCI du fichier SYSTEM.INI ou dans la partie appropriée du Registre. Ces informations identifient tous les pilotes MCI à Windows. Les entrées de la \[ \] section MCI utilisent la forme suivante :

*\_ nom du périphérique* nom  =  *\_ du pilote. extension*

L’exemple suivant montre une \[ section MCI classique \] de SYSTEM.INI :


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



Si un pilote MCI est installé à l’aide d’un nom d’appareil qui existe déjà dans SYSTEM.INI ou dans le registre, le système ajoute un entier au nom du périphérique du nouveau pilote, en créant un nom d’appareil unique. Dans l’exemple précédent, un pilote supplémentaire installé à l’aide du nom de l’appareil « cdaudio » se voit attribuer le nom de l’appareil « cdaudio1 ».

 

 




