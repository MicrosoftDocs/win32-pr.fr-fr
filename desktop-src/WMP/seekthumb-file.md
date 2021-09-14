---
title: Fichier SeekThumb
description: Fichier SeekThumb
ms.assetid: 757aeb93-ebf0-4659-8cb0-686e54485ac4
keywords:
- Lecteur Windows Media Skins mobiles, fichiers artistiques
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les habillages, fichiers SeekThumbd
- Lecteur Windows Media Skins mobiles, fichiers SeekThumb
- Skins, fichiers SeekThumb
- Fichiers SeekThumb dans les habillages
- Thumb, SeekThumb, fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9f1e9434a614dbc02e48b63508c7c2c04f553d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010862"
---
# <a name="seekthumb-file"></a>Fichier SeekThumb

Le fichier SeekThumb définit l’image qui indique l’emplacement de lecture dans l’élément multimédia pour un TrackBar de recherche. Vous pouvez utiliser un fichier et le définir pour une utilisation par SeekThumb et VolumeThumb. Contrairement aux autres fichiers art, les fichiers Thumb sont définis dans la section Trackbars du fichier de définition d’apparence.

L’image suivante est un fichier SeekThumb classique.

![fichier seekthumb](images/cesdksee.gif)

Ces deux fichiers de boutons sont identiques, mais leur taille est légèrement différente. L’image de gauche est l’affichage normal que l’utilisateur voit, tandis que l’image de droite est l’image que l’utilisateur voit lorsqu’il appuie sur le bouton.

> [!Note]  
> les fichiers art SeekThumb créés pour les apparences utilisées dans Lecteur Windows Media 10 Mobile ou version ultérieure doivent avoir les trois images suivantes (de gauche à droite) : normal, push et disabled.

 

Vous pouvez faire en sorte que certaines zones des images Thumb soient transparentes. Cela vous permettra de créer des images Thumb dans des formes autres que rectangulaires. Toute région d’une image Thumb que vous remplissez avec la couleur spécifiée par la valeur RVB 255, 0, 255 apparaîtra transparente dans votre apparence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fichiers art**](art-files-mobile.md)
</dt> </dl>

 

 




