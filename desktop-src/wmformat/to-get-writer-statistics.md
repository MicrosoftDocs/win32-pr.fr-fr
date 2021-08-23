---
title: Pour connaître les statistiques de l’enregistreur
description: Pour connaître les statistiques de l’enregistreur
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- ASF (Advanced Systems Format), statistiques de l’enregistreur
- ASF (format des systèmes avancés), statistiques de l’enregistreur
- statistiques de l’enregistreur, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cedd96f1e94b8d3c9499fe08e3eeebb2100e866b141b756483cfb07bb7cb0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083964"
---
# <a name="to-get-writer-statistics"></a>Pour connaître les statistiques de l’enregistreur

Le writer peut fournir des informations statistiques sur l’écriture d’opérations. Il existe deux méthodes pour collecter des statistiques d’enregistreur : [**IWMWriterAdvanced :: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) et [**IWMWriterAdvanced3 :: GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex). Les informations extraites par **GetStatisticsEx** sont plus spécifiques que les informations récupérées par **GetStatistics**.

Les deux méthodes remplissent des structures avec des informations statistiques. **GetStatistics** utilise la structure de statistiques de l' [**\_ \_ enregistreur WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) et **GetStatisticsEx** utilise la structure des statistiques de l' [**\_ enregistreur WM \_ \_ ex**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) . **GetStatisticsEx** ne duplique pas les données obtenues par **GetStatistics**. Pour obtenir les informations les plus complètes, vous devez appeler les deux méthodes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Interface IWMWriterAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




