---
title: Ajout d’une vidéo
description: Ajout d’une vidéo
ms.assetid: 6f20a9ad-e92e-4774-868d-ad0e071f4935
keywords:
- création d’apparences, vidéo
- apparences de Lecteur Windows Media, vidéo
- apparences, vidéo
- vidéo dans les apparences, ajout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc952f2fa80536bc6b2bb9ef3b43c6730616af3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856342"
---
# <a name="adding-video"></a>Ajout d’une vidéo

Vous pouvez ajouter une vidéo à votre fichier en utilisant simplement l’élément **Video** et en définissant l’emplacement où vous souhaitez placer la fenêtre vidéo.

Utilisez le même code que celui que vous avez fait dans la section choix des fichiers ; il vous suffit d’ajouter l’élément **vidéo** avec les attributs haut, gauche, largeur et hauteur.


```C++
        <VIDEO
            top = "10"
            left = "80"
            width = "180"
            height = "180"/>

```



Ensuite, lorsque vous lisez une vidéo, elle s’affiche dans la fenêtre. L’illustration de l’exemple de vidéo a été modifiée pour obtenir une apparence légèrement plus grande. Comme les couches étaient utilisées dans Photoshop, les boutons étaient facilement déplacés et un nouvel ensemble a été créé très rapidement. Seule l’image d’arrière-plan a été modifiée. Un remplissage a été utilisé dans une couche vide et un effet de biseau et de relief a été ajouté.

Vous pouvez voir une apparence de vidéo similaire dans la section exemple du kit de développement logiciel (SDK).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de création d’apparence**](skin-creation-guide.md)
</dt> </dl>

 

 




