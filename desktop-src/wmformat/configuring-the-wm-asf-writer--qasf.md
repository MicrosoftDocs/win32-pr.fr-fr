---
title: Configuration de l’enregistreur ASF de WM (QASF)
description: Configuration de l’enregistreur ASF de WM (QASF)
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- Windows Media Format SDK, configuration de WM ASF Writer (QASF)
- Windows Media Format SDK, DirectShow
- Windows Kit de développement logiciel (SDK) Media format, l’enregistreur ASF WM
- Windows Media Format SDK, QASF
- ASF (Advanced Systems Format), configuration de l’enregistreur ASF ASF (QASF)
- ASF (format avancé des systèmes), configuration de l’enregistreur ASF ASF (QASF)
- ASF (Advanced Systems Format), le rédacteur WM ASF
- ASF (format des systèmes avancés), enregistreur ASF WM
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), QASF
- ASF (format avancé des systèmes), QASF
- DirectShow, configuration de l’enregistreur ASF de WM (QASF)
- DirectShow, le rédacteur WM ASF
- DirectShow, QASF
- Rédacteur ASF WM, configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f954522c4acae89e6f6dd001561811088c2a9e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219577"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a>Configuration de l’enregistreur ASF de WM (QASF)

Lorsque le filtre de l' [enregistreur ASF WM](wm-asf-writer-filter.md) est créé, il est configuré automatiquement avec le \_ Profil WMProfile V80 \_ 256Video comme valeur par défaut. étant donné que ce profil utilise les codecs Windows Media Audio et Windows Media Video version 8, il est recommandé de créer un profil personnalisé qui utilise les codecs Windows Media 9 Series, puis de passer son pointeur [**IWMProfile**](iwmprofile.md) au filtre à l’aide de la méthode [**IConfigAsfWriter :: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) . Le filtre doit être ajouté au graphique pour que le filtre puisse être configuré, et il doit être configuré avant de pouvoir être connecté aux filtres en amont. le filtre utilise le profil pour déterminer le type de Windows fichier de Format multimédia à écrire, le nombre de broches d’entrée à configurer et les types de média que les épingles peuvent accepter.

Le filtre autorise la réinitialisation des profils lorsque leurs broches d’entrée sont connectées, tant que le nouveau profil ne nécessite pas de broches d’entrée supplémentaires. Par exemple, si vous modifiez le profil d’un profil audio à entrée unique en un profil audio et vidéo à deux entrées, seul le code confidentiel audio sera reconnectedAll les données d’entrée doivent être horodatées et toutes les broches d’entrée doivent être connectées pour que le filtre puisse être exécuté ou suspendu. Cela signifie que si vous configurez le filtre avec un profil qui a un flux audio et un flux vidéo, le filtre crée un fichier audio et une broche d’entrée vidéo, et les deux broches doivent être connectées pour que le filtre puisse être exécuté.

Ajout d’extensions d’unité de données

Vous pouvez configurer un flux de profil pour les extensions d’unité de données, telles que les codes temporels SMPTE, avant ou après la connexion du filtre, à condition que vous suiviez cet ordre d’opérations :

1.  Ajoutez une ou plusieurs extensions d’unité de données au flux à l’aide de [**IWMStreamConfig2 :: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).
2.  Appelez [**WMProfile :: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) pour mettre à jour le profil.
3.  Appelez [**IConfigAsfWriter :: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) avec l’objet de profil mis à jour.
4.  Recherchez la broche d’entrée vidéo et appelez sa méthode [**IAMWMBufferPass :: SetNotify**](iamwmbufferpass-setnotify.md) pour inscrire votre interface [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) définie par l’application.

Lorsque le graphique est exécuté, votre méthode [**IAMWMBufferPassCallback :: Notify**](iamwmbufferpasscallback-notify.md) est appelée pour chaque frame, et vous pouvez obtenir et définir des propriétés sur l’exemple à l’aide de ses méthodes d’interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .

> [!Note]  
> Dans certains scénarios nécessitant beaucoup de ressources processeur, comme inverse telecine, le rédacteur WM ASF peut nécessiter plus de tampons de sortie que certains filtres en aval peuvent prendre en charge. Par exemple, le décodeur DV n’acceptera pas plus d’une mémoire tampon pour sa broche de sortie et c’est le cas pour le décompresseur AVI dans certaines conditions. Si vous rencontrez des problèmes lors de la tentative de connexion à ces filtres, ou éventuellement lors de l’exécution du graphique, il peut être nécessaire d’écrire un filtre intermédiaire qui accepte un nombre quelconque de mémoires tampons sur sa broche de sortie.

 

 

 