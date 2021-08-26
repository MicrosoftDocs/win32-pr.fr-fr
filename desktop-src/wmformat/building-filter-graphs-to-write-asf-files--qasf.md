---
title: Création de graphiques de filtre pour écrire des fichiers ASF (QASF)
description: Création de graphiques de filtre pour écrire des fichiers ASF (QASF)
ms.assetid: 45583c97-4e59-4a6a-987b-5486e6f33990
keywords:
- Windows Media Format SDK, création de graphiques de filtre (QASF)
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, écriture de fichiers ASF (QASF)
- ASF (Advanced Systems Format), création de graphiques de filtre (QASF)
- ASF (format de systèmes avancés), création de graphiques de filtre (QASF)
- ASF (Advanced Systems Format), écriture (QASF)
- ASF (Advanced Systems Format), écriture (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- DirectShow, création de graphiques de filtre (QASF)
- DirectShow, écriture de fichiers ASF (QASF)
- Windows Media Format SDK, QASF
- ASF (Advanced Systems Format), QASF
- ASF (format avancé des systèmes), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6128fb7578d829579aad7e8895be9db4d5a842aa785866253b553d4deb8b3b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055579"
---
# <a name="building-filter-graphs-to-write-asf-files-qasf"></a>Création de graphiques de filtre pour écrire des fichiers ASF (QASF)

en général, les Applications basées sur DirectShow utilisent l’un des trois types de graphiques de filtre de base lors de la création d’un contenu multimédia Windows :

-   les graphiques de filtre pour la conversion ou le transcodage de contenu d’un autre format en Windows format multimédia.
-   les graphiques de filtre pour l’insertion de contenu qui n’est pas Windows les formats de flux (natifs) en fichiers ASF.
-   les graphiques de filtre permettant de capturer des données actives et de les encoder immédiatement dans Windows Format multimédia avant de les enregistrer sur le disque.

Chaque type de graphique de filtre est décrit plus en détail dans les sections suivantes.



| Section                                                                                                             | Description                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Transcodage de fichiers (QASF)](transcoding-files--qasf.md)                                                             | Décrit comment créer des graphiques de filtre de transcodage de fichier.                                               |
| [Insertion de formats de flux natifs dans des fichiers ASF (QASF)](inserting-native-stream-formats-into-asf-files--qasf.md)   | Décrit comment placer tout type de données audio ou vidéo compressées ou non compressées dans un fichier ASF. |
| [Capture directe à partir d’un appareil dans un fichier ASF (QASF)](capturing-directly-from-a-device-to-an-asf-file--qasf.md) | Décrit comment créer des graphiques de filtre de capture qui sont générés dans un fichier ASF.                             |



 

 

 




