---
title: Lecture des métadonnées lors de la lecture
description: Lecture des métadonnées lors de la lecture
ms.assetid: 48d37a9e-5e22-4298-abc4-b69998906dcb
keywords:
- Windows Media Format SDK, lecture des métadonnées
- Windows Media Format SDK, lecteurs asynchrones
- Windows Media Format SDK, lecteurs synchrones
- ASF (Advanced Systems Format), lecture des métadonnées
- ASF (format des systèmes avancés), lecture des métadonnées
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- lecteurs asynchrones, lecture des métadonnées
- lecteurs synchrones, lecture des métadonnées
- métadonnées, lire lors de la lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f62100da8c2f27e626e27ae6686e08f7217867ec2775f69292aac495d218fcb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027347"
---
# <a name="reading-metadata-at-playback"></a>Lecture des métadonnées lors de la lecture

L’objet lecteur asynchrone et l’objet lecteur synchrone peuvent lire les métadonnées à partir de l’en-tête d’un fichier ASF chargé. Lors de la lecture de fichiers, les attributs de métadonnées sont en lecture seule. Les deux objets Reader peuvent être interrogés pour les interfaces [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) et [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) .

Pour plus d’informations sur l’accès aux métadonnées, consultez [utilisation des métadonnées](working-with-metadata.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers ASF**](reading-asf-files.md)
</dt> </dl>

 

 




