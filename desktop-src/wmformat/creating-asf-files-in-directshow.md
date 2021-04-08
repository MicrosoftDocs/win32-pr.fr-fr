---
title: Création de fichiers ASF dans DirectShow (kit de développement logiciel (SDK) Windows Media format 11)
description: Création de fichiers ASF dans DirectShow
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media Format SDK, création de fichiers ASF dans DirectShow
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), création dans DirectShow
- ASF (format de systèmes avancés), création dans DirectShow
- DirectShow, création de fichiers ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe4a6a37a508e5d7c713ae4cf38d771d075cefa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102664"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a>Création de fichiers ASF dans DirectShow (kit de développement logiciel (SDK) Windows Media format 11)

Vous pouvez utiliser DirectShow pour créer des fichiers ASF directement à partir de sources de capture telles que des caméscopes DV ou pour transcoder d’autres fichiers au format Windows Media. Dans l’un ou l’autre scénario, les applications créent des graphiques de filtre qui incluent le filtre d' [enregistreur ASF WM](wm-asf-writer-filter.md) comme convertisseur.

L’enregistreur ASF WM fournit un wrapper partiel pour le kit de développement logiciel (SDK) du format Windows Media. Les applications peuvent utiliser l’interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) du filtre pour passer un profil système (versions 4, 7 ou 8), ou utiliser le kit de développement logiciel (SDK) du format Windows Media directement pour créer un profil personnalisé à passer au filtre. Pour ajouter des métadonnées et d’autres informations d’en-tête, l’application utilise l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , qui peut être obtenue à partir du filtre. Une fois le profil et les métadonnées configurés, l’application peut simplement exécuter le graphique de filtre. En interne, le filtre utilise le kit de développement logiciel (SDK) Windows Media format pour écrire le fichier. Le filtre gère tous les détails de synchronisation audio-vidéo, qui seraient autrement la responsabilité de l’application.

Ce processus est expliqué plus en détail dans les sections suivantes.



| Section                                                                                                           | Description                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Configuration de l’enregistreur ASF de WM (QASF)](configuring-the-wm-asf-writer--qasf.md)                                   | Décrit comment configurer le filtre d’enregistreur ASF WM.                                   |
| [Création de graphiques de filtre pour écrire des fichiers ASF (QASF)](building-filter-graphs-to-write-asf-files--qasf.md)           | Décrit comment créer des graphiques de transcodage et de capture de fichiers.                           |
| [Configuration des profils et des autres propriétés de fichier (QASF)](configuring-profiles-and-other-file-properties--qasf.md) | Décrit comment effectuer diverses tâches de configuration de fichiers ASF à l’aide du writer WM ASF. |



 

 

 
