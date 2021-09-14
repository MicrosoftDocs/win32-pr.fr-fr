---
description: Gestion des modifications de format à partir du convertisseur vidéo
ms.assetid: ac7d7b1c-3c9a-4693-87ea-0a10a8ab915c
title: Gestion des modifications de format à partir du convertisseur vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d731ac4b9d6985cf5ad92f642b6d8262209fa91d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119901"
---
# <a name="handling-format-changes-from-the-video-renderer"></a>Gestion des modifications de format à partir du convertisseur vidéo

Cette section décrit comment un filtre de décodeur ou de transformation doit gérer les modifications de format à partir du convertisseur vidéo.

**Filtre de convertisseur vidéo**

Lorsque l’ancien filtre de [convertisseur vidéo](video-renderer-filter.md) se connecte, il requiert un format RVB qui correspond au format d’affichage de l’écran principal. Cela lui permet d’utiliser GDI pour le rendu si DirectDraw n’est pas disponible. Lors du démarrage de la lecture, le convertisseur vidéo peut passer à un format compatible DirectDraw. Pour verfify si le filtre en amont peut prendre en charge le nouveau format, le convertisseur vidéo appelle [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur la broche de sortie du filtre en amont. Si le filtre amont accepte le nouveau format, la méthode **QueryAccept** retourne S \_ OK. Le convertisseur vidéo change de format en joignant un type de média avec le nouveau format à l’exemple de support suivant retourné par son allocateur. Le filtre amont doit vérifier les modifications de format en appelant [**IMediaSample :: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) sur chaque échantillon. Le convertisseur vidéo peut basculer entre le format d’origine et le nouveau format à tout moment pendant la diffusion en continu. Elle n’appelle pas **QueryAccept** après la première modification de mise en forme. Une fois que le filtre en amont a accepté le nouveau format, il doit être en mesure de basculer vers l’arrière.

Le filtre amont peut rejeter le changement de format en renvoyant S \_ false à partir de **QueryAccept**. Dans ce cas, le convertisseur vidéo continue d’utiliser GDI avec le format d’origine.

**Filtre de convertisseur de mixage vidéo**

Le filtre de convertisseur de mixage vidéo (VMR-7 et VMR-9) se connecte avec n’importe quel format pris en charge par le matériel graphique du système. VMR-7 utilise toujours DirectDraw pour le rendu et alloue les surfaces DirectDraw sous-jacentes lorsque le filtre amont se connecte. VMR-9 utilise toujours Direct3D pour le rendu et alloue les surfaces Direct3D sous-jacentes lorsque le filtre amont se connecte.

Le matériel graphique peut nécessiter un Stride plus grand que la largeur de l’image. Dans ce cas, VMR demande un nouveau format en appelant **QueryAccept**. Il signale le Stride de surface dans le membre à **bichasse** du [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) dans le format vidéo. Si le filtre amont ne retourne pas la \_ valeur S dans **QUERYACCEPT**, VMR rejette le format et tente de se connecter en utilisant le format suivant publié par le filtre amont. VMR attache le type de média avec le nouveau format au premier exemple de support. Après le premier exemple, le format reste constant. VMR ne change pas les formats lorsque le graphique est en cours d’exécution.

**Rendu vidéo amélioré (EVR)**

Le EVR utilise toujours Direct3D pour le rendu. Si une plus grande surface Stride est nécessaire, EVR utilise le même mécanisme **QueryAccept** que VMR.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[QueryAccept (en amont)](queryaccept--upstream.md)
</dt> </dl>

 

 



