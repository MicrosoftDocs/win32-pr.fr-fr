---
description: Le writer du récepteur est un composant permettant d’encoder des fichiers audio ou vidéo.
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: Enregistreur du récepteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1cfa60abb9b107030aba18e30175592d637c7676ff44781d62b3f5c1509351
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887352"
---
# <a name="sink-writer"></a>Enregistreur du récepteur

Le writer du récepteur est un composant permettant d’encoder des fichiers audio ou vidéo.

Le diagramme suivant montre, à un niveau élevé, comment une application utilise le writer de récepteur pour encoder et fichier audio/vidéo.

![diagramme qui montre le writer du récepteur.](images/encoding09.png)

Le writer du récepteur héberge un récepteur multimédia et éventuellement un ou plusieurs encodeurs. Les encodeurs convertissent les données audio ou vidéo non compressées en séquences binaires codées. Le récepteur multimédia génère des flux de fichiers binaires dans un fichier. L’enregistreur du récepteur effectue les tâches suivantes :

-   Charge le récepteur multimédia.
-   Recherche et charge les encodeurs.
-   Gère le workflow aux encodeurs et au récepteur multimédia.

L’application transmet les données audio/vidéo au writer du récepteur en tant qu’entrée. La façon dont l’application obtient ou génère les données d’entrée n’a pas d’importance. L’une des options consiste à utiliser le [lecteur source](source-reader.md), comme indiqué dans le diagramme suivant. Toutefois, l’enregistreur du récepteur ne requiert pas l’utilisation du lecteur source. Ces deux composants sont indépendants.

![diagramme qui montre le lecteur source et le writer du récepteur.](images/encoding02.png)

## <a name="in-this-section"></a>Dans cette section

-   [Utilisation de l’enregistreur du récepteur](using-the-sink-writer.md)
-   [Didacticiel : utilisation de l’enregistreur récepteur pour encoder une vidéo](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codage et création de fichier](encoding-and-file-authoring.md)
</dt> <dt>

[Vue d’ensemble de l’encodage dans Media Foundation](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



