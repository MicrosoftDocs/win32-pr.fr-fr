---
title: À propos des fonctions et macros AVIFile
description: À propos des fonctions et macros AVIFile
ms.assetid: 877f6759-8271-47eb-8a7f-540393e5ae89
keywords:
- AVIFileInit fonction)
- AVIFileExit fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f66bbac900b69841fd7cba814aad339731b75727
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029822"
---
# <a name="about-avifile-functions-and-macros"></a>À propos des fonctions et macros AVIFile

Les fonctions et macros AVIFile gèrent les informations dans des fichiers basés sur le temps sous la forme d’un ou de plusieurs *flux de données* au lieu de blocs balisés de données appelés segments. Les flux de données font référence aux composants d’un fichier basé sur l’heure. Un fichier AVI peut contenir plusieurs types de données différents, tels qu’une séquence vidéo, une piste audio anglaise et une bande son française. À l’aide de AVIFile, une application peut accéder séparément à chacun de ces composants.

> [!Note]  
> Bien que les fonctions et macros AVIFile fonctionnent avec n’importe quel fichier RIFF, cette vue d’ensemble illustre leur utilisation avec les fichiers AVI uniquement. Les fichiers AVI sont généralement des fichiers basés sur le temps utilisés avec les macros et les fonctions AVIFile.

 

Les fonctions et les macros AVIFile sont contenues dans une bibliothèque de liens dynamiques. Pour initialiser la bibliothèque, utilisez la fonction [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) . Après l’initialisation de la bibliothèque, vous pouvez utiliser l’une des fonctions ou macros AVIFile. Pour libérer la bibliothèque, utilisez la fonction [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) . AVIFile conserve un décompte de références des applications qui utilisent la bibliothèque, mais pas celles qui l’ont publié. Vos applications doivent équilibrer chaque utilisation de **AVIFileInit** avec un appel à **AVIFileExit** pour libérer complètement la bibliothèque une fois que chaque application a terminé de l’utiliser.

 

 




