---
title: Pour transcoder du contenu avec la recompression intelligente
description: Pour transcoder du contenu avec la recompression intelligente
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- Kit de développement logiciel (SDK) Windows Media format, transcodage de contenu
- Windows Media Format SDK, recompression intelligente
- Windows Media Format SDK, recompression
- Windows Media Format SDK, Windows Media Audio codecs
- ASF (Advanced Systems Format), contenu de transcodage
- ASF (format des systèmes avancés), transcodage du contenu
- Format de systèmes avancés (ASF), recompression intelligente
- ASF (format de systèmes avancés), recompression intelligente
- Format de systèmes avancés (ASF), recompression
- ASF (format des systèmes avancés), recompression
- Formats ASF (Advanced Systems Format), Windows Media Audio les codecs
- ASF (format des systèmes avancés), Windows Media Audio codecs
- contenu de transcodage
- recompression intelligente
- recompression
- Codecs Windows Media Audio, contenu de transcodage
- codecs, Windows Media Audio les codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1317989ea9384d4a9747d712af1ce5c61d484c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314293"
---
# <a name="to-transcode-content-with-smart-recompression"></a>Pour transcoder du contenu avec la recompression intelligente

Vous pouvez transcoder du contenu d’une vitesse de transmission à une autre à l’aide du kit de développement logiciel (SDK) Windows Media format. Normalement, cela implique simplement le décodage du contenu et son encodage à la vitesse de transmission souhaitée. Le codec Windows Media Audio 9 prend en charge la recompression intelligente, qui permet le transcodage qui atteint une qualité supérieure à la normale.

Pour la recompression intelligente, le flux audio d’origine doit être encodé avec le codec Windows Media Audio. Toutes les versions du codec sont prises en charge, mais les codecs audio spécialisés (Windows Media Audio 9 Professional et Windows Media Audio 9 Voice) ne le sont pas. Si l’audio d’origine a été encodé avec le codec Windows Media Audio 9 Lossless, il n’est pas nécessaire d’utiliser la recompression intelligente, car aucune information n’a été perdue dans l’encodage d’origine.

Pour utiliser la recompression intelligente, procédez comme suit.

1.  Configurez un objet lecteur avec le fichier source pour la lecture. Pour plus d’informations, consultez [lecture de fichiers ASF](reading-asf-files.md).
2.  Configurez un objet Writer à utiliser pour le transcodage du fichier. Définissez le nom de fichier du nouveau fichier. Sélectionnez un profil à utiliser pour le nouveau fichier. Définissez le profil sélectionné dans l’objet Writer. Pour plus d’informations, consultez [écriture de fichiers ASF](writing-asf-files.md).
3.  Obtenir un pointeur vers l’interface [**IWMProfile**](iwmprofile.md) de l’objet lecteur en appelant **IWMReader :: QueryInterface**.
4.  Récupérez l’interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) pour le flux audio à transcoder en appelant [**IWMProfile :: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).
5.  Obtenir l’interface [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) pour l’objet de configuration de flux en appelant **IWMStreamConfig :: QueryInterface**.
6.  Récupérez la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) pour le flux en effectuant deux appels à [**IWMMediaProps :: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Obtenir la taille de la structure sur le premier appel et allouer de la mémoire pour qu’une mémoire tampon passe au deuxième appel.
7.  Obtenir un pointeur vers l’interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) pour l’entrée dans le writer en appelant [**IWMWriter :: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).
8.  Obtenir l’interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) pour l’objet de propriétés de média d’entrée en appelant **IWMInputMediaProps :: QueryInterface**.
9.  Utilisez la méthode [**IWMPropertyVault :: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) pour définir la \_ propriété g wszOriginalWaveFormat. Utilisez la structure **WAVEFORMATEX** obtenue à l’étape 6 comme valeur de la propriété.
10. Incluez les modifications apportées aux propriétés du média d’entrée en appelant [**IWMWriter :: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) et en lui transmettant un pointeur vers l’interface **IWMInputMediaProps** .
11. Commencez la lecture des exemples à partir du fichier d’origine et transmettez-les au writer avec des appels à [**IWMWriter :: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Rubriques avancées**](advanced-topics.md)
</dt> <dt>

[**Interface IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[**Interface IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**Interface IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interface IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[**Interface IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 




