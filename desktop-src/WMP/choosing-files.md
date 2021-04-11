---
title: Choix des fichiers
description: Choix des fichiers
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- création d’apparences, sélection de fichiers
- Apparences du lecteur Windows Media, choix des fichiers
- apparences, choix des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0098a37635c52ba3e48fb77f07a5868ceb957239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197220"
---
# <a name="choosing-files"></a>Choix des fichiers

Si vous souhaitez choisir un fichier, vous pouvez utiliser du code similaire à l’exemple de sélection, mais substituez ce qui suit à la section PLAYELEMENT :


```C++
<PLAYELEMENT
  mappingColor = "#00FF00"
  onClick = "JScript:player.URL=theme.openDialog('FILE_OPEN','FILES_ALL');"
  />

```



Cette ligne utilise la méthode **openDialog** de **thème** pour définir une **URL** pour le lecteur. Vous pouvez l’utiliser pour choisir des fichiers qui ne se trouvent pas dans les sélections.

Vous pouvez voir un exemple de **openDialog** de travail similaire dans la section exemple du kit de développement logiciel (SDK).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de création d’apparence**](skin-creation-guide.md)
</dt> </dl>

 

 




