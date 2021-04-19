---
title: Gravure de playlists contenant des fichiers sécurisés
description: Gravure de playlists contenant des fichiers sécurisés
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- Windows Media Format SDK, gravure de playlists avec des fichiers sécurisés
- Windows Media Format SDK, playlists avec des fichiers sécurisés
- ASF (Advanced Systems Format), gravure de playlists avec des fichiers sécurisés
- ASF (format de systèmes avancés), gravage de sélections avec des fichiers sécurisés
- ASF (Advanced Systems Format), sélections avec des fichiers sécurisés
- ASF (format de systèmes avancés), playlists avec des fichiers sécurisés
- gestion des droits numériques (DRM), gravure de playlists avec des fichiers sécurisés
- DRM (Digital Rights Management), gravure de playlists avec des fichiers sécurisés
- gestion des droits numériques (DRM), listes de diffusion avec fichiers sécurisés
- DRM (gestion des droits numériques), sélections avec des fichiers sécurisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214c1dbd4ee08f90b3e5e8aa6186508af5044f29
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "106511275"
---
# <a name="burning-playlists-that-contain-secure-files"></a>Gravure de playlists contenant des fichiers sécurisés

Les licences créées à l’aide des objets du kit de développement logiciel (SDK) Windows Media Rights Manager 10 peuvent spécifier le droit de copier un fichier vers un CD-ROM dans le cadre d’une sélection. Cette fonctionnalité, appelée « gravure de playlist », requiert que vous vérifiiez les licences de tous les fichiers de la sélection avant de commencer à copier les données. Le kit de développement logiciel (SDK) Windows Media Format fournit l’interface [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) pour effectuer la vérification des fichiers.

Pour implémenter la gravure de playlist, procédez comme suit :

1.  Créez une instance de l’objet Reader ou de l’objet lecteur synchrone. Pour plus d’informations, consultez [lecture de fichiers ASF](reading-asf-files.md).
2.  Appelez la méthode **QueryInterface** de l’interface du lecteur ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) ou [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) pour obtenir un pointeur vers l’interface [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) .
3.  Copiez les noms de fichiers de la sélection dans un tableau de chaînes de caractères larges. Les noms de fichiers dans le tableau doivent être dans l’ordre dans lequel ils apparaissent dans la sélection.
4.  Appelez la méthode [**IWMReaderPlaylistBurn :: InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) , en passant un pointeur vers le tableau créé à l’étape 3, pour initialiser la vérification de la licence pour les fichiers.
5.  Lorsque la vérification de la licence est terminée, l’objet lecteur envoie \_ un \_ message de gravure de sélection d’initialisation WMT \_ à votre implémentation de la méthode de rappel [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . Lorsque votre rappel reçoit ce message, appelez la méthode [**IWMReaderPlaylistBurn :: GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) pour obtenir les résultats de la vérification de licence. Cette méthode prend un tableau de variables **HRESULT** qui correspondent aux noms de fichiers dans le tableau passé à **InitPlaylistBurn**. Si toutes les valeurs du tableau de résultats sont égales à S \_ OK, vous pouvez continuer. Si un résultat est un code d’erreur, la sélection ne doit pas être copiée.
6.  À l’aide de la même instance du lecteur, ouvrez et lisez chaque fichier. Vous devez ouvrir les fichiers dans l’ordre dans lequel les noms de fichiers apparaissent dans le tableau de noms de fichiers transmis à **InitPlaylistBurn**.
7.  Une fois que vous avez copié tous les fichiers de la sélection, appelez [**IWMReaderPlaylistBurn :: EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) pour terminer le processus de gravure de la sélection et libérer les ressources utilisées par le lecteur.

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




