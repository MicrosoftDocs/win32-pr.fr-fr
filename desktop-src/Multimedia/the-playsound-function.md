---
title: La fonction PlaySound
description: La fonction PlaySound
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- audio multimédia, fonction PlaySound
- audio, PlaySound, fonction
- Wave audio, fonction PlaySound
- PlaySound, fonction, à propos de
- sndPlaySound fonction)
- Fonction PlaySound, comparée à la fonction sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5723b1937c974e6c622c1f2010e8d2129e787cdd
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369324"
---
# <a name="the-playsound-function"></a>La fonction PlaySound

Vous pouvez utiliser la fonction [**PlaySound**](/previous-versions//dd743680(v=vs.85)) pour lire du son de forme d’onde si le son s’ajuste à la mémoire disponible. (La fonction [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) offre un sous-ensemble des fonctionnalités de PlaySound. Pour optimiser la portabilité de votre application Win32, utilisez **PlaySound**, et non **sndPlaySound**.)

La fonction **PlaySound** vous permet de spécifier un son de l’une des trois façons suivantes :

-   En tant qu’alerte système, à l’aide de l’alias stocké dans le fichier WIN.INI ou le registre
-   En tant que nom de fichier
-   En tant qu’identificateur de ressource

La fonction [**PlaySound**](/previous-versions//dd743680(v=vs.85)) vous permet de lire un son dans une boucle continue, en se terminant uniquement quand vous appelez **PlaySound** à nouveau, en spécifiant soit **null** , soit l’identificateur de son d’un autre son pour le paramètre *pszSound* .

Vous pouvez utiliser **PlaySound** pour lire le son de façon synchrone ou asynchrone, et pour contrôler le comportement de la fonction d’une autre façon lorsqu’elle doit partager des ressources système.

Pour plus d’informations sur l’utilisation de PlaySound, consultez les rubriques suivantes :

-   [Utilisation de PlaySound pour lire des fichiers Waveform-Audio](using-playsound-to-play-waveform-audio-files.md)
-   [Utilisation de PlaySound pour boucler des sons](using-playsound-to-loop-sounds.md)
-   [Utilisation de PlaySound pour lire des sons système](using-playsound-to-play-system-sounds.md)

Pour obtenir plus d’exemples sur l’utilisation de **PlaySound** dans vos applications Win32, consultez [Playing Wave Resources](playing-wave-resources.md)(en anglais).

 

 