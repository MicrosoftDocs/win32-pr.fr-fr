---
description: En savoir plus sur les exemples de média dans Microsoft Media Foundation. Un exemple de média est un objet qui contient une liste triée de zéro ou plusieurs mémoires tampons.
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Exemples de supports (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83bad0186d54d99b6c7f7666a5971f6c35e8e2a561109e7bfd6afd45fd5f5e6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061069"
---
# <a name="media-samples-microsoft-media-foundation"></a>Exemples de supports (Microsoft Media Foundation)

Un exemple de média est un objet qui contient une liste triée de zéro ou plusieurs mémoires tampons. Les exemples de supports exposent l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) . La quantité de données contenues dans un échantillon dépend du composant qui crée l’échantillon et du type de données dans les mémoires tampons. Pour une vidéo non compressée, un échantillon contient généralement une seule image vidéo. Pour le son non compressé, la quantité de données peut varier, mais généralement une trame audio ne couvre pas deux échantillons. Pour les données compressées, ces instructions peuvent ne pas s’appliquer.

Un seul échantillon peut contenir plusieurs mémoires tampons pour des raisons d’efficacité. Par exemple, dans un fichier ASF, une image vidéo est souvent répartie entre plusieurs paquets ASF. La source du média peut lire les paquets dans plusieurs mémoires tampons. Au lieu de copier chaque fragment dans une mémoire tampon, la source place simplement toutes les mémoires tampon dans un seul échantillon. Les composants en aval peuvent ensuite décider s’il faut copier les mémoires tampons plus petites dans une seule mémoire tampon contiguë. En règle générale, si vous écrivez un composant de pipeline, vous devez supposer que tout exemple peut contenir plusieurs mémoires tampons.

Cette section contient les rubriques suivantes :



| Rubrique                                                        | Description                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Utilisation des exemples de supports](working-with-media-samples.md) | Décrit le comportement général des exemples de supports.                                                                         |
| [Exemples vidéo](video-samples.md)                           | Décrit une implémentation spécialisée de [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) conçue pour contenir des images vidéo non compressées. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de média](media-buffers.md)
</dt> <dt>

[Primitives de Media Foundation](media-foundation-primitives.md)
</dt> </dl>

 

 



