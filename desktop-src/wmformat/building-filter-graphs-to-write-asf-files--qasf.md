---
title: Création de graphiques de filtre pour écrire des fichiers ASF (QASF)
description: Création de graphiques de filtre pour écrire des fichiers ASF (QASF)
ms.assetid: 45583c97-4e59-4a6a-987b-5486e6f33990
keywords:
- Kit de développement logiciel (SDK) de format Windows Media, création de graphiques de filtres (QASF)
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, écriture de fichiers ASF (QASF)
- ASF (Advanced Systems Format), création de graphiques de filtre (QASF)
- ASF (format de systèmes avancés), création de graphiques de filtre (QASF)
- ASF (Advanced Systems Format), écriture (QASF)
- ASF (Advanced Systems Format), écriture (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- DirectShow, génération de graphiques de filtre (QASF)
- DirectShow, écriture de fichiers ASF (QASF)
- Windows Media Format SDK, QASF
- ASF (Advanced Systems Format), QASF
- ASF (format avancé des systèmes), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbf0a261d1502f76cebc0eb2141cd230c509029
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517942"
---
# <a name="building-filter-graphs-to-write-asf-files-qasf"></a>Création de graphiques de filtre pour écrire des fichiers ASF (QASF)

Les applications basées sur DirectShow utilisent généralement l’un des trois types de graphiques de filtre de base lors de la création de contenu Windows Media :

-   Les graphiques de filtre pour la conversion ou le transcodage de contenu à partir d’un autre format au format Windows Media.
-   Graphiques de filtre pour l’insertion de contenu qui n’est pas basé sur Windows Media (formats de flux natifs) dans des fichiers ASF.
-   Les graphiques de filtre permettant de capturer des données actives et de les encoder immédiatement dans le format Windows Media avant de les enregistrer sur le disque.

Chaque type de graphique de filtre est décrit plus en détail dans les sections suivantes.



| Section                                                                                                             | Description                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Transcodage de fichiers (QASF)](transcoding-files--qasf.md)                                                             | Décrit comment créer des graphiques de filtre de transcodage de fichier.                                               |
| [Insertion de formats de flux natifs dans des fichiers ASF (QASF)](inserting-native-stream-formats-into-asf-files--qasf.md)   | Décrit comment placer tout type de données audio ou vidéo compressées ou non compressées dans un fichier ASF. |
| [Capture directe à partir d’un appareil dans un fichier ASF (QASF)](capturing-directly-from-a-device-to-an-asf-file--qasf.md) | Décrit comment créer des graphiques de filtre de capture qui sont générés dans un fichier ASF.                             |



 

 

 




