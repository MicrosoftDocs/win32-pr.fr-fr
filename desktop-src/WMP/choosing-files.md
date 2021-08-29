---
title: Choix des fichiers
description: Choix des fichiers
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- création d’apparences, sélection de fichiers
- Lecteur Windows Media des apparences, choix des fichiers
- apparences, choix des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed90a5813880c87dbaf297808cc79c65ed066eb1585ba63ddd97d0305199230
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764249"
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

 

 




