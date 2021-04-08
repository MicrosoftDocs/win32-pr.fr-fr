---
title: Index
description: Index
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- Windows Media Format SDK, index
- ASF (Advanced Systems Format), index
- ASF (format avancé des systèmes), index
- Windows Media Format SDK, index temporels
- ASF (Advanced Systems Format), index temporels
- ASF (format de systèmes avancés), index temporels
- Kit de développement logiciel (SDK) Windows Media format, index basés sur des frames
- ASF (Advanced Systems Format), index basés sur des trames
- ASF (format de systèmes avancés), index basés sur des trames
- Windows Media Format SDK, codes temporels SMPTE
- ASF (Advanced Systems Format), codes temporels SMPTE
- ASF (format des systèmes avancés), codes temporels SMPTE
- index, à propos de
- index temporels
- index basés sur des frames
- Codes temporels SMPTE, index
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2e5a194f9c495720cbc40ccdb192509723eee0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840581"
---
# <a name="indexes"></a>Index

Une exigence courante pour les applications qui lisent des fichiers multimédias numériques est la possibilité de rechercher un point spécifique dans le contenu. La recherche peut être difficile, car il n’y a aucune garantie que les différents flux d’un fichier comportent des échantillons avec des heures de début simultanées. Ce problème est résolu avec l’utilisation d' *index*. Un index est un objet dans un fichier ASF qui représente des exemples vidéo avec les durées de présentation. Aucun index n’est requis pour les flux audio, car les données audio sont plus étroitement liées à l’heure de présentation que les données vidéo.

L’objet indexeur du kit de développement logiciel (SDK) du format Windows Media peut créer trois types d’index différents : les index temporels, les index basés sur des trames et les index de code temporel SMPTE.

Les index temporels sont le type le plus courant. Ils associent simplement les exemples de vidéos aux temps de présentation correspondants.

Un index basé sur des frames correspond à des exemples vidéo avec des nombres d’images vidéo et des durées de présentation. Les numéros de frame sont particulièrement utiles dans les applications qui modifient la vidéo.

Un index de code de temps SMTP est le type d’index le plus rare. Il utilise le code de temps SMPTE comme base de l’index et peut être utilisé uniquement sur les flux qui ont des horodatages SMPTE inclus avec leurs échantillons. Pour plus d’informations sur le code temporel SMPTE, consultez [prise en charge du code temporel SMPTE](smpte-time-code-support.md).

Un fichier ASF peut contenir un index de chaque type pour chaque flux vidéo qu’il contient. Par défaut, un index temporel est inclus pour chaque flux vidéo dans des fichiers créés par l’objet Writer. Vous pouvez modifier les paramètres d’indexation automatique de vos fichiers en fonction de vos besoins.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités des fichiers ASF**](asf-file-features.md)
</dt> <dt>

[**Utilisation des index**](working-with-indexes.md)
</dt> <dt>

[**Lecture des fichiers avec le lecteur asynchrone**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lecture des fichiers avec le lecteur synchrone**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




