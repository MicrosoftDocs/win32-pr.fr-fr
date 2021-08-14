---
title: Configuration de Flux Web
description: Configuration de Flux Web
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- flux, configuration de flux Web
- codecs, configuration de flux Web
- Flux Web, configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8df1ced96a772a26b674fb47a30a8664d6431ff946328f45467554857b1ee4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199120"
---
# <a name="configuring-web-streams"></a>Configuration de Flux Web

Les flux Web sont un type spécialisé de flux de transfert de fichiers utilisé pour distribuer les fichiers associés à un site Web dans un flux unique. La configuration du flux Web est résumée dans le tableau suivant.



| Paramètre                                            | Description                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| **\_Type de média WM \_ . MajorType**                      | Définissez sur WMMEDIATYPE \_ filetransfer.                                                 |
| **\_Type de média WM \_ . SubType**                        | Définissez sur WMMEDIASUBTYPE \_ webstream.                                                 |
| **\_Type de média WM \_ . bFixedSizeSamples**              | Affectez la valeur false.                                                                     |
| **\_Type de média WM \_ . bTemporalCompression**           | Affectez la valeur true.                                                                      |
| **\_Type de média WM \_ . lSampleSize**                    | Définit la valeur 0.                                                                         |
| **\_Type de média WM \_ . formatType**                     | Définissez sur WMFORMAT \_ webstream.                                                       |
| **\_Type de média WM \_ . punk**                           | Affectez la valeur **null**.                                                                  |
| **\_Type de média WM \_ . cbFormat**                       | Défini sur `sizeof(WMT_WEBSTREAM_FORMAT)`.                                            |
| **\_Type de média WM \_ . pbFormat**                       | Défini sur l’adresse d’une structure de **\_ \_ format de flux de diffusion en continu WMT** correctement configurée. |
| **\_Format WEBSTREAM WMT \_ . cbSampleHeaderFixedData** | Défini sur `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.                                     |
| **\_Format WEBSTREAM WMT \_ . wVersion**                | défini sur 1.                                                                         |
| **\_Format WEBSTREAM WMT \_ . wReserved**               | Définit la valeur 0.                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration commune à tous les Flux**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuration de types de flux arbitraires**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Flux Web**](web-streams.md)
</dt> </dl>

 

 




