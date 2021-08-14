---
title: Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur synchrone
description: Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur synchrone
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- ASF (Advanced Systems Format), recherche par les codes temporels SMPTE
- ASF (format des systèmes avancés), recherche par les codes temporels SMPTE
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- ASF (Advanced Systems Format), codes temporels SMPTE
- ASF (format des systèmes avancés), codes temporels SMPTE
- lecteurs synchrones, recherche par code de temps SMPTE
- lecteurs synchrones, codes temporels SMPTE
- Codes temporels SMPTE, recherche
- Codes temporels SMPTE, lecteurs synchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b368492d45d3bc564ce0fbb84a6013349c26fcdaca8c1ad576863a9cee6f6f36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196468"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a>Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur synchrone

L’objet lecteur synchrone peut rechercher un point dans un fichier en fonction du code temporel SMPTE associé à un flux vidéo. Les données de code d’heure sont encapsulées dans les structures de [**\_ données d' \_ extension \_ du code**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) d’erreur WMT qui sont attachées à des exemples vidéo en tant qu’extensions d’unité de données.

Les codes temporels SMPTE sont définis par une plage et un code horaire dans cette plage. Une plage est une série continue de codes temporels. Chaque code de temps est défini par les heures, les minutes, les secondes et les frames.

Pour rechercher des données dans un fichier ASF par code temporel SMPTE à l’aide du lecteur synchrone, procédez comme suit.

1.  Définissez le code d’heure de début et le code d’heure de fin pour l’exemple de livraison en appelant [**IWMSyncReader :: SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe). Vous devez spécifier le numéro de flux d’un flux vidéo indexé par code de temps. Le lecteur synchrone synchronise le reste des sorties avec l’heure de présentation du cadre spécifié du flux spécifié.
2.  Commencez la récupération des exemples avec des appels à [**IWMSyncReader :: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Procédez comme vous le feriez normalement avec le lecteur synchrone.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers avec le lecteur synchrone**](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[**Prise en charge des codes temporels SMPTE**](smpte-time-code-support.md)
</dt> <dt>

[**Utilisation des index**](working-with-indexes.md)
</dt> </dl>

 

 




