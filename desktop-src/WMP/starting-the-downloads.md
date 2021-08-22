---
title: Démarrage des téléchargements
description: Démarrage des téléchargements
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Lecteur Windows Media des magasins en ligne, gestionnaire de téléchargement
- magasins en ligne, gestionnaire de téléchargement
- tapez 2 magasins en ligne, gestionnaire de téléchargement
- Lecteur Windows Media des magasins en ligne, démarrage des téléchargements
- magasins en ligne, démarrage des téléchargements
- tapez 2 magasins en ligne, à partir de téléchargements
- Lecteur Windows Media, gestionnaire de téléchargement
- Lecteur Windows Media Gestionnaire de téléchargement
- Gestionnaire de téléchargement
- démarrage des téléchargements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d600bb037204b4dae1c07d8938e92eae2862460b94ef285567a8ca14144e72c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995069"
---
# <a name="starting-the-downloads"></a>Démarrage des téléchargements

Le téléchargement démarre lorsque l’utilisateur clique sur **Télécharger**. Ce bouton est nommé btnDownload dans le code et la fonction du gestionnaire d’événements pour l’événement **OnClick** est nommée « OnDownload ».

« OnDownload » crée d’abord un nouvel objet **DownloadCollection** vide et l’assigne à une variable locale.


```C++
oDLC = g_oManager.createDownloadCollection();

```



Ensuite, la fonction démarre chacun des cinq éléments qui sont téléchargés et stocke l’objet **DownloadItem** retourné dans un tableau.


```C++
g_DLI[0] = oDLC.startDownload(g_sFiles[0], g_sDLType);
g_DLI[1] = oDLC.startDownload(g_sFiles[1], g_sDLType);
g_DLI[2] = oDLC.startDownload(g_sFiles[2], g_sDLType);
g_DLI[3] = oDLC.startDownload(g_sFiles[3], g_sDLType);
g_DLI[4] = oDLC.startDownload(g_sFiles[4], g_sDLType);

```



Le code met ensuite à jour les éléments de l’interface utilisateur avec les informations relatives à la collection de téléchargements et à ses éléments de téléchargement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation du gestionnaire de téléchargement**](using-the-download-manager.md)
</dt> </dl>

 

 




