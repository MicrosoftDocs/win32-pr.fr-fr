---
title: Pour suspendre ou arrêter la lecture
description: Pour suspendre ou arrêter la lecture
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- ASF (Advanced Systems Format), suspension de la lecture
- ASF (format de systèmes avancés), suspension de la lecture
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), arrêt de la lecture
- ASF (format des systèmes avancés), arrêt de la lecture
- ASF (Advanced Systems Format), lecture suspendue ou arrêtée
- ASF (format avancé des systèmes), lecture en suspens ou en cours d’arrêt
- lecteurs asynchrones, suspension de la lecture
- lecteurs asynchrones, arrêt de la lecture
- lecteurs asynchrones, lecture suspendue ou arrêtée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728ce4c58f9198f605764d0f19d0d5f55c7f6c6b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507787"
---
# <a name="to-pause-or-stop-playback"></a>Pour suspendre ou arrêter la lecture

Quand vous appelez [**IWMReader :: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) pour commencer à lire un fichier, le lecteur asynchrone continue le traitement dans ses propres threads distincts jusqu’à ce que la fin du fichier soit atteinte. Vous pouvez suspendre ou arrêter la remise des exemples à l’aide des méthodes [**IWMReader ::P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) ou [**IWMReader :: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) , respectivement.

## <a name="pausing"></a>Suspension en cours

Quand vous appelez **IWMReader ::P ause** pour suspendre la lecture d’un fichier, le lecteur effectue le suivi de la position actuelle dans le fichier. Pour reprendre la diffusion après une pause, appelez [**IWMReader :: Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume). La lecture reprendra à partir du point où elle a été suspendue.

## <a name="stopping"></a>En cours d’arrêt

Quand vous appelez **IWMReader :: Stop** pour arrêter la lecture d’un fichier, le lecteur n’effectue pas le suivi des informations sur la progression de la lecture. Pour utiliser **Stop** , puis revenir au point d’arrêt, vous devez enregistrer l’heure de présentation du dernier exemple livré et l’utiliser dans votre appel à **IWMReader :: Start**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lecture des fichiers avec le lecteur asynchrone**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




