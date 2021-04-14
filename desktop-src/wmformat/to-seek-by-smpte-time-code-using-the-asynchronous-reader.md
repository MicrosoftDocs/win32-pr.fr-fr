---
title: Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur asynchrone
description: Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur asynchrone
ms.assetid: 5c618f04-3761-418c-b75a-70c7bf7fa5be
keywords:
- ASF (Advanced Systems Format), recherche par les codes temporels SMPTE
- ASF (format des systèmes avancés), recherche par les codes temporels SMPTE
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), codes temporels SMPTE
- ASF (format des systèmes avancés), codes temporels SMPTE
- lecteurs asynchrones, recherche par les codes temporels SMPTE
- lecteurs asynchrones, codes temporels SMPTE
- Codes temporels SMPTE, recherche
- Codes temporels SMPTE, lecteurs asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bb90e899db9820ccbd14e42b9699a5f99c7434
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381475"
---
# <a name="to-seek-by-smpte-time-code-using-the-asynchronous-reader"></a>Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur asynchrone

L’objet lecteur peut rechercher un point dans un fichier en fonction du code temporel SMPTE associé à un flux vidéo. Les données de code d’heure sont encapsulées dans les structures de [**\_ données d' \_ extension \_ du code**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) d’erreur WMT qui sont attachées à des exemples vidéo en tant qu’extensions d’unité de données.

Les codes temporels SMPTE sont définis par une plage et un code horaire dans cette plage. Une plage est une série continue de codes temporels. Chaque code de temps est défini par les heures, les minutes, les secondes et les frames.

Pour rechercher des données dans un fichier ASF par code temporel SMPTE à l’aide du lecteur asynchrone, procédez comme suit.

1.  Obtenez un pointeur vers l’interface [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) de l’objet lecteur en appelant **IWMReader :: QueryInterface**.
2.  Définissez le code et la durée de l’heure de début en appelant [**IWMReaderAdvanced3 :: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition). Vous devez spécifier le numéro de flux d’un flux vidéo qui est indexé par code de temps. Le lecteur synchronise le reste des sorties avec l’heure de présentation du frame spécifié du flux spécifié et commence à fournir des exemples de sortie.
3.  Gérez les exemples comme vous le feriez normalement dans votre implémentation de la méthode **IWMReaderCallback :: OnSample** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers avec le lecteur asynchrone**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Utilisation des index**](working-with-indexes.md)
</dt> <dt>

[**Prise en charge des codes temporels SMPTE**](smpte-time-code-support.md)
</dt> </dl>

 

 




