---
title: Exécution de fichiers à partir d’une source réseau
description: Exécution de fichiers à partir d’une source réseau
ms.assetid: 72f2d685-56fc-4da2-8372-3774cc65f59d
keywords:
- Windows Media Format SDK, lire des données ASF
- Windows Media Format SDK, exécuter des fichiers à partir de sources réseau
- ASF (Advanced Systems Format), lecture des données
- ASF (format des systèmes avancés), lire les données
- ASF (Advanced Systems Format), exécuter des fichiers à partir de sources réseau
- ASF (format des systèmes avancés), exécuter des fichiers à partir de sources réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1e4e41ddf94498ddeddf90e64439c1b11b7ba8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411360"
---
# <a name="playing-files-from-a-network-source"></a>Exécution de fichiers à partir d’une source réseau

La lecture à partir d’un réseau n’est pas fondamentalement différente de la lecture d’un fichier local. L’application passe l’URL à la méthode [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) de l’objet lecteur et l’objet lecteur gère les détails des protocoles réseau. L’objet lecteur utilise la gestion de tampons intelligente pour offrir la lecture la plus lisse possible. Si l’application a besoin de davantage de contrôle sur les paramètres réseau de l’objet lecteur, ceux-ci sont disponibles via les interfaces [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig) et [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) .

Le contenu d’une source réseau se trouve dans l’une des deux catégories suivantes :

-   Contenu. Les données sont transmises juste à temps pour être lues sur l’ordinateur local. les serveurs qui exécutent Services Windows Media peuvent fournir des données de streaming. Si le contenu de la vitesse de transmission multiple (MBR) est diffusé en continu, le client peut demander une vitesse de transmission différente du serveur en fonction de la progression de la diffusion en continu.
-   Avez. Toutes les données sont transmises aussi rapidement que possible afin qu’elles puissent être enregistrées sous la forme d’un fichier sur l’ordinateur local. Les serveurs Web fournissent des données téléchargées. Il n’y a aucune communication entre le client et le serveur une fois le téléchargement démarré.

Lorsque l’objet lecteur télécharge un fichier à partir d’un serveur Web, il utilise une technique appelée diffusion en continu progressive, qui permet à un joueur de commencer à afficher le contenu avant que le téléchargement soit terminé. Les données sont mises en mémoire tampon pour fournir un flot de données ininterrompues au joueur. Des informations telles que le taux de transfert et la durée du contenu sont utilisées pour déterminer la durée pendant laquelle les données doivent être mises en mémoire tampon avant de les donner au joueur.

Pour ouvrir un fichier ou un flux sur un réseau, appelez la méthode **IWMReader :: Open** de l’objet lecteur avec l’URL appropriée. **Open** est un appel asynchrone, donc il est retourné immédiatement. Lorsque la source est prête pour la lecture, l’objet lecteur envoie une \_ notification WMT ouverte à la méthode de rappel [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) de l’application. À ce stade, l’application peut interroger le lecteur pour le mode de remise en appelant [**IWMReaderAdvanced2 :: GetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode). Pour le contenu réseau, cette méthode retourne le téléchargement d’un \_ mode de lecture WMT, l’indication du \_ \_ contenu téléchargé ou la \_ \_ diffusion en continu du mode de lecture WMT \_ , indiquant le contenu diffusé en continu.

Pour commencer à lire le fichier ou le flux, appelez la méthode [**IWMReader :: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) . Le lecteur envoie une \_ notification de démarrage de mise en mémoire tampon WMT \_ lorsqu’il commence à mettre en mémoire tampon le contenu, et une \_ notification d’arrêt de mise en mémoire tampon WMT lorsque la mise en \_ mémoire tampon est terminée. Tandis que le lecteur met en mémoire tampon du contenu (c’est-à-dire entre ces deux notifications), vous pouvez afficher la progression de la mise en mémoire tampon pour l’utilisateur. La méthode [**IWMReaderAdvanced2 :: GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress) retourne le pourcentage de données qui ont été mises en mémoire tampon et la durée estimée restante. Pour le contenu téléchargé, vous pouvez également appeler [**IWMReaderAdvanced2 :: GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress) pour obtenir la progression du téléchargement. Appelez ces méthodes à plusieurs reprises pour mettre à jour votre affichage, jusqu’à ce que la mise en mémoire tampon soit terminée. La mise en mémoire tampon peut se produire à nouveau lors de la lecture, en raison de facteurs tels que la congestion du réseau. Si cela se produit, l’application reçoit une autre notification de démarrage de la \_ mise en mémoire tampon WMT \_ .

Lorsque l’objet lecteur commence à lire le contenu, il envoie une notification de démarrage de WMT \_ . À mesure que chaque échantillon est décodé et devient disponible pour le rendu, le lecteur le transmet à l’application par le biais de la méthode de rappel [**IWMReaderCallback :: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) . À ce stade, le processus est le même que pour la lecture de fichiers locaux. Lorsque la lecture s’arrête, le lecteur envoie \_ une \_ notification de fin de \_ diffusion WMT.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers ASF**](reading-asf-files.md)
</dt> </dl>

 

 




