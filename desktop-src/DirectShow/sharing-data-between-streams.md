---
description: Partage de données entre des flux
ms.assetid: e18eecf8-9475-420a-9a60-4b1b5f8fd43a
title: Partage de données entre des flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0b2f53fe1952bbc16711f7c7e39c3182ba94a7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481976"
---
# <a name="sharing-data-between-streams"></a>Partage de données entre des flux

> [!Note]  
> Ces API sont déconseillées. Les applications doivent utiliser le filtre d' [**accrochage d’exemple**](sample-grabber-filter.md) ou implémenter un filtre personnalisé pour obtenir des données à partir d’un graphique de filtre DirectShow.

 

Le traitement des données multimédias nécessite généralement une grande quantité de ressources système. par conséquent, vous devez éviter de copier les données dans la mesure du possible. L’architecture de streaming prend en charge les exemples de flux partagés, un mécanisme qui déplace les données d’un flux vers un autre sans les copier. Cette mémoire tampon permet le transport efficace de données entre deux flux, même si le flux de destination ne prend pas spécifiquement en charge le format de données sous-jacent.

Par exemple, supposons que vous disposez d’un flux multimédia avec trois flux de données : vidéo et audio, et les données d’URL sont horodatées pour correspondre au contenu de la vidéo. Vous souhaitez écrire une application qui ajoute une mention de droits d’auteur sur chaque image vidéo et écrit les données dans un autre flux de données pour le stockage, mais votre application ne comprend aucun format de données à l’exception du flux vidéo. Pour le flux vidéo, vous créez un exemple attaché à la surface DirectDraw souhaitée. Vous pouvez ensuite créer un flux de sortie en appelant la méthode [**IDirectDrawMediaStream :: CreateSample**](/previous-versions/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-createsample) avec ce pointeur sur la même surface ou [**IMediaStream :: CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample). Dans les deux cas, les flux d’entrée et de sortie partagent la surface DirectDraw. Étant donné que vous comprenez le format vidéo, vous pouvez accéder à cette surface en fonction des besoins.

Pour récupérer les autres pointeurs de flux source (audio et URL), énumérez le flux de conteneur source et récupérez les pointeurs vers les flux qui ne sont pas des vidéos. Chacun de ces flux source est associé à un flux de sortie dans le conteneur du flux de sortie. Récupérez ces pointeurs de sortie en appelant la méthode [**IMultiMediaStream :: GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) sur le conteneur de sortie avec chacun des pointeurs de flux source. Les étapes de ce processus sont décrites ci-dessous.

1.  Appelez [**IMultiMediaStream :: EnumMediaStreams**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-enummediastreams) pour récupérer un pointeur vers un flux source. Assurez-vous qu’il ne s’agit pas du flux vidéo, car votre application comprend déjà son format.
2.  Appelez [**IMultiMediaStream :: GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) sur le flux de conteneur de sortie avec le pointeur de l’étape 1. Cela retourne un pointeur vers le flux de sortie souhaité.
3.  Appelez [**AllocateSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-allocatesample) sur le flux source.
4.  Appelez [**CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) sur le flux de sortie.
5.  Appelez [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) sur le flux source pour lire les données.
6.  Appelez [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) sur le flux de sortie pour écrire les données.

Répétez ces étapes pour chaque flux dont le format n’est pas pris en charge. Lorsque les deux exemples terminent la mise à jour, le flux de sortie contient toutes les données du flux source et vous avez terminé.

 

 



