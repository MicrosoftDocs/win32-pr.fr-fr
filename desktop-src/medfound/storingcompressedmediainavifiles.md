---
description: Décrit comment stocker des données Windows Media dans un fichier AVI.
ms.assetid: f2a9d9ff-4876-4f24-b96a-5d89e42fa3d5
title: Stockage d’un média compressé dans des fichiers AVI (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 080524a47b4295517d50705f6aeb125d085a8346
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321574"
---
# <a name="storing-compressed-media-in-avi-files-microsoft-media-foundation"></a>Stockage d’un média compressé dans des fichiers AVI (Microsoft Media Foundation)

Tout le contenu que vous compressez à l’aide des codecs Windows Media Audio et vidéo doit être placé dans un format de conteneur. L’un des formats les plus populaires est Audio Video entrelacé ou AVI. Vous pouvez utiliser Microsoft Video for Windows (VfW) ou Microsoft DirectShow pour créer des fichiers AVI. Pour plus d’informations sur l’utilisation de la vidéo pour Windows ou DirectShow, reportez-vous à la documentation du produit sur MSDN.

Les codecs vidéo et Windows Media Audio ont été développés pour utiliser les propriétés du format ASF (Advanced Systems Format), qui est le conteneur utilisé par Windows Media. Étant donné que les contenus AVI et ASF stockent le contenu différemment, certaines difficultés surviennent lors du stockage de contenu compressé avec les codecs Windows Media Audio et vidéo dans un fichier AVI.

Les codecs Windows Media Audio compressent le contenu audio de manière à ce qu’il ne puisse pas être correctement décompressé sans horodatage pour les échantillons individuels. Cela permet d’optimiser le support compressé. Étant donné que le conteneur ASF conserve les horodatages avec tous les échantillons, cette caractéristique des algorithmes audio a toujours fonctionné correctement.

Toutefois, les fichiers AVI ne conservent pas les horodatages avec des échantillons. Cela signifie que le contenu Windows Media Audio ne peut pas être décompressé correctement lorsqu’il est stocké dans un fichier AVI. Le contenu de Windows Media Video n’a pas cette limitation et peut être inclus dans des fichiers AVI. Pour encoder Windows Media Video contenu dans un fichier AVI avec un son synchronisé, vous devez utiliser un autre codec audio.

L’autre problème lié à l’utilisation d’un fichier AVI comme conteneur pour Windows Media concerne la vidéo à faible vitesse de transmission. L’une des façons dont les codecs Windows Media Video produisent du contenu vidéo pour des vitesses de transmission faibles consiste à déposer des frames en double. Si vous souhaitez placer Windows Media Video contenu dans un fichier ASF, vous devez définir l’encodeur pour fournir des frames factices pour les trames dupliquées (définissez [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) sur variant \_ true) afin que chaque frame soit représenté dans le fichier. La taille des frames factices produits par le codec est de 8 octets. Toutefois, le frame écrit dans un fichier par le multiplexeur AVI peut avoir des centaines d’octets plus grands et remplir des données aléatoires. Un fichier AVI créé de cette façon sera toujours lisible, mais il sera bien plus grand que prévu. Vous pouvez éviter ce problème en utilisant des taux de bits plus élevés lors de l’encodage vidéo pour le stockage dans des fichiers AVI.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codecs Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



