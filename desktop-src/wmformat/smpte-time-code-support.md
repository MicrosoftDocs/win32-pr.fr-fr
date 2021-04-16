---
title: Prise en charge des codes temporels SMPTE
description: Prise en charge des codes temporels SMPTE
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- Windows Media Format SDK, codes temporels SMPTE
- ASF (Advanced Systems Format), codes temporels SMPTE
- ASF (format des systèmes avancés), codes temporels SMPTE
- Windows Media Format SDK, interface IWMReaderTimecode
- ASF (Advanced Systems Format), interface IWMReaderTimecode
- ASF (format des systèmes avancés), interface IWMReaderTimecode
- Codes temporels SMPTE, à propos de
- IWMReaderTimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecf8ef9da7d0fb0ee7d973cf21129f307066bc9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507795"
---
# <a name="smpte-time-code-support"></a>Prise en charge des codes temporels SMPTE

Le kit de développement logiciel (SDK) du format Windows Media offre une prise en charge limitée du code temporel SMPTE, qui est un format de code de temps standard pour les films et la télévision. Vous pouvez inclure des données de code temporel SMPTE avec des exemples comme extensions d’unité de données. La partie données de l’extension est une structure de [**\_ données d' \_ extension \_ de code**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) d’exécution WMT qui contient les informations de l’horodatage SMPTE d’origine.

La conservation du code temporel SMPTE dans vos fichiers ASF est accompagnée de limites de performances. Chaque échantillon avec un horodatage SMPTE associé nécessite le transport des 14 octets dans la structure de l’horodatage. Dans un scénario de diffusion en continu, cette exigence accrue en bande passante peut être catastrophique. Par conséquent, il est recommandé de conserver les codes temporels SMPTE uniquement dans les fichiers ASF pendant le processus de modification vidéo, ce qui est généralement fait avec des fichiers locaux. Une fois le fichier final créé, vous devez supprimer les extensions d’unité de données.

Vous pouvez lire les horodatages SMPTE comme vous le feriez pour n’importe quelle autre extension d’unité de données, mais les objets de lecture offrent une prise en charge intégrée de la recherche par code de temps SMPTE. Pour pouvoir Rechercher les horodatages SMPTE, vous devez d’abord indexer le fichier par code de temps SMPTE. Vous pouvez configurer l’indexeur de façon à indexer les codes de temps à l’aide de la méthode [**IWMIndexer2 :: configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) .

À l’aide du lecteur asynchrone, vous pouvez naviguer dans un fichier à l’aide des horodatages SMPTE à l’aide des méthodes de l’interface [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) et de la méthode [**IWMReaderAdvanced3 :: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) . Avec le lecteur synchrone, utilisez [**IWMSyncReader2 :: SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités des fichiers ASF**](asf-file-features.md)
</dt> <dt>

[**Configuration d’extensions d’unité de données**](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




