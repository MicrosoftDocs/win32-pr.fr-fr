---
description: Configuration de l’enregistreur ASF
ms.assetid: 5708c4a0-6197-4a42-adfd-01c6dfe86302
title: Configuration de l’enregistreur ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e3d28b3b6178a383909f53a98fef98a5c3e69297f71615010f505d28b77375a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871699"
---
# <a name="configuring-the-asf-writer"></a>Configuration de l’enregistreur ASF

Lorsque le filtre de l' [enregistreur ASF WM](wm-asf-writer-filter.md) est créé, il est configuré automatiquement avec le \_ Profil WMProfile V80 \_ 256Video. ce profil utilise les codecs Windows Media Audio et Windows Media Video version 8, qui ne sont pas aussi récents que les codecs Windows Media 9 Series. nous vous recommandons de créer un profil personnalisé qui utilise les codecs de la série Media 9 Windows, puis de configurer l’enregistreur WM ASF avec le profil personnalisé, comme décrit dans [configuration de profils et d’autres propriétés de fichier asf](configuring-profiles-and-other-asf-file-properties.md). Vous devez ajouter le filtre d’enregistreur ASF WM au graphique de filtre avant de configurer le filtre et configurer le filtre avant de le connecter à d’autres filtres.

Toutes les données d’entrée doivent être horodatées et toutes les broches d’entrée doivent être connectées pour que le filtre puisse être exécuté ou suspendu. Par conséquent, si vous configurez le filtre avec un profil qui a un flux audio et un flux vidéo, le filtre crée un fichier audio et une broche d’entrée vidéo, et les deux broches doivent être connectées pour que le filtre puisse être exécuté. étant donné que le kit de développement logiciel (SDK) Windows Media Format requiert un flux audio, le rédacteur de fichiers ASF doit toujours disposer d’un code confidentiel audio d’entrée, même s’il s’agit d’un flux factice, c’est-à-dire un flux audio en sourdine et à vitesse de transmission faible.

Ajout d’extensions d’unité de données

Vous pouvez configurer un flux de profil pour les extensions d’unité de données, telles que les codes temporels SMPTE, avant ou après la connexion du filtre, à condition que vous suiviez cet ordre d’opérations :

1.  Ajoutez une ou plusieurs extensions d’unité de données au flux à l’aide de **IWMStreamConfig2 :: AddDataUnitExtension**.
2.  Appelez **IWMProfile :: ReconfigStream** pour mettre à jour le profil.
3.  Appelez [**IConfigAsfWriter :: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) avec l’objet de profil mis à jour.
4.  Recherchez la broche d’entrée vidéo et appelez sa méthode [**IAMWMBufferPass :: SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) pour inscrire votre interface [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) définie par l’application.

Lorsque le graphique est exécuté, votre méthode [**IAMWMBufferPassCallback :: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) est appelée pour chaque frame, et vous pouvez obtenir et définir des propriétés sur l’exemple à l’aide de ses méthodes d’interface **INSSBuffer3** .

> [!Note]  
> Dans certains scénarios nécessitant beaucoup de ressources processeur, comme inverse telecine, le rédacteur WM ASF peut nécessiter plus de tampons de sortie que certains filtres en aval peuvent prendre en charge. Par exemple, le décodeur DV n’acceptera pas plus d’une mémoire tampon pour sa broche de sortie et c’est le cas pour le décompresseur AVI dans certaines conditions. Si vous rencontrez des problèmes lors de la tentative de connexion à ces filtres, ou éventuellement lors de l’exécution du graphique, il peut être nécessaire d’écrire un filtre intermédiaire qui accepte un nombre quelconque de mémoires tampons sur sa broche de sortie.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



