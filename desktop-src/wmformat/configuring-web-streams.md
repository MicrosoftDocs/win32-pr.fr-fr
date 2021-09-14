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
ms.openlocfilehash: 27c91c36788b858b2378ebf46b553f076c5ec490
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219561"
---
# <a name="configuring-web-streams"></a>Configuration de Flux Web

Les flux Web sont un type spécialisé de flux de transfert de fichiers utilisé pour distribuer les fichiers associés à un site Web dans un flux unique. La configuration du flux Web est résumée dans le tableau suivant.



| Paramètre                                            | Description                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| **\_Type de média WM \_ . MajorType**                      | Définissez sur WMMEDIATYPE \_ filetransfer.                                                 |
| **\_Type de média WM \_ . SubType**                        | Définissez sur WMMEDIASUBTYPE \_ webstream.                                                 |
| **\_Type de média WM \_ . bFixedSizeSamples**              | Affectez la valeur false.                                                                     |
| **\_Type de média WM \_ . bTemporalCompression**           | Définissez sur True.                                                                      |
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

 

 




