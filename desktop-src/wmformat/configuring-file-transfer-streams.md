---
title: Configuration des flux de transfert de fichiers
description: Configuration des flux de transfert de fichiers
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
ms.openlocfilehash: 75fac7d2270da82f1f9e82ed9123611ae608dd3c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030841"
---
# <a name="configuring-file-transfer-streams"></a>Configuration des flux de transfert de fichiers

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

[**Configuration commune à tous les flux**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuration de types de flux arbitraires**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Flux de fichiers**](file-streams.md)
</dt> </dl>

 

 




