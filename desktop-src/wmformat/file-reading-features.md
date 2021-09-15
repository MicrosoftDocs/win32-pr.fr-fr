---
title: Fonctionnalités de lecture de fichier
description: Fonctionnalités de lecture de fichier
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- Windows Media Format SDK, fonctionnalités de lecture de fichiers
- Windows Media Format SDK, lecture asynchrone des fichiers
- Windows Media Format SDK, lecture synchrone de fichiers
- ASF (Advanced Systems Format), fonctionnalités de lecture de fichiers
- ASF (format des systèmes avancés), fonctionnalités de lecture de fichiers
- ASF (Advanced Systems Format), lecture asynchrone des fichiers
- ASF (format de systèmes avancés), lecture de fichier asynchrone
- ASF (Advanced Systems Format), lecture synchrone des fichiers
- ASF (format avancé des systèmes), lecture synchrone des fichiers
- lecture asynchrone de fichiers
- lecture synchrone de fichiers
- lecteurs synchrones, fonctionnalités de lecture de fichiers
- lecture du fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83d3ce112d0d9e47626b4f7850f760da5c6583e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521081"
---
# <a name="file-reading-features"></a>Fonctionnalités de lecture de fichier

la lecture des fichiers ASF est l’une des principales fonctionnalités du kit de développement logiciel (SDK) de Format multimédia Windows. Deux types de lecture sont pris en charge : asynchrone et synchrone. La lecture asynchrone des fichiers est gérée par l’objet lecteur. L’objet lecteur synchrone est utilisé pour lire les fichiers de façon synchrone. Pour plus d’informations sur les différents objets de lecture, consultez [objet lecteur](reader-object.md) et [objet lecteur synchrone](synchronous-reader-object.md).

Dans le scénario de lecture de fichier asynchrone le plus basique, vous devez implémenter une méthode de rappel que l’objet lecteur appellera quand les exemples sont prêts. Une fois que vous avez commencé à lire un fichier, votre application attend que les exemples soient remis à votre méthode de rappel. La lecture asynchrone est utile pour les applications de lecteur et prend en charge les fonctionnalités non disponibles avec la lecture synchrone. si votre application doit lire des fichiers à partir d’un emplacement réseau ou interagir avec un serveur exécutant Services Windows Media, vous devez utiliser l’objet lecteur. L’inconvénient de l’objet lecteur est qu’un thread distinct est utilisé pour chaque sortie fournie. En outre, l’objet lecteur n’est pas aussi flexible que le lecteur synchrone dans la manière dont il peut fournir des exemples.

Avec le lecteur synchrone, vous n’avez pas besoin d’utiliser de méthodes de rappel. Au lieu de cela, vous sélectionnez une partie du fichier pour lire et récupérer les exemples un par un avec les appels de méthode. Le lecteur synchrone est bien adapté aux besoins des applications de modification de contenu, où l’accès rapide à des exemples spécifiques est essentiel. Étant donné qu’aucune méthode de rappel n’est utilisée par le lecteur synchrone, vous pouvez créer des applications pour lire les fichiers ASF avec un minimum de surcharge de codage. toutefois, le lecteur synchrone ne peut pas ouvrir un fichier à partir d’un emplacement réseau ou interagir avec un serveur exécutant Services Windows Media, ni lire des fichiers protégés par [*DRM*](wmformat-glossary.md).

Les rubriques suivantes décrivent les fonctionnalités du lecteur et du lecteur synchrone.



| Rubrique                                                              | Description                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Prise en charge de l’exemple alloué par l’utilisateur](user-allocated-sample-support.md) | Décrit l’allocation de mémoire tampon dans le lecteur et le lecteur synchrone, et comment l’allocation des utilisateurs peut améliorer les performances. |
| [Énumération de format de sortie](output-format-enumeration.md)         | Présente l’énumération de format de sortie.                                                                               |



 

En outre, les rubriques suivantes de la section écriture des fonctionnalités s’appliquent également à la lecture de fichiers :

-   [Redimensionnement vidéo](video-resizing.md)
-   [Conversion de l’espace colorimétrique](color-space-conversion.md)
-   [Rééchantillonnage audio](audio-resampling.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Éléments**](features.md)
</dt> <dt>

[**Lecture des fichiers ASF**](reading-asf-files.md)
</dt> </dl>

 

 




