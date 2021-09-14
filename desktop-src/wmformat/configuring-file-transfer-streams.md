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
ms.openlocfilehash: 75fac7d2270da82f1f9e82ed9123611ae608dd3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219644"
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

 

 




