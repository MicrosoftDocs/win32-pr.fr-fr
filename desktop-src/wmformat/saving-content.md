---
title: Enregistrement du contenu
description: Enregistrement du contenu
ms.assetid: 22f4e580-43a4-48b5-8eb3-90e1346a1093
keywords:
- Windows Media Format SDK, enregistrement du contenu
- Windows Media Format SDK, Fast cache streaming
- ASF (Advanced Systems Format), enregistrement du contenu
- ASF (format des systèmes avancés), enregistrement du contenu
- ASF (Advanced Systems Format), diffusion en continu du cache rapide
- ASF (format de systèmes avancés), diffusion en continu de cache rapide
- flux, enregistrement du contenu
- Diffusion en continu rapide du cache, enregistrement du contenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c215a81accef29f8943ed52ca24264f785d94
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724082"
---
# <a name="saving-content"></a>Enregistrement du contenu

À l’aide de ce kit de développement logiciel (SDK), une application peut enregistrer le contenu téléchargé ou diffusé sur l’ordinateur local de l’utilisateur, en appelant la méthode [**IWMReaderAdvanced2 :: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) sur l’objet lecteur. Pour le contenu diffusé en continu, le serveur doit utiliser Fast cache streaming, qui est décrit dans la section [activation de la diffusion en continu du cache rapide à partir du client](enabling-fast-cache-streaming-from-the-client.md). Pour le contenu diffusé en continu, la méthode **SaveFileAs** crée un fichier ASX qui pointe vers un fichier ASF contenant le contenu enregistré. Si l’objet lecteur diffuse en continu une sélection côté serveur, chaque entrée est enregistrée en tant que fichier ASF distinct, et le fichier ASX pointe vers chacun des fichiers ASF. Pour le contenu téléchargé, la méthode **SaveFileAs** crée simplement un fichier ASF.

Pour enregistrer du contenu dans un fichier local, procédez comme suit :

1.  Appelez [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) avec l’URL. **Open** est un appel asynchrone et est retourné immédiatement. Attendez que l’opération se termine, comme décrit dans [pour créer un lecteur et ouvrir un fichier](to-create-a-reader-and-open-a-file.md).
2.  Interrogez l’objet lecteur de l’interface [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) .
3.  Vérifiez si le contenu peut être enregistré en appelant la méthode [**IWMReaderAdvanced4 :: CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) . Si la méthode retourne la valeur false, le contenu ne peut pas être enregistré localement. Dans le cas contraire, passez à l’étape 4.
4.  Appelez la méthode [**IWMReaderAdvanced4 :: IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) pour déterminer si le serveur utilise la diffusion en continu du cache rapide.
5.  Appelez [**IWMReaderAdvanced2 :: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) avec un nom de fichier pour le fichier local. Si la méthode **IsUsingFastCache** a retourné la valeur true, donnez au fichier un nom d’extension. asx. Sinon, donnez au nom de fichier une extension. ASF,. WMA ou. wmv.

L’application peut annuler l’opération d’enregistrement pendant qu’elle est en cours, en appelant la méthode [**IWMReaderAdvanced4 :: CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) .

Le contenu enregistré peut être protégé par DRM, donc il n’est pas possible de lire le fichier sur un autre ordinateur. Pour plus d’informations sur la protection du contenu, consultez [fonctionnalités de Rights Management numérique](digital-rights-management-features.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interface IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




