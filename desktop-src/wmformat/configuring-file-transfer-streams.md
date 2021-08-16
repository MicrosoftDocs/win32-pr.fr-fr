---
title: Configuration du transfert de fichiers Flux
description: Configuration du transfert de fichiers Flux
ms.assetid: faed54ae-9e80-492a-9602-e726bdb3b54a
keywords:
- flux, configuration des flux de transfert de fichiers
- codecs, configuration des flux de transfert de fichiers
- flux de transfert de fichiers
- flux, extensions d’unité de données
- codecs, extensions d’unité de données
- extensions d’unité de données, flux de transfert de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0be95c9760a02275e223f56785149f6867d4aaf2462d07d158991b3cd21c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849062"
---
# <a name="configuring-file-transfer-streams"></a>Configuration du transfert de fichiers Flux

Les flux de transfert de fichiers ne nécessitent pas de paramètres spéciaux dans la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Ils requièrent une extension d’unité de données pour associer un nom de fichier à chaque exemple. Pour envoyer un nom avec des exemples de transfert de fichiers, vous devez implémenter un système d’extension d’unité de données pour le flux.

Pour définir une extension d’unité de données pour le flux, procédez comme suit :

1.  Obtenez un pointeur vers l’interface [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) de l’objet de configuration de flux en appelant **IWMStreamConfig :: QueryInterface**.
2.  Ajoutez une extension d’unité de données pour le flux en appelant [**IWMStreamConfig2 :: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) comme suit :
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration commune à tous les Flux**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuration de types de flux arbitraires**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Flux de fichiers**](file-streams.md)
</dt> </dl>

 

 




