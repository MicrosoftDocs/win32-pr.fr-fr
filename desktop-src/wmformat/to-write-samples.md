---
title: Pour écrire des exemples
description: Pour écrire des exemples
ms.assetid: 9ce10a77-9e80-45e0-a7e7-2ffdf8b57773
keywords:
- ASF (Advanced Systems Format), écriture d’exemples
- ASF (format avancé des systèmes), écrire des exemples
- ASF (Advanced Systems Format), passer des exemples à l’enregistreur
- ASF (format de systèmes avancés), passer des exemples à l’enregistreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738014b3c42441e878105d12a8ebf23ce4b266f7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381497"
---
# <a name="to-write-samples"></a>Pour écrire des exemples

Une fois que vous avez identifié et configuré les entrées pour le fichier que vous écrivez, vous pouvez commencer à passer des exemples au writer. Vous devez passer des exemples dans l’ordre de la présentation, si possible, pour rendre le processus d’écriture plus efficace.

Avant de passer des exemples, vous devez définir le writer pour les accepter en appelant [**IWMWriter :: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

Pour passer un exemple au writer, procédez comme suit :

1.  Allouez une mémoire tampon et récupérez un pointeur vers l’interface [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) en appelant [**IWMWriter :: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).
2.  Récupérez l’adresse de la mémoire tampon créée à l’étape 1 en appelant [**INSSBuffer :: GetBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer).
3.  Copiez vos données d’exemple dans l’emplacement de la mémoire tampon, en vous assurant que l’exemple passé sera contenu dans la mémoire tampon allouée. Vous pouvez utiliser n’importe quelle fonction de copie de mémoire pour copier vos données. Le choix le plus courant est memcpy, qui est inclus dans la bibliothèque Runtime C standard.
4.  Mettez à jour la quantité de données utilisées dans la mémoire tampon pour refléter la taille réelle de l’exemple en appelant [**INSSBuffer :: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).
5.  Transmettez l’interface de mémoire tampon à l’enregistreur avec le nombre d’entrées et l’heure d’échantillonnage à l’aide de la méthode [**IWMWriter :: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) . Tous les échantillons audio d’une entrée représentent la même durée de contenu, ce qui vous permet de déterminer la durée de l’exemple en ajoutant la durée de l’échantillon à un total cumulé. Pour la vidéo, vous devez calculer l’heure en fonction de la fréquence d’images.

**WriteSample** fonctionne de façon asynchrone et peut ne pas finir d’écrire les données à partir de la mémoire tampon avant que votre application soit prête à appeler à nouveau la méthode. Par conséquent, il est important d’appeler **AllocateSample** une fois pour chaque appel à **WriteSample**. Toutefois, vous pouvez libérer l’interface **INSSBuffer** immédiatement après avoir appelé **WriteSample**.

Lorsque vous avez terminé de passer des exemples, appelez [**IWMWriter :: EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).

**Remarque** Il est important que les exemples de tous les flux du fichier soient transmis au writer en cours de synchronisation les uns avec les autres. Autrement dit, chaque fois que cela est possible, vous devez passer des exemples à l’enregistreur dans l’ordre de la durée de la présentation dans la tolérance de synchronisation spécifiée dans [**IWMWriterAdvanced :: SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance). Les meilleurs résultats sont obtenus lorsque les données sont remises à chaque flux en unités d’une seconde ou moins.

Les flux doivent également se terminer à peu près en même temps. Par exemple, vous ne devez pas écrire un fichier avec un flux audio d’une durée de 45 secondes et un flux vidéo de 50 secondes. Si vous encodez un fichier de ce type avec des entrées non modifiées, certaines données audio à la fin du flux seront supprimées (même s’il s’agit du flux plus petit). Pour que l’encodage de fichier fonctionne, vous devez ajouter 5 secondes de silence à l’entrée audio afin qu’un flux ne se termine pas plusieurs secondes avant un autre. Il n’est pas nécessaire pour les types de flux avec des échantillons intermittents, tels que les flux de texte ou d’image, à remplir de cette manière. Les flux de commandes de script doivent également suivre toutes ces règles.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**Interface IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




